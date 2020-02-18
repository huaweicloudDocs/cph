# ADB方式（公网）<a name="cph_ug_0010"></a>

ADB方式连接云手机包括两个步骤：建立SSH隧道；通过ADB连接云手机。用来连接云手机的本地物理设备需开通公网，并安装SSH客户端服务（比如OpenSSH），本地设备的操作系统可以为Windows、Linux或Mac OS，本节操作以Windows系统为例。

## 准备工作<a name="section13533746254"></a>

建立SSH隧道前，您需要登录云手机管理控制台，并完成如下准备工作：

1.  <a name="li292753322516"></a>获取云手机所在区域的项目ID。方法如下：
    1.  在右上角用户名的下拉列表中，选择“我的凭证”。

        ![](figures/10.png)

    2.  在“API凭证 \> 项目列表”中，获取待连接的云手机所在区域的“项目ID”。

        以“华东-上海一”为例：

        ![](figures/11.png)

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >若项目ID位数多于32位，则取前32位作为建立SSH隧道的用户名。  


2.  <a name="li918704218111"></a>选择一个本地设备中任意未被占用的端口，用来和云手机建立连接。

    您可以执行**netstat -an**命令，查看端口占用情况：

    如下图，6667端口已被其他程序占用，而1234端口空闲。

    ![](figures/zh-cn_image_0223476130.png)

3.  <a name="li827525992514"></a>获取云手机监听地址，即云手机的内网IP与端口。方法如下：
    1.  在云手机控制台，选择左侧导航中的“云手机 \> 云手机管理”，单击待连接云手机的名称，进入云手机详情页面。

        ![](figures/29.png)

    2.  在“应用端口”区域获取ADB应用对应的云手机监听地址。

        ![](figures/30.png)

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >-   如果在购买云手机服务器时，在高级配置中自定义了应用端口，这里会显示这些端口信息。SSH隧道鉴权方式与使用默认的ADB端口一样，只需要将云手机监听地址替换为对应端口的云手机监听地址即可。  
        >-   若创建自定义应用端口时勾选了“公网访问”，则此处会显示对应端口的公网访问地址，用户可以通过公网直接访问此端口到云手机，但要注意安全风险。  


4.  <a name="li12571818103710"></a>获取云手机服务器的公网IP地址。方法如下：

    在云手机控制台，选择左侧导航中的“云手机 \> 云手机服务器管理”，单击![](figures/31.png)图标，展开云手机服务器详情，获取“IP”参数的取值。

    ![](figures/27.png)

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >如果有多台云手机服务器，请根据云手机名称来判断云手机所属服务器是哪一台。例如，云手机名称为cph-test-1-00001，那么对应的云手机服务器名称为cph-test-1。  

5.  <a name="li5745145662516"></a>获取云手机服务器的密钥对对应的私钥文件在本地的保存路径，即[购买云手机实例](购买云手机实例.md)步骤[7](购买云手机实例.md#li1875842514113)中创建密钥对时保存在本地的私钥文件路径，例如：C:\\Users\\Administrator\\Downloads\\KeyPair-a49c.pem。路径不区分大小写，推荐您使用全英文路径。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >如果云手机服务器的密钥对对应的私钥文件丢失，请参考[私钥文件丢失，怎么办？](https://support.huaweicloud.com/cph_faq/cph_faq_0010.html)。  


## 步骤1：建立SSH隧道<a name="section9258213142515"></a>

1.  在本地设备打开命令提示符窗口，以Windows 10操作系统为例，方法如下：

    同时按下“Win + R”，在打开的“运行”对话框中输入**cmd**，按“Enter”。

2.  <a name="li213212132583"></a>执行以下命令，建立SSH隧道。

    **ssh -L 本地空闲端口:云手机监听地址 SSH隧道用户名@公网IP地址 -i 私钥文件路径 -Nf**

    各参数说明及获取方式如下所述：

    -   **本地空闲端口**：用户自由选择的本地设备中任意未被占用的端口，通过该端口映射云手机应用端口。获取方式见[2](#li918704218111)。
    -   **云手机监听地址**：云手机的内网IP与端口。获取方式见[3](#li827525992514)。
    -   **SSH隧道用户名**：云手机所在区域的项目ID。获取方式见[1](#li292753322516)。
    -   **公网IP地址**：云手机服务器的公网IP。获取方式见[4](#li12571818103710)。
    -   **私钥文件路径**：云手机服务器的密钥对对应的私钥文件在本地的保存路径。获取方式见[5](#li5745145662516)。

    假设本地空闲端口为1234，云手机监听地址为10.237.0.61:5555，SSH隧道用户名为05e1aexxx，公网IP地址为xxx.xxx.xxx.xxx，私钥文件路径为C:\\Users\\Administrator\\Downloads\\KeyPair-a49c.pem，命令如下：

    **ssh -L 1234:10.237.0.54:5555 05e1aexxx@xxx.xxx.xxx.xxx -i C:\\Users\\Administrator\\Downloads\\KeyPair-a49c.pem -Nf**

    该命令表示从本地PC建立一个到云手机的SSH隧道，使用本地端口转发模式，监听本地PC的1234端口；访问本地PC的1234端口时，通信数据将会被转发到云手机的5555端口。

    执行命令后，SSH程序会在后台执行隧道的转发，执行后无报错即为SSH隧道建立成功。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >若执行命令后报“too open”错误，请参考[建立SSH隧道时报错“too open”？](https://support.huaweicloud.com/cph_faq/cph_faq_0008.html)处理。  


## 步骤2：通过ADB连接云手机<a name="section1650324092412"></a>

1.  下载ADB工具。

    访问[https://developer.android.com/studio/releases/platform-tools](https://developer.android.com/studio/releases/platform-tools)，选择“Download SDK Platform-Tools for Windows”。

    ![](figures/38.png)

    在弹出的对话框中勾选“I have read and agree with the above terms and conditions”，并单击“DOWNLOAD ANDROID SDK PLATFORM-TOOLS FOR WINDOWS”进行下载。

2.  下载后得到“platform-tools\_r29.0.5-windows.zip”文件，解压该zip文件至您选定的目录，例如“C:\\Users\\Administrator\\Downloads”。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >“platform-tools\_r29.0.5-windows.zip”文件中的版本号“29.0.5”仅为示例，请以实际下载的版本为准。  

3.  打开命令提示符窗口，进入“C:\\Users\\Administrator\\Downloads\\platform-tools”目录。

    **cd C:\\Users\\Administrator\\Downloads\\platform-tools**

    ![](figures/18.png)

4.  执行如下ADB命令，创建与云手机的ADB连接。

    **adb connect 127.0.0.1:本地空闲端口**

    其中，本地空闲端口为[2](#li213212132583)中所使用的空闲端口。

    ![](figures/19.png)

5.  检测当前端口是否已连接，可输入**adb devices**命令检查。

    ![](figures/20.png)

6.  执行相关ADB命令，开始操作云手机，如adb shell命令。

    ![](figures/21.png)

7.  安装手机APK程序至云手机。

    云手机没有自带浏览器或相关应用市场，如果您想要在云手机内安装APP，可以自行找一个APP的apk包使用ADB命令传递至云手机上去安装。命令为：

    **adb -s 127.0.0.1:本地空闲端口 install 需要安装的APK所在路径**

    如图：

    ![](figures/23.png)


