# 查询指定API版本信息<a name="zh-cn_topic_0133153747"></a>

## 功能介绍<a name="section11355891"></a>

查询弹性伸缩API指定版本信息。

## URI<a name="section35094160"></a>

GET /\{api\_version\}

**表 1**  参数说明

<a name="table53255854"></a>
<table><thead align="left"><tr id="row14242537"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p12794876"><a name="p12794876"></a><a name="p12794876"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.2.5.1.2"><p id="p29752015"><a name="p29752015"></a><a name="p29752015"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.2.5.1.3"><p id="p61102986"><a name="p61102986"></a><a name="p61102986"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="38%" id="mcps1.2.5.1.4"><p id="p50394838"><a name="p50394838"></a><a name="p50394838"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5926171820323"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p20926201863219"><a name="p20926201863219"></a><a name="p20926201863219"></a>api_version</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.2 "><p id="p5926151873215"><a name="p5926151873215"></a><a name="p5926151873215"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="p992671833216"><a name="p992671833216"></a><a name="p992671833216"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38%" headers="mcps1.2.5.1.4 "><p id="p1392631853211"><a name="p1392631853211"></a><a name="p1392631853211"></a>弹性伸缩API版本号ID</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section47411987"></a>

-   请求参数

    无

-   请求样例

    本示例展示了查询v1版本API的版本信息。

    ```
    GET https://{Endpoint}/v1
    ```


## 响应消息<a name="section24054701"></a>

