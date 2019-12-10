# 卸载apk<a name="ZH-CN_TOPIC_0167640655"></a>

## 功能介绍<a name="section115949747"></a>

-   接口名称

    UninstallApk

-   功能描述

    实时在手机中卸载apk。


## URI<a name="section9161799415"></a>

-   URI格式

    POST /v1/\{project\_id\}/cloud-phone/phones/commands

-   参数说明

    <a name="table191631896414"></a>
    <table><thead align="left"><tr id="row10274091143"><th class="cellrowborder" valign="top" width="24.490000000000002%" id="mcps1.1.5.1.1"><p id="p427489747"><a name="p427489747"></a><a name="p427489747"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.43%" id="mcps1.1.5.1.2"><p id="p727417917416"><a name="p727417917416"></a><a name="p727417917416"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.41%" id="mcps1.1.5.1.3"><p id="p122741299412"><a name="p122741299412"></a><a name="p122741299412"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.67%" id="mcps1.1.5.1.4"><p id="p2274895413"><a name="p2274895413"></a><a name="p2274895413"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row11274791349"><td class="cellrowborder" valign="top" width="24.490000000000002%" headers="mcps1.1.5.1.1 "><p id="p10274491843"><a name="p10274491843"></a><a name="p10274491843"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.43%" headers="mcps1.1.5.1.2 "><p id="p5274491848"><a name="p5274491848"></a><a name="p5274491848"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.41%" headers="mcps1.1.5.1.3 "><p id="p7633781"><a name="p7633781"></a><a name="p7633781"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.5.1.4 "><p id="p18834193641812"><a name="p18834193641812"></a><a name="p18834193641812"></a>项目ID</p>
    <p id="p98341736131817"><a name="p98341736131817"></a><a name="p98341736131817"></a>获取项目ID请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section2016979147"></a>

