# 安装apk<a name="ZH-CN_TOPIC_0167640654"></a>

## 功能介绍<a name="section4320541733"></a>

-   接口名称

    InstallApk

-   功能描述

    实时在手机中安装apk，系统会将指定的apk文件下载后直接安装到手机中，一次只支持安装一个apk。


## URI<a name="section1135185418310"></a>

-   URI格式

    POST /v1/\{project\_id\}/cloud-phone/phones/commands

-   参数说明

    <a name="table203716540318"></a>
    <table><thead align="left"><tr id="row17167115413312"><th class="cellrowborder" valign="top" width="24.490000000000002%" id="mcps1.1.5.1.1"><p id="p516713542311"><a name="p516713542311"></a><a name="p516713542311"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.43%" id="mcps1.1.5.1.2"><p id="p81674549314"><a name="p81674549314"></a><a name="p81674549314"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.41%" id="mcps1.1.5.1.3"><p id="p5167054232"><a name="p5167054232"></a><a name="p5167054232"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.67%" id="mcps1.1.5.1.4"><p id="p12167165412315"><a name="p12167165412315"></a><a name="p12167165412315"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row61671354831"><td class="cellrowborder" valign="top" width="24.490000000000002%" headers="mcps1.1.5.1.1 "><p id="p1216719541531"><a name="p1216719541531"></a><a name="p1216719541531"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.43%" headers="mcps1.1.5.1.2 "><p id="p171677541032"><a name="p171677541032"></a><a name="p171677541032"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.41%" headers="mcps1.1.5.1.3 "><p id="p7633781"><a name="p7633781"></a><a name="p7633781"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.5.1.4 "><p id="p18834193641812"><a name="p18834193641812"></a><a name="p18834193641812"></a>项目ID</p>
    <p id="p98341736131817"><a name="p98341736131817"></a><a name="p98341736131817"></a>获取项目ID请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section94213541135"></a>

