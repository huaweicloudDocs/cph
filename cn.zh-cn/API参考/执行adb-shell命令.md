# 执行adb shell命令<a name="ZH-CN_TOPIC_0167640656"></a>

## 功能介绍<a name="section155694211249"></a>

-   接口名称

    RunShellCommand

-   功能描述

    实时在手机中执行shell命令。


## URI<a name="section1757211211549"></a>

-   URI格式

    POST /v1/\{project\_id\}/cloud-phone/phones/commands

-   参数说明

    <a name="table14575202115413"></a>
    <table><thead align="left"><tr id="row468917215410"><th class="cellrowborder" valign="top" width="24.490000000000002%" id="mcps1.1.5.1.1"><p id="p1868992116417"><a name="p1868992116417"></a><a name="p1868992116417"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.43%" id="mcps1.1.5.1.2"><p id="p1168912217412"><a name="p1168912217412"></a><a name="p1168912217412"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.41%" id="mcps1.1.5.1.3"><p id="p176890211744"><a name="p176890211744"></a><a name="p176890211744"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.67%" id="mcps1.1.5.1.4"><p id="p268916211847"><a name="p268916211847"></a><a name="p268916211847"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1689112112412"><td class="cellrowborder" valign="top" width="24.490000000000002%" headers="mcps1.1.5.1.1 "><p id="p16899212420"><a name="p16899212420"></a><a name="p16899212420"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.43%" headers="mcps1.1.5.1.2 "><p id="p7689142118417"><a name="p7689142118417"></a><a name="p7689142118417"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.41%" headers="mcps1.1.5.1.3 "><p id="p7633781"><a name="p7633781"></a><a name="p7633781"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.5.1.4 "><p id="p18834193641812"><a name="p18834193641812"></a><a name="p18834193641812"></a>项目ID</p>
    <p id="p98341736131817"><a name="p98341736131817"></a><a name="p98341736131817"></a>获取项目ID请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section17581721746"></a>