-   参数说明

    <a name="table51721899413"></a>
    <table><thead align="left"><tr id="row9274791249"><th class="cellrowborder" valign="top" width="24.6%" id="mcps1.1.5.1.1"><p id="p82741491144"><a name="p82741491144"></a><a name="p82741491144"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.46%" id="mcps1.1.5.1.2"><p id="p8274209844"><a name="p8274209844"></a><a name="p8274209844"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="22%" id="mcps1.1.5.1.3"><p id="p8274139542"><a name="p8274139542"></a><a name="p8274139542"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.94%" id="mcps1.1.5.1.4"><p id="p82741091147"><a name="p82741091147"></a><a name="p82741091147"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1527416920417"><td class="cellrowborder" valign="top" width="24.6%" headers="mcps1.1.5.1.1 "><p id="p1927439248"><a name="p1927439248"></a><a name="p1927439248"></a>command</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.46%" headers="mcps1.1.5.1.2 "><p id="p182745919411"><a name="p182745919411"></a><a name="p182745919411"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.5.1.3 "><p id="p11274397412"><a name="p11274397412"></a><a name="p11274397412"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.4 "><p id="p132741891416"><a name="p132741891416"></a><a name="p132741891416"></a>adb命令，固定填写uninstall。</p>
    </td>
    </tr>
    <tr id="row17274792420"><td class="cellrowborder" valign="top" width="24.6%" headers="mcps1.1.5.1.1 "><p id="p427412910417"><a name="p427412910417"></a><a name="p427412910417"></a>content</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.46%" headers="mcps1.1.5.1.2 "><p id="p9274149946"><a name="p9274149946"></a><a name="p9274149946"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.5.1.3 "><p id="p32745914411"><a name="p32745914411"></a><a name="p32745914411"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.4 "><p id="p48361447101517"><a name="p48361447101517"></a><a name="p48361447101517"></a>待卸载的APP名称。</p>
    <p id="p427412916420"><a name="p427412916420"></a><a name="p427412916420"></a>最大长度为1024字节，只支持大小写字母、数字、下划线_、点.、斜线/、冒号:、中划线 -</p>
    </td>
    </tr>
    <tr id="row132741691416"><td class="cellrowborder" valign="top" width="24.6%" headers="mcps1.1.5.1.1 "><p id="p02741291413"><a name="p02741291413"></a><a name="p02741291413"></a>server_ids</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.46%" headers="mcps1.1.5.1.2 "><p id="p209051820181117"><a name="p209051820181117"></a><a name="p209051820181117"></a>否</p>
    <p id="p122741395417"><a name="p122741395417"></a><a name="p122741395417"></a>phone_ids参数不存在时必选</p>
    </td>
    <td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.5.1.3 "><p id="p92751896419"><a name="p92751896419"></a><a name="p92751896419"></a>server_id数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.4 "><p id="p182751894413"><a name="p182751894413"></a><a name="p182751894413"></a>云手机服务器ID列表</p>
    <p id="p255431071419"><a name="p255431071419"></a><a name="p255431071419"></a>通过<a href="查询云手机服务器列表.md">查询云手机服务器列表</a>获取。</p>
    </td>
    </tr>
    <tr id="row4275991444"><td class="cellrowborder" valign="top" width="24.6%" headers="mcps1.1.5.1.1 "><p id="p1927599541"><a name="p1927599541"></a><a name="p1927599541"></a>phone_ids</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.46%" headers="mcps1.1.5.1.2 "><p id="p6826623101119"><a name="p6826623101119"></a><a name="p6826623101119"></a>否</p>
    <p id="p5275891843"><a name="p5275891843"></a><a name="p5275891843"></a>server_ids参数不存在时必选</p>
    </td>
    <td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.5.1.3 "><p id="p327511917413"><a name="p327511917413"></a><a name="p327511917413"></a>phone_id数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.4 "><p id="p627519912414"><a name="p627519912414"></a><a name="p627519912414"></a>云手机ID列表</p>
    <p id="p124279151919"><a name="p124279151919"></a><a name="p124279151919"></a>通过<a href="查询云手机列表.md">查询云手机列表</a>获取。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    POST https://{CPH_Endpoint}/v1/{project_id}/cloud-phone/phones/commands{
       "command": "uninstall",
       "content": "com.myapp.test",
       "phone_ids":[
            "1234567b8bab40ffb711234cb80d0234",
            "1678567b8bab40f93711234cb80d0764"
         ]
    }
    ```


## 响应<a name="section151851291647"></a>

-   要素说明

    <a name="table1418719042"></a>
    <table><thead align="left"><tr id="row122751592413"><th class="cellrowborder" valign="top" width="25.509999999999998%" id="mcps1.1.4.1.1"><p id="p112751792419"><a name="p112751792419"></a><a name="p112751792419"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.67%" id="mcps1.1.4.1.2"><p id="p32751992417"><a name="p32751992417"></a><a name="p32751992417"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.82%" id="mcps1.1.4.1.3"><p id="p1427519916410"><a name="p1427519916410"></a><a name="p1427519916410"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row72751191947"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.1.4.1.1 "><p id="p32752916411"><a name="p32752916411"></a><a name="p32752916411"></a>request_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.4.1.2 "><p id="p152751911415"><a name="p152751911415"></a><a name="p152751911415"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.82%" headers="mcps1.1.4.1.3 "><p id="p827549142"><a name="p827549142"></a><a name="p827549142"></a>请求的唯一标识ID。</p>
    </td>
    </tr>
    <tr id="row1227517910416"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.1.4.1.1 "><p id="p16275119743"><a name="p16275119743"></a><a name="p16275119743"></a>jobs</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.4.1.2 "><p id="p152751393414"><a name="p152751393414"></a><a name="p152751393414"></a>job结构体数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.82%" headers="mcps1.1.4.1.3 "><p id="p162751391243"><a name="p162751391243"></a><a name="p162751391243"></a>请参见<a href="#table1131122810124">表1</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 1**  job结构体

    <a name="table1131122810124"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0149256134_row103731228111213"><th class="cellrowborder" valign="top" width="29.292929292929294%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0149256134_p17373328111217"><a name="zh-cn_topic_0149256134_p17373328111217"></a><a name="zh-cn_topic_0149256134_p17373328111217"></a><strong id="zh-cn_topic_0149256134_b93733289125"><a name="zh-cn_topic_0149256134_b93733289125"></a><a name="zh-cn_topic_0149256134_b93733289125"></a>名称</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="28.28282828282828%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0149256134_p0373122821217"><a name="zh-cn_topic_0149256134_p0373122821217"></a><a name="zh-cn_topic_0149256134_p0373122821217"></a><strong id="zh-cn_topic_0149256134_b16373122812126"><a name="zh-cn_topic_0149256134_b16373122812126"></a><a name="zh-cn_topic_0149256134_b16373122812126"></a>参数类型</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="42.42424242424242%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0149256134_p1373172815123"><a name="zh-cn_topic_0149256134_p1373172815123"></a><a name="zh-cn_topic_0149256134_p1373172815123"></a><strong id="zh-cn_topic_0149256134_b1337315282122"><a name="zh-cn_topic_0149256134_b1337315282122"></a><a name="zh-cn_topic_0149256134_b1337315282122"></a>说明</strong></p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0149256134_row237413281129"><td class="cellrowborder" valign="top" width="29.292929292929294%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0149256134_p15374132821219"><a name="zh-cn_topic_0149256134_p15374132821219"></a><a name="zh-cn_topic_0149256134_p15374132821219"></a>phone_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.28282828282828%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0149256134_p037414288128"><a name="zh-cn_topic_0149256134_p037414288128"></a><a name="zh-cn_topic_0149256134_p037414288128"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="42.42424242424242%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0149256134_p23741128101211"><a name="zh-cn_topic_0149256134_p23741128101211"></a><a name="zh-cn_topic_0149256134_p23741128101211"></a>云手机的唯一标识。phone相关任务包含此字段</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0149256134_row12374192819123"><td class="cellrowborder" valign="top" width="29.292929292929294%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0149256134_p437415281123"><a name="zh-cn_topic_0149256134_p437415281123"></a><a name="zh-cn_topic_0149256134_p437415281123"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.28282828282828%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0149256134_p11374182810129"><a name="zh-cn_topic_0149256134_p11374182810129"></a><a name="zh-cn_topic_0149256134_p11374182810129"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="42.42424242424242%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0149256134_p1937442831217"><a name="zh-cn_topic_0149256134_p1937442831217"></a><a name="zh-cn_topic_0149256134_p1937442831217"></a>任务的唯一标识。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
           "request_id": "6837531fd3f54550927b930180a706bf",
           "jobs":  [
                 {
                 "phone_id":  "1234567b8bab40ffb711234cb80d0234",
                 "job_id":  "1564567b8bab40f34711234cb80d0123"
              },
             {
                 "phone_id":  "1678567b8bab40f93711234cb80d0764",
                 "job_id":  "1564567b8bab40f34711234cb80d5678"
             }
       ] }
    ```


## 返回值<a name="section4200159446"></a>

请参考[返回值](返回值.md)。