-   参数说明

    <a name="table12466541314"></a>
    <table><thead align="left"><tr id="row71675541031"><th class="cellrowborder" valign="top" width="28.57%" id="mcps1.1.5.1.1"><p id="p13167175411315"><a name="p13167175411315"></a><a name="p13167175411315"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.490000000000002%" id="mcps1.1.5.1.2"><p id="p1216710542033"><a name="p1216710542033"></a><a name="p1216710542033"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.47%" id="mcps1.1.5.1.3"><p id="p616810542320"><a name="p616810542320"></a><a name="p616810542320"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.47%" id="mcps1.1.5.1.4"><p id="p31682546313"><a name="p31682546313"></a><a name="p31682546313"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row91680541838"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.5.1.1 "><p id="p1016813543314"><a name="p1016813543314"></a><a name="p1016813543314"></a>command</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.490000000000002%" headers="mcps1.1.5.1.2 "><p id="p516811543310"><a name="p516811543310"></a><a name="p516811543310"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.47%" headers="mcps1.1.5.1.3 "><p id="p61680541734"><a name="p61680541734"></a><a name="p61680541734"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.47%" headers="mcps1.1.5.1.4 "><p id="p101686541036"><a name="p101686541036"></a><a name="p101686541036"></a>adb命令，固定填写install。</p>
    </td>
    </tr>
    <tr id="row13168554235"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.5.1.1 "><p id="p121682541436"><a name="p121682541436"></a><a name="p121682541436"></a>content</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.490000000000002%" headers="mcps1.1.5.1.2 "><p id="p016817541339"><a name="p016817541339"></a><a name="p016817541339"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.47%" headers="mcps1.1.5.1.3 "><p id="p61684541536"><a name="p61684541536"></a><a name="p61684541536"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.47%" headers="mcps1.1.5.1.4 "><p id="p13191111318175"><a name="p13191111318175"></a><a name="p13191111318175"></a>指定的是obs桶中的apk文件（需要提前上传到指定桶中）</p>
    <p id="p1216875416310"><a name="p1216875416310"></a><a name="p1216875416310"></a>最大长度为1024字节，只支持大小写字母、数字、下划线_、点.、斜线/、冒号:、中划线 -。推送的文件只支持tar文件类型。文件格式：obs://obs-bucket-name/obs-file-path/file.apk。命令以文件参数结尾。</p>
    </td>
    </tr>
    <tr id="row101689541134"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.5.1.1 "><p id="p61681354339"><a name="p61681354339"></a><a name="p61681354339"></a>server_ids</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.490000000000002%" headers="mcps1.1.5.1.2 "><p id="p0671586913"><a name="p0671586913"></a><a name="p0671586913"></a>否</p>
    <p id="p1616805410314"><a name="p1616805410314"></a><a name="p1616805410314"></a>phone_ids参数不存在时必选</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.47%" headers="mcps1.1.5.1.3 "><p id="p61681354137"><a name="p61681354137"></a><a name="p61681354137"></a>server_id数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.47%" headers="mcps1.1.5.1.4 "><p id="p1016811541310"><a name="p1016811541310"></a><a name="p1016811541310"></a>云手机服务器ID列表</p>
    <p id="p578955201414"><a name="p578955201414"></a><a name="p578955201414"></a>通过<a href="查询云手机服务器列表.md">查询云手机服务器列表</a>获取。</p>
    </td>
    </tr>
    <tr id="row71681541137"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.5.1.1 "><p id="p141682542035"><a name="p141682542035"></a><a name="p141682542035"></a>phone_ids</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.490000000000002%" headers="mcps1.1.5.1.2 "><p id="p137678114910"><a name="p137678114910"></a><a name="p137678114910"></a>否</p>
    <p id="p1016919546318"><a name="p1016919546318"></a><a name="p1016919546318"></a>server_ids参数不存在时必选</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.47%" headers="mcps1.1.5.1.3 "><p id="p18169195414311"><a name="p18169195414311"></a><a name="p18169195414311"></a>phone_id数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.47%" headers="mcps1.1.5.1.4 "><p id="p31691954834"><a name="p31691954834"></a><a name="p31691954834"></a>云手机ID列表</p>
    <p id="p124279151919"><a name="p124279151919"></a><a name="p124279151919"></a>通过<a href="查询云手机列表.md">查询云手机列表</a>获取。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    POST https://{CPH_Endpoint}/v1/{project_id}/cloud-phone/phones/commands{
        "command": "install",
        "content": "-t -r obs://push-bucket/my_apps/test.apk",
        "phone_ids":[
            "1234567b8bab40ffb711234cb80d0234",
            "1678567b8bab40f93711234cb80d0764"
         ]
    }
    ```


## 响应<a name="section76520544316"></a>

-   要素说明

    <a name="table5671454332"></a>
    <table><thead align="left"><tr id="row1216912545318"><th class="cellrowborder" valign="top" width="25.509999999999998%" id="mcps1.1.4.1.1"><p id="p19169195412310"><a name="p19169195412310"></a><a name="p19169195412310"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.67%" id="mcps1.1.4.1.2"><p id="p31691954236"><a name="p31691954236"></a><a name="p31691954236"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.82%" id="mcps1.1.4.1.3"><p id="p1116912542312"><a name="p1116912542312"></a><a name="p1116912542312"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row121696541231"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.1.4.1.1 "><p id="p101693548320"><a name="p101693548320"></a><a name="p101693548320"></a>request_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.4.1.2 "><p id="p81696549314"><a name="p81696549314"></a><a name="p81696549314"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.82%" headers="mcps1.1.4.1.3 "><p id="p1516910540312"><a name="p1516910540312"></a><a name="p1516910540312"></a>请求的唯一标识ID。</p>
    </td>
    </tr>
    <tr id="row51691554432"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.1.4.1.1 "><p id="p516915417312"><a name="p516915417312"></a><a name="p516915417312"></a>jobs</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.4.1.2 "><p id="p1616920542316"><a name="p1616920542316"></a><a name="p1616920542316"></a>job结构体数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.82%" headers="mcps1.1.4.1.3 "><p id="p71690541430"><a name="p71690541430"></a><a name="p71690541430"></a>请参见<a href="#table1131122810124">表1</a>。</p>
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
                 "phone_id": "1234567b8bab40ffb711234cb80d0234",
                 "job_id": "1564567b8bab40f34711234cb80d0123"
             },
             {
                 "phone_id": "1678567b8bab40f93711234cb80d0764",
                 "job_id": "1564567b8bab40f34711234cb80d5678"
             }
       ] }
    ```


## 返回值<a name="section1674115420313"></a>

请参考[返回值](返回值.md)。

