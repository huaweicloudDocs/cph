# 策略语法：RBAC<a name="cph_ug_0017"></a>

## 策略结构<a name="zh-cn_topic_0173481717_zh-cn_topic_0172268190_section1661242202715"></a>

策略结构包括：策略版本号（Version）、策略授权语句（Statement）和策略依赖（Depends）。

**图 1**  策略结构<a name="zh-cn_topic_0173481717_zh-cn_topic_0172268190_fig2641112616326"></a>  
![](figures/策略结构.png "策略结构")

## 策略语法<a name="section789713102221"></a>

如下以CPH服务的“CPH Administraor”为例，说明RBAC策略语法。

![](figures/RDBC.png)

```
{
        "Version": "1.0",
        "Statement":[
                {
                        "Action": [
                                "cph:*:*"
                        ],
                        "Effect": "Allow"
                }
        ]
}
```

**表 1**  参数说明

<a name="table4805855114411"></a>
<table><thead align="left"><tr id="row8886195594416"><th class="cellrowborder" colspan="2" valign="top" id="mcps1.2.5.1.1"><p id="p208861355114419"><a name="p208861355114419"></a><a name="p208861355114419"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" id="mcps1.2.5.1.2"><p id="p17886165510447"><a name="p17886165510447"></a><a name="p17886165510447"></a>含义</p>
</th>
<th class="cellrowborder" valign="top" id="mcps1.2.5.1.3"><p id="p1388655514447"><a name="p1388655514447"></a><a name="p1388655514447"></a>值</p>
</th>
</tr>
</thead>
<tbody><tr id="row3886655114415"><td class="cellrowborder" colspan="2" valign="top" headers="mcps1.2.5.1.1 "><p id="p12886155154416"><a name="p12886155154416"></a><a name="p12886155154416"></a>Version</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1988635512447"><a name="p1988635512447"></a><a name="p1988635512447"></a>策略的版本</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p8886115564418"><a name="p8886115564418"></a><a name="p8886115564418"></a>固定为“1.0”</p>
</td>
</tr>
<tr id="row5887185515441"><td class="cellrowborder" rowspan="2" valign="top" width="17.17171717171717%" headers="mcps1.2.5.1.1 "><p id="p128871755134412"><a name="p128871755134412"></a><a name="p128871755134412"></a>Statement</p>
</td>
<td class="cellrowborder" valign="top" width="17.17171717171717%" headers="mcps1.2.5.1.1 "><p id="p08878555448"><a name="p08878555448"></a><a name="p08878555448"></a>Action</p>
</td>
<td class="cellrowborder" valign="top" width="27.14271427142714%" headers="mcps1.2.5.1.2 "><p id="p178871955184419"><a name="p178871955184419"></a><a name="p178871955184419"></a>定义对CPH 的具体操作。</p>
</td>
<td class="cellrowborder" valign="top" width="38.513851385138516%" headers="mcps1.2.5.1.3 "><p id="p2088785524410"><a name="p2088785524410"></a><a name="p2088785524410"></a>格式为：服务名:资源类型:操作</p>
<p id="p58871955144410"><a name="p58871955144410"></a><a name="p58871955144410"></a>"cph:*:*"，其中cph为服务名称；“*”为通配符，表示对CPH的所有资源类型执行所有操作。</p>
</td>
</tr>
<tr id="row188785524410"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1887755154417"><a name="p1887755154417"></a><a name="p1887755154417"></a>Effect</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1788719556444"><a name="p1788719556444"></a><a name="p1788719556444"></a>定义Action中所包含的具体操作是否允许执行。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><a name="ul188871455134417"></a><a name="ul188871455134417"></a><ul id="ul188871455134417"><li>Allow：允许执行。</li><li>Deny：不允许执行。</li></ul>
</td>
</tr>
<tr id="row1588715544411"><td class="cellrowborder" rowspan="2" valign="top" width="17.17171717171717%" headers="mcps1.2.5.1.1 "><p id="p1688715555445"><a name="p1688715555445"></a><a name="p1688715555445"></a>Depends</p>
</td>
<td class="cellrowborder" valign="top" width="17.17171717171717%" headers="mcps1.2.5.1.1 "><p id="p38871055154411"><a name="p38871055154411"></a><a name="p38871055154411"></a>catalog</p>
</td>
<td class="cellrowborder" valign="top" width="27.14271427142714%" headers="mcps1.2.5.1.2 "><p id="p12887115544418"><a name="p12887115544418"></a><a name="p12887115544418"></a>依赖的策略的所属服务。</p>
</td>
<td class="cellrowborder" valign="top" width="38.513851385138516%" headers="mcps1.2.5.1.3 "><p id="p18887185574414"><a name="p18887185574414"></a><a name="p18887185574414"></a>服务名称</p>
<p id="p2088795524414"><a name="p2088795524414"></a><a name="p2088795524414"></a>例如：BASE</p>
</td>
</tr>
<tr id="row38871155174412"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p3887355204419"><a name="p3887355204419"></a><a name="p3887355204419"></a>display_name</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p12887655154413"><a name="p12887655154413"></a><a name="p12887655154413"></a>依赖的策略的名称。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p158887551446"><a name="p158887551446"></a><a name="p158887551446"></a>权限名称</p>
<p id="p688825519446"><a name="p688825519446"></a><a name="p688825519446"></a>例如：Tenant Administrator</p>
</td>
</tr>
</tbody>
</table>