-   参数说明

    <a name="table358619211341"></a>
    <table><thead align="left"><tr id="row11689152116413"><th class="cellrowborder" valign="top" width="20.49%" id="mcps1.1.5.1.1"><p id="p46891121646"><a name="p46891121646"></a><a name="p46891121646"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.799999999999997%" id="mcps1.1.5.1.2"><p id="p12690102113417"><a name="p12690102113417"></a><a name="p12690102113417"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.490000000000002%" id="mcps1.1.5.1.3"><p id="p7690122114412"><a name="p7690122114412"></a><a name="p7690122114412"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.220000000000002%" id="mcps1.1.5.1.4"><p id="p16690102115415"><a name="p16690102115415"></a><a name="p16690102115415"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row196901321746"><td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.1.5.1.1 "><p id="p20690192118410"><a name="p20690192118410"></a><a name="p20690192118410"></a>command</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.5.1.2 "><p id="p1869017211741"><a name="p1869017211741"></a><a name="p1869017211741"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.490000000000002%" headers="mcps1.1.5.1.3 "><p id="p169018211946"><a name="p169018211946"></a><a name="p169018211946"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.220000000000002%" headers="mcps1.1.5.1.4 "><p id="p869012211047"><a name="p869012211047"></a><a name="p869012211047"></a>adb命令，固定填写shell。</p>
    </td>
    </tr>
    <tr id="row146901021746"><td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.1.5.1.1 "><p id="p18690192118416"><a name="p18690192118416"></a><a name="p18690192118416"></a>content</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.5.1.2 "><p id="p169042119413"><a name="p169042119413"></a><a name="p169042119413"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.490000000000002%" headers="mcps1.1.5.1.3 "><p id="p176901219413"><a name="p176901219413"></a><a name="p176901219413"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.220000000000002%" headers="mcps1.1.5.1.4 "><p id="p87621553161219"><a name="p87621553161219"></a><a name="p87621553161219"></a>待执行的命令。</p>
    <p id="p206904211745"><a name="p206904211745"></a><a name="p206904211745"></a>最大长度为1024字节，只支持大小写字母、数字、下划线_、点.、斜线/、冒号:、中划线 -</p>
    </td>
    </tr>
    <tr id="row16690162120418"><td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.1.5.1.1 "><p id="p1669019211947"><a name="p1669019211947"></a><a name="p1669019211947"></a>server_ids</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.5.1.2 "><p id="p94533146137"><a name="p94533146137"></a><a name="p94533146137"></a>否</p>
    <p id="p1469011211949"><a name="p1469011211949"></a><a name="p1469011211949"></a>phone_ids参数不存在时必选</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.490000000000002%" headers="mcps1.1.5.1.3 "><p id="p1769072119417"><a name="p1769072119417"></a><a name="p1769072119417"></a>server_id数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.220000000000002%" headers="mcps1.1.5.1.4 "><p id="p6690821347"><a name="p6690821347"></a><a name="p6690821347"></a>云手机服务器ID列表</p>
    <p id="p24784209148"><a name="p24784209148"></a><a name="p24784209148"></a>通过<a href="查询云手机服务器列表.md">查询云手机服务器列表</a>获取。</p>
    </td>
    </tr>
    <tr id="row8690202112412"><td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.1.5.1.1 "><p id="p196905211748"><a name="p196905211748"></a><a name="p196905211748"></a>phone_ids</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.5.1.2 "><p id="p0440141731311"><a name="p0440141731311"></a><a name="p0440141731311"></a>否</p>
    <p id="p2690182118419"><a name="p2690182118419"></a><a name="p2690182118419"></a>server_ids参数不存在时必选</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.490000000000002%" headers="mcps1.1.5.1.3 "><p id="p16909211244"><a name="p16909211244"></a><a name="p16909211244"></a>phone_id数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.220000000000002%" headers="mcps1.1.5.1.4 "><p id="p1369017216419"><a name="p1369017216419"></a><a name="p1369017216419"></a>云手机ID列表</p>
    <p id="p124279151919"><a name="p124279151919"></a><a name="p124279151919"></a>通过<a href="查询云手机列表.md">查询云手机列表</a>获取。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    POST https://{CPH_Endpoint}/v1/{project_id}/cloud-phone/phones/commands{
       "command": "shell",
       "content": "ls -l /system",
       "phone_ids":[
            "1234567b8bab40ffb711234cb80d0234",
            "1678567b8bab40f93711234cb80d0764"
         ]
    }
    ```


## 响应<a name="section13599921948"></a>

-   要素说明

    <a name="table660219211644"></a>
    <table><thead align="left"><tr id="row669162115417"><th class="cellrowborder" valign="top" width="25.509999999999998%" id="mcps1.1.4.1.1"><p id="p169102114412"><a name="p169102114412"></a><a name="p169102114412"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.67%" id="mcps1.1.4.1.2"><p id="p176911921349"><a name="p176911921349"></a><a name="p176911921349"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.82%" id="mcps1.1.4.1.3"><p id="p11691321144"><a name="p11691321144"></a><a name="p11691321144"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1269119215414"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.1.4.1.1 "><p id="p176915211641"><a name="p176915211641"></a><a name="p176915211641"></a>request_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.4.1.2 "><p id="p06917214410"><a name="p06917214410"></a><a name="p06917214410"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.82%" headers="mcps1.1.4.1.3 "><p id="p1569117211141"><a name="p1569117211141"></a><a name="p1569117211141"></a>请求的唯一标识ID。</p>
    </td>
    </tr>
    <tr id="row186912021447"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.1.4.1.1 "><p id="p17691122113419"><a name="p17691122113419"></a><a name="p17691122113419"></a>jobs</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.1.4.1.2 "><p id="p136915210417"><a name="p136915210417"></a><a name="p136915210417"></a>job结构体数组</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.82%" headers="mcps1.1.4.1.3 "><p id="p7691102119418"><a name="p7691102119418"></a><a name="p7691102119418"></a>请参见<a href="#table1131122810124">表1</a>。</p>
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


## 返回值<a name="section12610122117419"></a>

请参考[返回值](返回值.md)。