-   响应参数

    **表 2**  响应参数

    <a name="table59665636"></a>
    <table><thead align="left"><tr id="row28755990"><th class="cellrowborder" valign="top" width="21.782178217821784%" id="mcps1.2.4.1.1"><p id="p47533853"><a name="p47533853"></a><a name="p47533853"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.762376237623762%" id="mcps1.2.4.1.2"><p id="p25036876"><a name="p25036876"></a><a name="p25036876"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="54.45544554455446%" id="mcps1.2.4.1.3"><p id="p14721100"><a name="p14721100"></a><a name="p14721100"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row34736162"><td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.2.4.1.1 "><p id="p1654215818362"><a name="p1654215818362"></a><a name="p1654215818362"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p77023552159"><a name="p77023552159"></a><a name="p77023552159"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.45544554455446%" headers="mcps1.2.4.1.3 "><p id="p48612303"><a name="p48612303"></a><a name="p48612303"></a>描述弹性伸缩API指定版本信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  version字段数据结构说明

    <a name="table786171513527"></a>
    <table><thead align="left"><tr id="row16870715205219"><th class="cellrowborder" valign="top" width="22%" id="mcps1.2.4.1.1"><p id="p787314157521"><a name="p787314157521"></a><a name="p787314157521"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23%" id="mcps1.2.4.1.2"><p id="p15875415185216"><a name="p15875415185216"></a><a name="p15875415185216"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.00000000000001%" id="mcps1.2.4.1.3"><p id="p1487831516528"><a name="p1487831516528"></a><a name="p1487831516528"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1288051545213"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="p198824151526"><a name="p198824151526"></a><a name="p198824151526"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="p4884915105217"><a name="p4884915105217"></a><a name="p4884915105217"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p088519150526"><a name="p088519150526"></a><a name="p088519150526"></a>API版本ID</p>
    </td>
    </tr>
    <tr id="row8887191525212"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="p9888151505213"><a name="p9888151505213"></a><a name="p9888151505213"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="p1489112150526"><a name="p1489112150526"></a><a name="p1489112150526"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1894161514527"><a name="p1894161514527"></a><a name="p1894161514527"></a>API 的url地址，详情请见<a href="#t759e6d15d244474e8f286185ede143fb">表4 links字段数据结构说明</a>。</p>
    </td>
    </tr>
    <tr id="row20895111565214"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="p9107111411399"><a name="p9107111411399"></a><a name="p9107111411399"></a>min_version</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="p58981015115218"><a name="p58981015115218"></a><a name="p58981015115218"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p19907734114018"><a name="p19907734114018"></a><a name="p19907734114018"></a>API支持的最小微版本</p>
    </td>
    </tr>
    <tr id="row9901141525214"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="p3903415185215"><a name="p3903415185215"></a><a name="p3903415185215"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="p390610159525"><a name="p390610159525"></a><a name="p390610159525"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p4907191535213"><a name="p4907191535213"></a><a name="p4907191535213"></a>API版本状态：</p>
    <a name="ul19909615185218"></a><a name="ul19909615185218"></a><ul id="ul19909615185218"><li>CURRENT：表示该版本为主推版本。</li><li>SUPPORTED：表示为老版本，但是现在还在继续支持。</li><li>DEPRECATED：表示为废弃版本，存在后续删除的可能。</li></ul>
    </td>
    </tr>
    <tr id="row149151915105212"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="p4918715155215"><a name="p4918715155215"></a><a name="p4918715155215"></a>updated</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="p892011518520"><a name="p892011518520"></a><a name="p892011518520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1255911034615"><a name="p1255911034615"></a><a name="p1255911034615"></a>API版本发布时间</p>
    </td>
    </tr>
    <tr id="row17923151519525"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="p1892416155523"><a name="p1892416155523"></a><a name="p1892416155523"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="p16926191511523"><a name="p16926191511523"></a><a name="p16926191511523"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p12928215185216"><a name="p12928215185216"></a><a name="p12928215185216"></a>API支持的最大微版本号</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 4**  links字段数据结构说明

    <a name="t759e6d15d244474e8f286185ede143fb"></a>
    <table><thead align="left"><tr id="rce98b9668cd747c88039421afe5ce935"><th class="cellrowborder" valign="top" width="22%" id="mcps1.2.4.1.1"><p id="ad9ac3007570a4752b2b2dbc0fb04dadc"><a name="ad9ac3007570a4752b2b2dbc0fb04dadc"></a><a name="ad9ac3007570a4752b2b2dbc0fb04dadc"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23%" id="mcps1.2.4.1.2"><p id="a602246198adf4a79a13bc4317d4c0d4f"><a name="a602246198adf4a79a13bc4317d4c0d4f"></a><a name="a602246198adf4a79a13bc4317d4c0d4f"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.00000000000001%" id="mcps1.2.4.1.3"><p id="a8cbfa8dcb0b943ff8e789755123fec83"><a name="a8cbfa8dcb0b943ff8e789755123fec83"></a><a name="a8cbfa8dcb0b943ff8e789755123fec83"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r43de461181294c56b28da56a1f604b09"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="abc19a41a8f594f1ba6701e10da50a078"><a name="abc19a41a8f594f1ba6701e10da50a078"></a><a name="abc19a41a8f594f1ba6701e10da50a078"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="a15ae7b8585d24e48abc6b9bf45636fda"><a name="a15ae7b8585d24e48abc6b9bf45636fda"></a><a name="a15ae7b8585d24e48abc6b9bf45636fda"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p139393206480"><a name="p139393206480"></a><a name="p139393206480"></a>API的url地址</p>
    </td>
    </tr>
    <tr id="rbd5ec7242fef4c03b21636ac14160d9e"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="a18479f6b70b34f29b2b90d754f59282a"><a name="a18479f6b70b34f29b2b90d754f59282a"></a><a name="a18479f6b70b34f29b2b90d754f59282a"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="ae1f14fa2e6a54531aeffd26874fea267"><a name="ae1f14fa2e6a54531aeffd26874fea267"></a><a name="ae1f14fa2e6a54531aeffd26874fea267"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p115877381483"><a name="p115877381483"></a><a name="p115877381483"></a>API的url地址依赖</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
      "version": {
        "id": "v1",
        "links": [
          {
            "href": "https://as.XXX.mycloud.com/autoscaling-api/v1/",
            "rel": "self"
          }
        ],
        "min_version": "",
        "status": "CURRENT",
        "updated": "2016-06-30T00:00:00Z",
        "version": ""
      }
    }
    ```


## 返回值<a name="section15165719"></a>

-   正常

    200

-   异常

    <a name="table5908907"></a>
    <table><thead align="left"><tr id="row16065622"><th class="cellrowborder" valign="top" width="41%" id="mcps1.1.3.1.1"><p id="p26246992"><a name="p26246992"></a><a name="p26246992"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="59%" id="mcps1.1.3.1.2"><p id="p45631627"><a name="p45631627"></a><a name="p45631627"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5174319"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p16466658"><a name="p16466658"></a><a name="p16466658"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p58730959"><a name="p58730959"></a><a name="p58730959"></a>服务器未能处理请求。</p>
    </td>
    </tr>
    <tr id="row58816586"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p66523006"><a name="p66523006"></a><a name="p66523006"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p19654399"><a name="p19654399"></a><a name="p19654399"></a>被请求的页面需要用户名和密码。</p>
    </td>
    </tr>
    <tr id="row42671863"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p33868885"><a name="p33868885"></a><a name="p33868885"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p59025204"><a name="p59025204"></a><a name="p59025204"></a>对被请求的页面访问禁止。</p>
    </td>
    </tr>
    <tr id="row61464796"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p12592542"><a name="p12592542"></a><a name="p12592542"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p13362997"><a name="p13362997"></a><a name="p13362997"></a>服务器无法找到被请求的页面。</p>
    </td>
    </tr>
    <tr id="row53158116"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p10840149"><a name="p10840149"></a><a name="p10840149"></a>405 Method Not Allowed</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p5636878"><a name="p5636878"></a><a name="p5636878"></a>请求中指定的方法不被允许。</p>
    </td>
    </tr>
    <tr id="row50731910"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p15644031"><a name="p15644031"></a><a name="p15644031"></a>406 Not Acceptable</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p59206997"><a name="p59206997"></a><a name="p59206997"></a>服务器生成的响应无法被客户端所接受。</p>
    </td>
    </tr>
    <tr id="row63100926"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p10901353"><a name="p10901353"></a><a name="p10901353"></a>407 Proxy Authentication Required</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p10594405"><a name="p10594405"></a><a name="p10594405"></a>用户必须首先使用代理服务器进行验证，这样请求才会被处理。</p>
    </td>
    </tr>
    <tr id="row28240785"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p5802216"><a name="p5802216"></a><a name="p5802216"></a>408 Request Timeout</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p217508"><a name="p217508"></a><a name="p217508"></a>请求超出了服务器的等待时间。</p>
    </td>
    </tr>
    <tr id="row1957580"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p24346266"><a name="p24346266"></a><a name="p24346266"></a>409 Conflict</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p25890496"><a name="p25890496"></a><a name="p25890496"></a>由于冲突，请求无法被完成。</p>
    </td>
    </tr>
    <tr id="row31687876"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p16581154"><a name="p16581154"></a><a name="p16581154"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p896237"><a name="p896237"></a><a name="p896237"></a>请求未完成。服务异常。</p>
    </td>
    </tr>
    <tr id="row8066134"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p49377135"><a name="p49377135"></a><a name="p49377135"></a>501 Not Implemented</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p40124968"><a name="p40124968"></a><a name="p40124968"></a>请求未完成。服务器不支持所请求的功能。</p>
    </td>
    </tr>
    <tr id="row25580392"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p58745844"><a name="p58745844"></a><a name="p58745844"></a>502 Bad Gateway</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p60792949"><a name="p60792949"></a><a name="p60792949"></a>请求未完成。服务器从上游服务器收到一个无效的响应。</p>
    </td>
    </tr>
    <tr id="row10265637"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p26210288"><a name="p26210288"></a><a name="p26210288"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p42658596"><a name="p42658596"></a><a name="p42658596"></a>请求未完成。系统暂时异常。</p>
    </td>
    </tr>
    <tr id="row48383044"><td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.3.1.1 "><p id="p26712487"><a name="p26712487"></a><a name="p26712487"></a>504 Gateway Timeout</p>
    </td>
    <td class="cellrowborder" valign="top" width="59%" headers="mcps1.1.3.1.2 "><p id="p16227847"><a name="p16227847"></a><a name="p16227847"></a>网关超时。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 错误码<a name="section17669131616110"></a>

请参考[错误码](错误码.md)。

