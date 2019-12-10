# 创建弹性伸缩组<a name="zh-cn_topic_0043063023"></a>

## 功能介绍<a name="section21784493"></a>

伸缩组是具有相同应用场景的实例的集合，是启停伸缩策略和进行伸缩活动的基本单位。伸缩组内定义了最大实例数、期望实例数、最小实例数、虚拟私有云、子网、负载均衡等信息。

-   默认最多可以创建10个伸缩组。
-   如果伸缩组配置了负载均衡，在添加或移除实例时，会自动为实例绑定或解绑负载均衡监听器。
-   如果伸缩组使用负载均衡健康检查方式，伸缩组中的实例需要启用负载均衡器的监听端口才能通过健康检查。端口启用可在安全组中进行配置，可参考[添加安全组规则](https://support.huaweicloud.com/usermanual-vpc/zh-cn_topic_0030969470.html)进行操作。

## URI<a name="section61842715"></a>

POST /autoscaling-api/v1/\{project\_id\}/scaling\_group

**表 1**  参数说明

<a name="table4718148"></a>
<table><thead align="left"><tr id="row62417507"><th class="cellrowborder" valign="top" width="23%" id="mcps1.2.5.1.1"><p id="p22653281"><a name="p22653281"></a><a name="p22653281"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27%" id="mcps1.2.5.1.2"><p id="p22976439"><a name="p22976439"></a><a name="p22976439"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p49152270"><a name="p49152270"></a><a name="p49152270"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p21910925"><a name="p21910925"></a><a name="p21910925"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row29954525"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.1 "><p id="p1221320251318"><a name="p1221320251318"></a><a name="p1221320251318"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.5.1.2 "><p id="p36889359"><a name="p36889359"></a><a name="p36889359"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p35248064"><a name="p35248064"></a><a name="p35248064"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p36520930"><a name="p36520930"></a><a name="p36520930"></a>项目ID</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section19713524"></a>

-   请求参数

    **表 2**  请求参数

    <a name="table147283118511"></a>
    <table><thead align="left"><tr id="row1971971119513"><th class="cellrowborder" valign="top" width="22.3%" id="mcps1.2.5.1.1"><p id="p271981175113"><a name="p271981175113"></a><a name="p271981175113"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.04%" id="mcps1.2.5.1.2"><p id="p3719161114518"><a name="p3719161114518"></a><a name="p3719161114518"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.5.1.3"><p id="p1971971112515"><a name="p1971971112515"></a><a name="p1971971112515"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.54%" id="mcps1.2.5.1.4"><p id="p7719141125110"><a name="p7719141125110"></a><a name="p7719141125110"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row572015117517"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p1871951175116"><a name="p1871951175116"></a><a name="p1871951175116"></a>scaling_group_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p15719411165112"><a name="p15719411165112"></a><a name="p15719411165112"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p1572019119513"><a name="p1572019119513"></a><a name="p1572019119513"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p177201011155120"><a name="p177201011155120"></a><a name="p177201011155120"></a>伸缩组名称(1-64个字符)，只能包含中文、字母、数字、下划线或中划线。</p>
    </td>
    </tr>
    <tr id="row13720101125119"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p4720161114511"><a name="p4720161114511"></a><a name="p4720161114511"></a>scaling_configuration_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p10720181195114"><a name="p10720181195114"></a><a name="p10720181195114"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p1172081115118"><a name="p1172081115118"></a><a name="p1172081115118"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p1872071118516"><a name="p1872071118516"></a><a name="p1872071118516"></a>伸缩配置ID，通过查询弹性伸缩配置列表接口获取，请参考<a href="查询弹性伸缩配置列表.md">查询弹性伸缩配置列表</a>。</p>
    </td>
    </tr>
    <tr id="row157209117514"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p1372051114519"><a name="p1372051114519"></a><a name="p1372051114519"></a>desire_instance_number</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p17201711195118"><a name="p17201711195118"></a><a name="p17201711195118"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p872061115113"><a name="p872061115113"></a><a name="p872061115113"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p1720191110516"><a name="p1720191110516"></a><a name="p1720191110516"></a>期望实例数量，默认值为最小实例数。</p>
    <p id="p18720611165111"><a name="p18720611165111"></a><a name="p18720611165111"></a>最小实例数≤期望实例数≤最大实例数。</p>
    </td>
    </tr>
    <tr id="row12721161115115"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p1172012115510"><a name="p1172012115510"></a><a name="p1172012115510"></a>min_instance_number</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p1720311195118"><a name="p1720311195118"></a><a name="p1720311195118"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p117201111185113"><a name="p117201111185113"></a><a name="p117201111185113"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p107217119510"><a name="p107217119510"></a><a name="p107217119510"></a>最小实例数量，默认值为0。</p>
    </td>
    </tr>
    <tr id="row1572131135116"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p072118112512"><a name="p072118112512"></a><a name="p072118112512"></a>max_instance_number</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p97211311115113"><a name="p97211311115113"></a><a name="p97211311115113"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p147211911185114"><a name="p147211911185114"></a><a name="p147211911185114"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p372116118513"><a name="p372116118513"></a><a name="p372116118513"></a>最大实例数量，默认值为0。</p>
    </td>
    </tr>
    <tr id="row18721101135112"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p672111110515"><a name="p672111110515"></a><a name="p672111110515"></a>cool_down_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p167211411195114"><a name="p167211411195114"></a><a name="p167211411195114"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p47211011205118"><a name="p47211011205118"></a><a name="p47211011205118"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p14721131145111"><a name="p14721131145111"></a><a name="p14721131145111"></a>冷却时间，取值范围0-86400，默认为300，单位是秒。</p>
    <p id="p8060118"><a name="p8060118"></a><a name="p8060118"></a>在每次伸缩活动完成之后，系统开始计算冷却时间。伸缩组在冷却时间内，会拒绝由告警策略触发的伸缩活动，其他类型的伸缩策略（如定时策略和周期策略）及手动触发的伸缩活动不受限制。</p>
    </td>
    </tr>
    <tr id="row672221111511"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p14721811105111"><a name="p14721811105111"></a><a name="p14721811105111"></a>lb_listener_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p37213119510"><a name="p37213119510"></a><a name="p37213119510"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p3721611125116"><a name="p3721611125116"></a><a name="p3721611125116"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p20895122411511"><a name="p20895122411511"></a><a name="p20895122411511"></a>弹性负载均衡（经典型）监听器ID，最多支持绑定6个负载均衡监听器，多个负载均衡监听器ID以逗号分隔。获取监听器ID的方法请参考<a href="https://support.huaweicloud.com/api-elb/zh-cn_topic_0096561504.html" target="_blank" rel="noopener noreferrer">查询负载均衡器列表</a>。</p>
    <p id="p1560095562314"><a name="p1560095562314"></a><a name="p1560095562314"></a>该字段与lbaas_listeners互斥。</p>
    </td>
    </tr>
    <tr id="row1872231185115"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p197228111512"><a name="p197228111512"></a><a name="p197228111512"></a>lbaas_listeners</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p19722611145120"><a name="p19722611145120"></a><a name="p19722611145120"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p1393644073714"><a name="p1393644073714"></a><a name="p1393644073714"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p172210118517"><a name="p172210118517"></a><a name="p172210118517"></a>弹性负载均衡器（增强型）信息，最多支持绑定6个负载均衡。列表数据结构请参考<a href="#table154023755417">表3</a>。获取增强型负载均衡器的信息请参考<a href="https://support.huaweicloud.com/api-elb/zh-cn_topic_0096561547.html" target="_blank" rel="noopener noreferrer">查询后端云服务器组</a>。</p>
    <p id="p1772211115117"><a name="p1772211115117"></a><a name="p1772211115117"></a>该字段与lb_listener_id互斥。</p>
    </td>
    </tr>
    <tr id="row16722211115118"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p57221411125116"><a name="p57221411125116"></a><a name="p57221411125116"></a>available_zones</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p67221511135117"><a name="p67221511135117"></a><a name="p67221511135117"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p117221011175115"><a name="p117221011175115"></a><a name="p117221011175115"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p3722181114516"><a name="p3722181114516"></a><a name="p3722181114516"></a>可用区信息。弹性伸缩活动中自动添加的云服务器会被创建在指定的可用区中。如果没有指定可用区，会由系统自动指定可用区。详情请参考<a href="https://developer.huaweicloud.com/endpoint" target="_blank" rel="noopener noreferrer">地区和终端节点</a>。</p>
    </td>
    </tr>
    <tr id="row972281135114"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p87221811195114"><a name="p87221811195114"></a><a name="p87221811195114"></a>networks</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p1446924373712"><a name="p1446924373712"></a><a name="p1446924373712"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p347824310372"><a name="p347824310372"></a><a name="p347824310372"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p87221511205113"><a name="p87221511205113"></a><a name="p87221511205113"></a>网络信息，最多支持选择5个子网，传入的第一个子网默认作为云服务器的主网卡。获取子网信息请参考<a href="https://support.huaweicloud.com/api-vpc/zh-cn_topic_0020090592.html" target="_blank" rel="noopener noreferrer">查询子网列表</a>。数据结构信息请参考<a href="#table16283330203725">表4</a>。</p>
    </td>
    </tr>
    <tr id="row972231195110"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p272271125110"><a name="p272271125110"></a><a name="p272271125110"></a>security_groups</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p872212119515"><a name="p872212119515"></a><a name="p872212119515"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p5722151135117"><a name="p5722151135117"></a><a name="p5722151135117"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p1272251135116"><a name="p1272251135116"></a><a name="p1272251135116"></a>安全组信息，仅支持选择1个安全组。获取安全组信息请参考<a href="https://support.huaweicloud.com/api-vpc/zh-cn_topic_0020090617.html" target="_blank" rel="noopener noreferrer">查询安全组列表</a>。数据结构信息请参考<a href="#table25481545203427">表6</a>。</p>
    <p id="p17221511155111"><a name="p17221511155111"></a><a name="p17221511155111"></a>当伸缩配置和伸缩组同时指定安全组时，将以伸缩配置中的安全组为准；当伸缩配置和伸缩组都没有指定安全组时，将使用默认安全组。为了使用灵活性更高，推荐在伸缩配置中指定安全组。</p>
    </td>
    </tr>
    <tr id="row77231111185119"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p177221911175110"><a name="p177221911175110"></a><a name="p177221911175110"></a>vpc_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p2722511175113"><a name="p2722511175113"></a><a name="p2722511175113"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p157231611125114"><a name="p157231611125114"></a><a name="p157231611125114"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p1723811115118"><a name="p1723811115118"></a><a name="p1723811115118"></a>虚拟私有云（VPC）信息，获取VPC信息具体操作请参考<a href="https://support.huaweicloud.com/api-vpc/zh-cn_topic_0020090625.html" target="_blank" rel="noopener noreferrer">查询VPC列表</a>。</p>
    </td>
    </tr>
    <tr id="row15723111165117"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p772361185111"><a name="p772361185111"></a><a name="p772361185111"></a>health_periodic_audit_method</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p7723181111516"><a name="p7723181111516"></a><a name="p7723181111516"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p472391175111"><a name="p472391175111"></a><a name="p472391175111"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p672313117518"><a name="p672313117518"></a><a name="p672313117518"></a>伸缩组实例健康检查方式：ELB_AUDIT和NOVA_AUDIT。当伸缩组设置负载均衡时，默认为ELB_AUDIT；否则默认为NOVA_AUDIT。</p>
    <a name="ul27231211175112"></a><a name="ul27231211175112"></a><ul id="ul27231211175112"><li>ELB_AUDIT：负载均衡健康检查方式，在有监听器的伸缩组中有效。</li><li><span>NOVA_AUDIT：云服务器健康检查方式，是弹性伸缩自带的健康检查方式。</span></li></ul>
    </td>
    </tr>
    <tr id="row5724311175118"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p1072314114512"><a name="p1072314114512"></a><a name="p1072314114512"></a>health_periodic_audit_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p13724171120513"><a name="p13724171120513"></a><a name="p13724171120513"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p14724111135119"><a name="p14724111135119"></a><a name="p14724111135119"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p187241111205115"><a name="p187241111205115"></a><a name="p187241111205115"></a>伸缩组实例的健康检查周期，可设置为1、5、15、60、180（分钟），若不设置该参数，默认为5。</p>
    <p id="p157241911135110"><a name="p157241911135110"></a><a name="p157241911135110"></a>若设置为0，可以实现10秒级健康检查。</p>
    </td>
    </tr>
    <tr id="row13726191118514"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p19724611205116"><a name="p19724611205116"></a><a name="p19724611205116"></a>health_periodic_audit_grace_period</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p8724181105110"><a name="p8724181105110"></a><a name="p8724181105110"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p17241711185115"><a name="p17241711185115"></a><a name="p17241711185115"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p20726151117518"><a name="p20726151117518"></a><a name="p20726151117518"></a>伸缩组实例健康状况检查宽限期，取值范围0-86400，单位是秒，默认为600。</p>
    <p id="p4726511155112"><a name="p4726511155112"></a><a name="p4726511155112"></a>当实例加入伸缩组并且进入已启用状态后，健康状况检查宽限期才会启动，伸缩组会等健康状况检查宽限期结束后才检查实例的运行状况。</p>
    <p id="p9726131185116"><a name="p9726131185116"></a><a name="p9726131185116"></a>当伸缩组实例健康检查方式为ELB_AUDIT时，该参数生效。</p>
    </td>
    </tr>
    <tr id="row3726411195112"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p10726161195118"><a name="p10726161195118"></a><a name="p10726161195118"></a>instance_terminate_policy</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p7726111175114"><a name="p7726111175114"></a><a name="p7726111175114"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p672601119519"><a name="p672601119519"></a><a name="p672601119519"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p1472612119514"><a name="p1472612119514"></a><a name="p1472612119514"></a>伸缩组实例移除策略：</p>
    <a name="ul137261112513"></a><a name="ul137261112513"></a><ul id="ul137261112513"><li>OLD_CONFIG_OLD_INSTANCE（默认）：从“较早创建的配置”创建的实例中选择较早创建的实例进行优先移除。</li><li>OLD_CONFIG_NEW_INSTANCE：从“较早创建的配置”创建的实例中选择较晚创建的实例进行优先移除。</li><li>OLD_INSTANCE：较早创建的实例被优先移除。</li><li>NEW_INSTANCE：较晚创建的实例将被优先移除。</li></ul>
    </td>
    </tr>
    <tr id="row19727511155112"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p11726101115511"><a name="p11726101115511"></a><a name="p11726101115511"></a>notifications</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p8726181165110"><a name="p8726181165110"></a><a name="p8726181165110"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p147271311155118"><a name="p147271311155118"></a><a name="p147271311155118"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p3727181125117"><a name="p3727181125117"></a><a name="p3727181125117"></a>通知方式：</p>
    <p id="p7727611125118"><a name="p7727611125118"></a><a name="p7727611125118"></a>EMAIL为发送邮件通知。</p>
    <p id="p1772701119510"><a name="p1772701119510"></a><a name="p1772701119510"></a>该通知方式已经被废除，建议给弹性伸缩组配置通知功能。请参考<a href="通知.md">通知</a>。</p>
    </td>
    </tr>
    <tr id="row272741165118"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p167274119512"><a name="p167274119512"></a><a name="p167274119512"></a>delete_publicip</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p5727131117518"><a name="p5727131117518"></a><a name="p5727131117518"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p5727111119516"><a name="p5727111119516"></a><a name="p5727111119516"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><div class="p" id="p1063119062315"><a name="p1063119062315"></a><a name="p1063119062315"></a>配置删除云服务器时是否删除云服务器绑定的弹性IP。取值为true或false，默认为false。<a name="ul4934185211225"></a><a name="ul4934185211225"></a><ul id="ul4934185211225"><li>true：删除云服务器时，会同时删除绑定在云服务器上的弹性IP。当弹性IP的计费方式为包年包月时，不会被删除。</li><li>false：删除云服务器时，仅解绑定在云服务器上的弹性IP，不删除弹性IP。</li></ul>
    </div>
    </td>
    </tr>
    <tr id="row1920147191919"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p2120131361912"><a name="p2120131361912"></a><a name="p2120131361912"></a>delete_volume</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p312016138190"><a name="p312016138190"></a><a name="p312016138190"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p4120111317191"><a name="p4120111317191"></a><a name="p4120111317191"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><div class="p" id="p108891816236"><a name="p108891816236"></a><a name="p108891816236"></a>配置删除云服务器时是否删除云服务器绑定的数据盘。取值为true或false，默认为false。<a name="ul0854204462211"></a><a name="ul0854204462211"></a><ul id="ul0854204462211"><li>true：删除云服务器时，会同时删除绑定在云服务器上的数据盘。当数据盘的计费方式为包年包月时，不会被删除。</li><li>false：删除云服务器时，仅解绑定在云服务器上的数据盘，不删除数据盘。</li></ul>
    </div>
    </td>
    </tr>
    <tr id="row18728211195118"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p13727171115114"><a name="p13727171115114"></a><a name="p13727171115114"></a>enterprise_project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p8727121120518"><a name="p8727121120518"></a><a name="p8727121120518"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p10727111195110"><a name="p10727111195110"></a><a name="p10727111195110"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p117281711175115"><a name="p117281711175115"></a><a name="p117281711175115"></a>企业项目ID，用于指定伸缩组归属的企业项目。</p>
    <a name="ul381025535013"></a><a name="ul381025535013"></a><ul id="ul381025535013"><li>取值为0或无该值，表示属于default企业项目。</li><li>取值为UUID，表示属于该UUID对应的企业项目，如何获取企业项目ID，请参考<a href="https://support.huaweicloud.com/api-em/zh-cn_topic_0121230880.html" target="_blank" rel="noopener noreferrer">查询企业项目列表</a>。</li></ul>
    <p id="p87281211175111"><a name="p87281211175111"></a><a name="p87281211175111"></a>当伸缩组配置企业项目时，由该伸缩组创建的弹性云服务器将归属于该企业项目。否则将使用默认企业项目。</p>
    <div class="note" id="note272851195111"><a name="note272851195111"></a><a name="note272851195111"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p77281811125110"><a name="p77281811125110"></a><a name="p77281811125110"></a>关于企业项目特性的详细信息，请参见<a href="https://support.huaweicloud.com/usermanual-em/zh-cn_topic_0131965280.html" target="_blank" rel="noopener noreferrer">企业项目管理</a>。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row54865725419"><td class="cellrowborder" valign="top" width="22.3%" headers="mcps1.2.5.1.1 "><p id="p249115717542"><a name="p249115717542"></a><a name="p249115717542"></a>multi_az_priority_policy</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.04%" headers="mcps1.2.5.1.2 "><p id="p13511912195520"><a name="p13511912195520"></a><a name="p13511912195520"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.3 "><p id="p1551121275510"><a name="p1551121275510"></a><a name="p1551121275510"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.54%" headers="mcps1.2.5.1.4 "><p id="p25111112195515"><a name="p25111112195515"></a><a name="p25111112195515"></a>伸缩组扩缩容时目标AZ选择的优先级策略：</p>
    <a name="ul0511201275510"></a><a name="ul0511201275510"></a><ul id="ul0511201275510"><li>EQUILIBRIUM_DISTRIBUTE（默认）：均衡分布，云服务器扩缩容时优先保证available_zones列表中各AZ下虚拟机数量均衡，当无法在目标AZ下完成虚拟机扩容时，按照PICK_FIRST原则选择其他可用AZ。</li><li>PICK_FIRST：选择优先，虚拟机扩缩容时目标AZ的选择按照available_zones列表的顺序进行优先级排序。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  lbaas\_listeners字段数据结构说明

    <a name="table154023755417"></a>
    <table><thead align="left"><tr id="row174011876548"><th class="cellrowborder" valign="top" width="23%" id="mcps1.2.5.1.1"><p id="p164014710549"><a name="p164014710549"></a><a name="p164014710549"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12%" id="mcps1.2.5.1.2"><p id="p7401577544"><a name="p7401577544"></a><a name="p7401577544"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12%" id="mcps1.2.5.1.3"><p id="p104016716548"><a name="p104016716548"></a><a name="p104016716548"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="53%" id="mcps1.2.5.1.4"><p id="p174015735419"><a name="p174015735419"></a><a name="p174015735419"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row164021277541"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.1 "><p id="p34019719547"><a name="p34019719547"></a><a name="p34019719547"></a>pool_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.2 "><p id="p8401167115418"><a name="p8401167115418"></a><a name="p8401167115418"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p18402107195416"><a name="p18402107195416"></a><a name="p18402107195416"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.5.1.4 "><p id="p64020713547"><a name="p64020713547"></a><a name="p64020713547"></a>后端云服务器组ID</p>
    </td>
    </tr>
    <tr id="row1340215715415"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.1 "><p id="p19402777542"><a name="p19402777542"></a><a name="p19402777542"></a>protocol_port</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.2 "><p id="p740297195419"><a name="p740297195419"></a><a name="p740297195419"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p04022078549"><a name="p04022078549"></a><a name="p04022078549"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.5.1.4 "><p id="p114021472547"><a name="p114021472547"></a><a name="p114021472547"></a>后端协议号，指后端云服务器监听的端口，取值范围[1, 65535]。</p>
    </td>
    </tr>
    <tr id="row124029745419"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.1 "><p id="p14023716543"><a name="p14023716543"></a><a name="p14023716543"></a>weight</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.2 "><p id="p134021778545"><a name="p134021778545"></a><a name="p134021778545"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p1940213711546"><a name="p1940213711546"></a><a name="p1940213711546"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.5.1.4 "><p id="p34021974545"><a name="p34021974545"></a><a name="p34021974545"></a>权重，指后端云服务器经分发得到的请求数量的比例，取值范围[0, 100]，默认为1。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 4**  networks字段数据结构说明

    <a name="table16283330203725"></a>
    <table><thead align="left"><tr id="r9061055fab7042ad84743683a2b5b98d"><th class="cellrowborder" valign="top" width="22.5%" id="mcps1.2.5.1.1"><p id="a679fce5df7a14f22afdcfabeadfa041d"><a name="a679fce5df7a14f22afdcfabeadfa041d"></a><a name="a679fce5df7a14f22afdcfabeadfa041d"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.879999999999999%" id="mcps1.2.5.1.2"><p id="p41814948203944"><a name="p41814948203944"></a><a name="p41814948203944"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.139999999999999%" id="mcps1.2.5.1.3"><p id="a2c0586869bf949e6af882694148874ed"><a name="a2c0586869bf949e6af882694148874ed"></a><a name="a2c0586869bf949e6af882694148874ed"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.480000000000004%" id="mcps1.2.5.1.4"><p id="a4774d878ba474479ad17a6d04d9c0b6e"><a name="a4774d878ba474479ad17a6d04d9c0b6e"></a><a name="a4774d878ba474479ad17a6d04d9c0b6e"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r801df159f0ca4d40b2c4abcd91800eee"><td class="cellrowborder" valign="top" width="22.5%" headers="mcps1.2.5.1.1 "><p id="af56439ac85cc4740ac47a13abbb60fba"><a name="af56439ac85cc4740ac47a13abbb60fba"></a><a name="af56439ac85cc4740ac47a13abbb60fba"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.879999999999999%" headers="mcps1.2.5.1.2 "><p id="p31567631203944"><a name="p31567631203944"></a><a name="p31567631203944"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.139999999999999%" headers="mcps1.2.5.1.3 "><p id="ad129d99902cf4f55a062dafa6c161407"><a name="ad129d99902cf4f55a062dafa6c161407"></a><a name="ad129d99902cf4f55a062dafa6c161407"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.480000000000004%" headers="mcps1.2.5.1.4 "><p id="aba9652e07bf34af0a26c153ea5d73d9d"><a name="aba9652e07bf34af0a26c153ea5d73d9d"></a><a name="aba9652e07bf34af0a26c153ea5d73d9d"></a>网络ID</p>
    </td>
    </tr>
    <tr id="row1684516191189"><td class="cellrowborder" valign="top" width="22.5%" headers="mcps1.2.5.1.1 "><p id="p168461419171814"><a name="p168461419171814"></a><a name="p168461419171814"></a>ipv6_enable</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.879999999999999%" headers="mcps1.2.5.1.2 "><p id="p8846141981812"><a name="p8846141981812"></a><a name="p8846141981812"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.139999999999999%" headers="mcps1.2.5.1.3 "><p id="p128463194182"><a name="p128463194182"></a><a name="p128463194182"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.480000000000004%" headers="mcps1.2.5.1.4 "><p id="p204521031173520"><a name="p204521031173520"></a><a name="p204521031173520"></a>是否启用IPv6。</p>
    <p id="p517418420358"><a name="p517418420358"></a><a name="p517418420358"></a>true：标识此网卡已启用ipv6。</p>
    <p id="p1869495520194"><a name="p1869495520194"></a><a name="p1869495520194"></a>false：标识此网卡未启用ipv6。默认取值为false。</p>
    </td>
    </tr>
    <tr id="row4543172218186"><td class="cellrowborder" valign="top" width="22.5%" headers="mcps1.2.5.1.1 "><p id="p205431522101813"><a name="p205431522101813"></a><a name="p205431522101813"></a>ipv6_bandwidth</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.879999999999999%" headers="mcps1.2.5.1.2 "><p id="p14543172281814"><a name="p14543172281814"></a><a name="p14543172281814"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.139999999999999%" headers="mcps1.2.5.1.3 "><p id="p19543152215187"><a name="p19543152215187"></a><a name="p19543152215187"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.480000000000004%" headers="mcps1.2.5.1.4 "><p id="p18543162219184"><a name="p18543162219184"></a><a name="p18543162219184"></a>绑定的IPv6共享带宽。默认为空，表示未绑定IPv6的共享带宽。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 5**  ipv6\_bandwidth字段数据结构说明

    <a name="table389911412219"></a>
    <table><thead align="left"><tr id="row20900154152115"><th class="cellrowborder" valign="top" width="23.28%" id="mcps1.2.5.1.1"><p id="p18442811162111"><a name="p18442811162111"></a><a name="p18442811162111"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.75%" id="mcps1.2.5.1.2"><p id="p7445191111217"><a name="p7445191111217"></a><a name="p7445191111217"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.01%" id="mcps1.2.5.1.3"><p id="p444917113212"><a name="p444917113212"></a><a name="p444917113212"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.959999999999994%" id="mcps1.2.5.1.4"><p id="p164521211182118"><a name="p164521211182118"></a><a name="p164521211182118"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5901164192114"><td class="cellrowborder" valign="top" width="23.28%" headers="mcps1.2.5.1.1 "><p id="p109011143210"><a name="p109011143210"></a><a name="p109011143210"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.75%" headers="mcps1.2.5.1.2 "><p id="p59010416217"><a name="p59010416217"></a><a name="p59010416217"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.01%" headers="mcps1.2.5.1.3 "><p id="p17901164192117"><a name="p17901164192117"></a><a name="p17901164192117"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.959999999999994%" headers="mcps1.2.5.1.4 "><p id="p18389161592217"><a name="p18389161592217"></a><a name="p18389161592217"></a>IPv6共享带宽的ID</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 6**  security\_groups字段数据结构说明

    <a name="table25481545203427"></a>
    <table><thead align="left"><tr id="r0cd4feaf0dd34dbea5d88f1e2b5e52de"><th class="cellrowborder" valign="top" width="23%" id="mcps1.2.5.1.1"><p id="adb89aff830c241f1a8ba24a05025ec7d"><a name="adb89aff830c241f1a8ba24a05025ec7d"></a><a name="adb89aff830c241f1a8ba24a05025ec7d"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="13%" id="mcps1.2.5.1.2"><p id="p62623656203950"><a name="p62623656203950"></a><a name="p62623656203950"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="13%" id="mcps1.2.5.1.3"><p id="a5a70f90bbb614578b2e69d51730603b8"><a name="a5a70f90bbb614578b2e69d51730603b8"></a><a name="a5a70f90bbb614578b2e69d51730603b8"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51%" id="mcps1.2.5.1.4"><p id="a984b04e2931047e2ab76977321772cc5"><a name="a984b04e2931047e2ab76977321772cc5"></a><a name="a984b04e2931047e2ab76977321772cc5"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rd4f0b565f1b44c55a666b8609ebaf71a"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.1 "><p id="a333dfdd572ba4d87b073ffdf4f5fa7c3"><a name="a333dfdd572ba4d87b073ffdf4f5fa7c3"></a><a name="a333dfdd572ba4d87b073ffdf4f5fa7c3"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.5.1.2 "><p id="p39351407203950"><a name="p39351407203950"></a><a name="p39351407203950"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.5.1.3 "><p id="a59b78bb0a82c4f1c897a4180831bc790"><a name="a59b78bb0a82c4f1c897a4180831bc790"></a><a name="a59b78bb0a82c4f1c897a4180831bc790"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.5.1.4 "><p id="a36b8ec84f3b34629ae6133fec28f88fd"><a name="a36b8ec84f3b34629ae6133fec28f88fd"></a><a name="a36b8ec84f3b34629ae6133fec28f88fd"></a>安全组ID</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    示例为创建一个满足下述要求的伸缩组：

    -   伸缩组名称为GroupNameTest。
    -   伸缩配置ID为47683a91-93ee-462a-a7d7-484c006f4440。
    -   虚拟私有云ID为a8327883-6b07-4497-9c61-68d03ee193a，网络ID为3cd35bca-5a10-416f-8994-f79169559870。
    -   最大实例数为10，期望实例数为0，最小实例数为0。
    -   健康检查方式为云服务器健康检查。
    -   设置具体企业项目。
    -   伸缩组扩缩容时目标AZ选择的优先级策略为PICK\_FIRST（选择优先）。

    请求样例可参考如下：

    ```
    POST https://{Endpoint}/autoscaling-api/v1/{project_id}/scaling_group
    
    {
        "scaling_group_name": "GroupNameTest",
        "scaling_configuration_id": "47683a91-93ee-462a-a7d7-484c006f4440",
        "desire_instance_number": 0,
        "min_instance_number": 0,
        "max_instance_number": 10,
        "health_periodic_audit_method": "NOVA_AUDIT",
        "vpc_id": "a8327883-6b07-4497-9c61-68d03ee193a",
        "available_zones": ["XXXa","XXXb"],
        "networks": [
            {
                "id": "3cd35bca-5a10-416f-8994-f79169559870"
            }
        ],
        "enterprise_project_id": "c92b1a5d-6f20-43f2-b1b7-7ce35e58e413",
        "multi_az_priority_policy": "PICK_FIRST"
    }
    ```


## 响应消息<a name="section53291640"></a>

-   响应参数

    **表 7**  响应参数

    <a name="table187606212210"></a>
    <table><thead align="left"><tr id="row07608232110"><th class="cellrowborder" valign="top" width="21.94%" id="mcps1.2.4.1.1"><p id="p107601628217"><a name="p107601628217"></a><a name="p107601628217"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.06%" id="mcps1.2.4.1.2"><p id="p15760102102117"><a name="p15760102102117"></a><a name="p15760102102117"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52%" id="mcps1.2.4.1.3"><p id="p1976062152119"><a name="p1976062152119"></a><a name="p1976062152119"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row076013214211"><td class="cellrowborder" valign="top" width="21.94%" headers="mcps1.2.4.1.1 "><p id="p107601025216"><a name="p107601025216"></a><a name="p107601025216"></a>scaling_group_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.06%" headers="mcps1.2.4.1.2 "><p id="p11760192132118"><a name="p11760192132118"></a><a name="p11760192132118"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52%" headers="mcps1.2.4.1.3 "><p id="p276032192116"><a name="p276032192116"></a><a name="p276032192116"></a>伸缩组ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "scaling_group_id": "a8327883-6b07-4497-9c61-68d03ee193a1"
    }
    ```


## 返回值<a name="section9862716"></a>

-   正常

    200

-   异常

    <a name="table50474807"></a>
    <table><thead align="left"><tr id="row48020839"><th class="cellrowborder" valign="top" width="42.67%" id="mcps1.1.3.1.1"><p id="p64482741"><a name="p64482741"></a><a name="p64482741"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="57.330000000000005%" id="mcps1.1.3.1.2"><p id="p55719536"><a name="p55719536"></a><a name="p55719536"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row16988543"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p33894731"><a name="p33894731"></a><a name="p33894731"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p61118651"><a name="p61118651"></a><a name="p61118651"></a>服务器未能处理请求。</p>
    </td>
    </tr>
    <tr id="row13196948"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p62319862"><a name="p62319862"></a><a name="p62319862"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p14744048"><a name="p14744048"></a><a name="p14744048"></a>被请求的页面需要用户名和密码。</p>
    </td>
    </tr>
    <tr id="row65587574"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p10993288"><a name="p10993288"></a><a name="p10993288"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p18041159"><a name="p18041159"></a><a name="p18041159"></a>对被请求的页面访问禁止。</p>
    </td>
    </tr>
    <tr id="row28152706"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p65776751"><a name="p65776751"></a><a name="p65776751"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p26316604"><a name="p26316604"></a><a name="p26316604"></a>服务器无法找到被请求的页面。</p>
    </td>
    </tr>
    <tr id="row35522846"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p58778271"><a name="p58778271"></a><a name="p58778271"></a>405 Method Not Allowed</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p63419476"><a name="p63419476"></a><a name="p63419476"></a>请求中指定的方法不被允许。</p>
    </td>
    </tr>
    <tr id="row33904373"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p61899732"><a name="p61899732"></a><a name="p61899732"></a>406 Not Acceptable</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p47822428"><a name="p47822428"></a><a name="p47822428"></a>服务器生成的响应无法被客户端所接受。</p>
    </td>
    </tr>
    <tr id="row27748670"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p33049813"><a name="p33049813"></a><a name="p33049813"></a>407 Proxy Authentication Required</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p59789225"><a name="p59789225"></a><a name="p59789225"></a>用户必须首先使用代理服务器进行验证，这样请求才会被处理。</p>
    </td>
    </tr>
    <tr id="row1232117"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p32692654"><a name="p32692654"></a><a name="p32692654"></a>408 Request Timeout</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p30859352"><a name="p30859352"></a><a name="p30859352"></a>请求超出了服务器的等待时间。</p>
    </td>
    </tr>
    <tr id="row9298719"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p14998773"><a name="p14998773"></a><a name="p14998773"></a>409 Conflict</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p6941071"><a name="p6941071"></a><a name="p6941071"></a>由于冲突，请求无法被完成。</p>
    </td>
    </tr>
    <tr id="row62469641"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p26876165"><a name="p26876165"></a><a name="p26876165"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p29485753"><a name="p29485753"></a><a name="p29485753"></a>请求未完成。服务异常。</p>
    </td>
    </tr>
    <tr id="row64045192"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p20278084"><a name="p20278084"></a><a name="p20278084"></a>501 Not Implemented</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p31912141"><a name="p31912141"></a><a name="p31912141"></a>请求未完成。服务器不支持所请求的功能。</p>
    </td>
    </tr>
    <tr id="row18773818"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p44284256"><a name="p44284256"></a><a name="p44284256"></a>502 Bad Gateway</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p30254983"><a name="p30254983"></a><a name="p30254983"></a>请求未完成。服务器从上游服务器收到一个无效的响应。</p>
    </td>
    </tr>
    <tr id="row3859394"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p44175501"><a name="p44175501"></a><a name="p44175501"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p21445804"><a name="p21445804"></a><a name="p21445804"></a>请求未完成。系统暂时异常。</p>
    </td>
    </tr>
    <tr id="row58794511"><td class="cellrowborder" valign="top" width="42.67%" headers="mcps1.1.3.1.1 "><p id="p64734920"><a name="p64734920"></a><a name="p64734920"></a>504 Gateway Timeout</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.330000000000005%" headers="mcps1.1.3.1.2 "><p id="p9037129"><a name="p9037129"></a><a name="p9037129"></a>网关超时。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 错误码<a name="section17669131616110"></a>

请参考[错误码](错误码.md)。

