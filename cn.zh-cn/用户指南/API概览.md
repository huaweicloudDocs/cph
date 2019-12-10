# API概览<a name="zh-cn_topic_0130762807"></a>

通过使用弹性伸缩所提供的接口，您可以完整的使用弹性伸缩的所有功能，例如创建伸缩组。弹性伸缩支持的接口见[表1](#zh-cn_topic_0121588224_table5876102613294)。

**表 1**  弹性伸缩接口说明

<a name="zh-cn_topic_0121588224_table5876102613294"></a>
<table><thead align="left"><tr id="zh-cn_topic_0121588224_row3878122616298"><th class="cellrowborder" valign="top" width="17.44%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0121588224_p68781126182914"><a name="zh-cn_topic_0121588224_p68781126182914"></a><a name="zh-cn_topic_0121588224_p68781126182914"></a><strong id="zh-cn_topic_0121588224_b125201844173712"><a name="zh-cn_topic_0121588224_b125201844173712"></a><a name="zh-cn_topic_0121588224_b125201844173712"></a>子类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="82.56%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0121588224_p158781726112914"><a name="zh-cn_topic_0121588224_p158781726112914"></a><a name="zh-cn_topic_0121588224_p158781726112914"></a><strong id="zh-cn_topic_0121588224_b15203449370"><a name="zh-cn_topic_0121588224_b15203449370"></a><a name="zh-cn_topic_0121588224_b15203449370"></a>说明</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0121588224_row148781026122919"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0121588224_p128788265295"><a name="zh-cn_topic_0121588224_p128788265295"></a><a name="zh-cn_topic_0121588224_p128788265295"></a>弹性伸缩组</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0121588224_p56591328178"><a name="zh-cn_topic_0121588224_p56591328178"></a><a name="zh-cn_topic_0121588224_p56591328178"></a>实现伸缩组的创建、查询、修改、删除等操作。</p>
</td>
</tr>
<tr id="zh-cn_topic_0121588224_row1987820263297"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0121588224_p8939172693215"><a name="zh-cn_topic_0121588224_p8939172693215"></a><a name="zh-cn_topic_0121588224_p8939172693215"></a>弹性伸缩配置</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0121588224_p86434284717"><a name="zh-cn_topic_0121588224_p86434284717"></a><a name="zh-cn_topic_0121588224_p86434284717"></a>实现伸缩配置的创建、查询、删除等操作。</p>
</td>
</tr>
<tr id="zh-cn_topic_0121588224_row87746166614"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0121588224_p197741716567"><a name="zh-cn_topic_0121588224_p197741716567"></a><a name="zh-cn_topic_0121588224_p197741716567"></a>弹性伸缩实例</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0121588224_p1477491610610"><a name="zh-cn_topic_0121588224_p1477491610610"></a><a name="zh-cn_topic_0121588224_p1477491610610"></a>实现伸缩实例的查询、移出伸缩组等操作。</p>
</td>
</tr>
<tr id="zh-cn_topic_0121588224_row816313459617"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0121588224_p1216317451267"><a name="zh-cn_topic_0121588224_p1216317451267"></a><a name="zh-cn_topic_0121588224_p1216317451267"></a>弹性伸缩策略</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0121588224_p7163194516616"><a name="zh-cn_topic_0121588224_p7163194516616"></a><a name="zh-cn_topic_0121588224_p7163194516616"></a>实现伸缩策略的创建、查询、修改、删除等操作。</p>
</td>
</tr>
<tr id="zh-cn_topic_0121588224_row132213492619"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0121588224_p1722949363"><a name="zh-cn_topic_0121588224_p1722949363"></a><a name="zh-cn_topic_0121588224_p1722949363"></a>伸缩策略执行日志</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0121588224_p15221849464"><a name="zh-cn_topic_0121588224_p15221849464"></a><a name="zh-cn_topic_0121588224_p15221849464"></a>查询伸缩策略执行的历史记录。</p>
</td>
</tr>
<tr id="zh-cn_topic_0121588224_row9878726192911"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="p1866520431243"><a name="p1866520431243"></a><a name="p1866520431243"></a>伸缩活动日志</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0121588224_p14101184217244"><a name="zh-cn_topic_0121588224_p14101184217244"></a><a name="zh-cn_topic_0121588224_p14101184217244"></a>查询伸缩活动日志。</p>
</td>
</tr>
<tr id="zh-cn_topic_0121588224_row9878172662914"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0121588224_p1310194211243"><a name="zh-cn_topic_0121588224_p1310194211243"></a><a name="zh-cn_topic_0121588224_p1310194211243"></a>配额</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="p10578662"><a name="p10578662"></a><a name="p10578662"></a>查询指定租户的弹性伸缩组、伸缩配置、伸缩策略和伸缩实例的配额总数及已使用配额数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0121588224_row117351143103220"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0121588224_p15101134272411"><a name="zh-cn_topic_0121588224_p15101134272411"></a><a name="zh-cn_topic_0121588224_p15101134272411"></a>通知</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="p9961350469"><a name="p9961350469"></a><a name="p9961350469"></a>提供配置伸缩组通知、查询伸缩组通知列表和删除伸缩组通知功能。</p>
</td>
</tr>
<tr id="zh-cn_topic_0121588224_row11736144363213"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0121588224_p51011542102411"><a name="zh-cn_topic_0121588224_p51011542102411"></a><a name="zh-cn_topic_0121588224_p51011542102411"></a>生命周期挂钩</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0121588224_p20101542202416"><a name="zh-cn_topic_0121588224_p20101542202416"></a><a name="zh-cn_topic_0121588224_p20101542202416"></a>提供创建、查询、修改和删除生命周期挂钩等功能。</p>
</td>
</tr>
<tr id="row181481125813"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="p31491112181"><a name="p31491112181"></a><a name="p31491112181"></a>标签管理</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="p10149191217812"><a name="p10149191217812"></a><a name="p10149191217812"></a>提供查询租户或资源标签、创建或删除标签和查询资源实例的功能。</p>
</td>
</tr>
<tr id="row1195513153219"><td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.3.1.1 "><p id="p2019661316328"><a name="p2019661316328"></a><a name="p2019661316328"></a>弹性伸缩API管理</p>
</td>
<td class="cellrowborder" valign="top" width="82.56%" headers="mcps1.2.3.1.2 "><p id="p63514241380"><a name="p63514241380"></a><a name="p63514241380"></a>提供查询弹性伸缩API版本信息的功能。</p>
</td>
</tr>
</tbody>
</table>

