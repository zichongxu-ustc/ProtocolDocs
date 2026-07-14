---
date: 2022-01-06
category:
  - Category A
  - Category B
tag:
  - tag A
  - tag B
---

# PerturbSeq
<!-- more -->
<img :src="$withBase('/picture/PerturbSeq/001.png')" />

## 准备工作
1.  样本准备：FACS 出的 mAmetrine+ 细胞，FACS 后测量细胞密度是否符合预期 
2.  干浴器设置   
Program A 细胞裂解 
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Preheated </td>
    <td>25℃  </td>
    <td></td>
  </tr>
  <tr>
    <td rowspan="3">Heated</td>
    <td>25℃ </td>
    <td>15min </td>
  </tr>
  <tr>
    <td>37℃ </td>
    <td>45min </td>
  </tr>
  <tr>
    <td>25℃  </td>
    <td>10min  </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>20℃ </td>
  </tr>
</table>

Program B 细胞核裂解 
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Preheated </td>
    <td>66℃ </td>
    <td></td>
  </tr>
  <tr>
    <td rowspan="2">Heated</td>
    <td>66℃ /td>
    <td>45min </td>
  </tr>
  <tr>
    <td>25℃ </td>
    <td>10min </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>4℃ </td>
  </tr>
</table>

Program C 逆转录（sc 3’ RNA prep only） 
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Preheated </td>
    <td>25℃  </td>
    <td></td>
  </tr>
  <tr>
    <td rowspan="3">Heated</td>
    <td>25℃ </td>
    <td>30min </td>
  </tr>
  <tr>
    <td>42℃ </td>
    <td>90min </td>
  </tr>
  <tr>
    <td>85℃  </td>
    <td>10min  </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>4℃ </td>
  </tr>
</table>

Program E 逆转录（CRISPR prep only） 
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Preheated </td>
    <td>25℃  </td>
    <td></td>
  </tr>
  <tr>
    <td>Heated</td>
    <td>42℃ </td>
    <td>90min </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>4℃ </td>
  </tr>
</table>

Program F （CRISPR prep only） 
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Preheated </td>
    <td>37℃  </td>
    <td></td>
  </tr>
  <tr>
    <td rowspan="2">Heated</td>
    <td>37℃ </td>
    <td>20min </td>
  </tr>
  <tr>
    <td>85℃ </td>
    <td>10min </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>20℃ </td>
  </tr>
</table>

3.  解冻试剂 

<table>
  <tr>
  <th colspan="4">15～30℃储存 </th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th></th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>PAR   </td>
    <td>Partitioning Reagent </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 1 </td>
    <td>室温使用 </td>
  </tr>
  <tr>
    <td>CLB3   </td>
    <td></td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 1 </td>
    <td>室温使用 </td>
  </tr>
  <tr>
    <td>DPR  </td>
    <td>Departitioning Reagent </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 1 </td>
    <td>室温使用 </td>
  </tr>
  <tr>
  <th colspan="4">2～8℃储存  </th>
  </tr>
  <tr>
    <td>BBF </td>
    <td>Breaking Buffer </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 2 </td>
    <td>室温放置 30min </td>
  </tr>
  <tr>
    <td>PWB1 </td>
    <td>Wash Buffer </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 2 </td>
    <td>冰上放置 </td>
  </tr>
  <tr>
  <th colspan="4">-25～-15℃储存 </th>
  </tr>
  <tr>
    <td>CSB</td>
    <td>Cell Suspension Buffer</td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 3 </td>
    <td>冻存细胞使用需水浴加热至 37℃；新鲜细胞需冰上放置  </td>
  </tr>
  <tr>
    <td>RNI </td>
    <td>RNase Inhibitor </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 3 </td>
    <td>冰上放置  </td>
  </tr>
  <tr>
    <td>RTAM </td>
    <td>RT Additive Mix </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 3 </td>
    <td>冰上溶解  </td>
  </tr>
  <tr>
    <td>RTEM </td>
    <td>RT Enzyme Mix </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 3 </td>
    <td>冰上放置  </td>
  </tr>
  <tr>
    <td>PMM4 </td>
    <td>4X PCR Master Mix </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 3 </td>
    <td>冰上放置  </td>
  </tr>
  <tr>
    <td>WTA2 </td>
    <td>WTA Primer </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 3 </td>
    <td>冰上溶解 </td>
  </tr>
  <tr>
    <td>RTF </td>
    <td>RT Finishing Reagent </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 3 </td>
    <td>冰上放置  </td>
  </tr>
  <tr>
    <td>TSO2 </td>
    <td>Template-Switch Oligo </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 3 </td>
    <td>冰上溶解 </td>
  </tr>
  <tr>
  <th colspan="4">-85～-65℃储存 </th>
  </tr>
  <tr>
    <td>CPIPs </td>
    <td>T10 CRISPR PIPs </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 4 </td>
    <td>冰上溶解，每管供一个样本。冰上至多稳定5h。 </td>
  </tr>

</table> 

# Stage 1 mRNA Capture 
## Step 1  单细胞悬液制备（1-1.5 hrs）
### 实验材料
- Cell Suspension Buffer（CSB）<mark>细胞稀释步骤必须使用 Cell Suspension Buffer</mark>
- 1000 μL 大孔径、低残留移液器吸头 
- 细胞计数材料 
- 1.5 ml Safe-Lock PCR Clean tubes (emulsion safe) 

### 实验步骤

1. 室温下350× g 离心 5 min（使用吊篮式转子）使细胞沉淀
2. 小心弃去上清，准备加入 CSB 进行洗涤，以除去抑制性试剂
3. 按照以下步骤清洗：
  a)  拿出 37℃预热的 CSB 并置于生物安全柜  
  b)  加 2 mL CSB，<mark>剩余 CSB 置于冰上  </mark>
  c)  使用 1000 µL大口径移液器吸头，缓慢移液 5 次以混合  
  d)  350× g 离心 5 min   
  e)  小心弃去上清   
4. 加入 100-500 µL 预冷 CSB
5. 用尽可能轻的力度吹打混匀 10-15 次  
<mark><b>注：</b>如果可见团块，增加吹打力度，最好使用最少的力度和次数进行混匀。</mark>

6. 计数细胞以确定细胞密度及活率，最终细胞密度：2.6e7 ~3.4e7/mL，活率>90%；每次稀释都需要重复计数，一旦确定细胞浓度立即置于冰上准备捕获与裂解。
## Step 2 单细胞捕获与化学裂解
### 实验材料
- CLB3 
- CPIP 
- PAR 
- RNI 
- 0.5 mL Safe-Lock PCR Clean tubes (emulsion safe) 
- 1 mL syringe 
- 200 µL 大孔径、低残留移液器吸头 
- G22 blunt bottom syringe needle 
- 0.5/1.5 mL combination tube stand (blue) 

### 试剂预处理与仪器设置
1. CLB3——若观察到结晶，将其置于 25°C 的干浴器中，使其平衡至室温，涡旋 10 s， 然后瞬时离心；若无结晶，涡旋 5s，然后瞬时离心 
2.  CPIPs——瞬时离心 5s，冰上放置。 
3.  标记 0.5 mL PCR 管为 CLB3 管，每个反应准备一管（准备一管）。 
4.  将 PIPseq vortexer 设置为 3000 rpm 2min 
5.  根据样品类型使用不同选项设置盖子温度
6.  干浴器选择 Prog. A，然后手动将盖子温度按照以下操作设置为 +5.0  
a.  选择 Edit  
b.  选择 LidMode 切换到+5.0  
c.  选择 Save/Return  
1.  选择“Run”，将干浴器预热至适用裂解程序的保持温度。 
2.  选择“Lid On”预热干浴器盖子，当控制盖子温度时显示的是 LidOff 
### 实验步骤
1.  使用 200 μL 的大口径移液器吸头，缓慢移液 10 次以混合细胞悬液。 
2.  向 CPIP 管中的 CPIP 层缓慢加入 1 μL RNI（40 units） 
3.  向 CPIP 管中的 CPIP 层加入 4 μL 细胞悬液（密度：2.6 x 10 7 ~3.4 x 10 7  /mL，总共104000～13600） 
4.  将 200μL 移液枪调至 75 μL 缓慢吸吹 10 次混匀，<mark>以免产生气泡。 </mark>
5.  移除枪头时，沿管壁非常缓慢地打出最后一滴，以避免产生过多泡沫并减少 CPIP 的损失。 
6.  使用 1000 μL 的枪头，沿着 CPIP 管的侧壁加入 320 μL 的 PAR。 
7.  盖紧管盖，水平放入涡旋适配器的管位中，确保管子完全插入适配器中 
<img :src="$withBase('/picture/PerturbSeq/002.png')" />

8.   3000 rpm 震荡 15 秒后手动停止； 
9.  旋转适配器切换至垂直位，以 3000 rpm 震荡 2 分钟； 
<img :src="$withBase('/picture/PerturbSeq/003.png')" />

10.  将 PIP 管放入 <mark>combination tube stand（blue）</mark> 的 0.5 mL 侧，确保管子完全插入； 
11.  静置约 30 秒使乳液分层。 
<img :src="$withBase('/picture/PerturbSeq/004.png')" />

12.  使用安装在 1 mL 注射器上的 G22 钝头注射针，按照如下步骤吸取并弃去多余的 PAR（下层相）  
a.  将注射器针头缓缓穿过乳液（如图 A）降至试管底部。  
b.  等待 5 s。  
c.  抽吸下层液相，直至 CPIP 乳液底部接近管架 B 层，注意不要抽吸到任何乳液。  
d.  移除针头时，在管子内壁擦拭一下。  
e.  弃去针头和注射器到利器盒中  
<img :src="$withBase('/picture/PerturbSeq/005.png')" />

<mark><b>注：</b>在捕获和裂解步骤的剩余步骤内，请勿将 PIP 管置于冰上，以免裂解试剂沉淀</mark>  

13.   制备化学裂解乳液（配制一个样品的量）： 
- CLB3（90 μL） 
- PAR（270 μL）  
<mark><b>注：</b>切勿大量配制化学裂解乳液。每个样本应分别单独配制。</mark> 

14.   <b>涡旋化学裂解乳液 10s 混匀 </b> 
<mark>在转移前充分混匀 CLB3 和 PAR 对形成乳液至关重要</mark> 

15.   用 1000 μL 低残留枪头立即将每个 CLB3 管中的全部化学裂解乳液移至每个 CPIP 管中 
16.   颠倒混匀 10-15 次 
17.   将 CPIP 管置于预热的干浴器上。 
18.   选择 <b>Skip</b>，然后选择 <b>Yes</b> 以运行裂解程序 <b>Prog. A</b>   

## Step 3 mRNA分离
### 耗材准备
- BBF(Breaking Buffer) 
- DPR(Departitioning Reagent) 
- PWB1(Washing Buffer) 
- 0.5 ml Safe-Lock PCR Clean tubes (emulsion safe) 
- 1.5 ml Safe-Lock PCR Clean tubes (emulsion safe) 
- 1 ml syringe 
- G22 blunt bottom syringe needle 
- 0.5/1.5 ml combination tube stand (blue) 
### 试剂预处理与仪器设置
1.  BBF: 颠倒混匀 
2.  用 PWB1 配制<b>洗涤缓冲液</b>：   
a.  为每个样品标记一个 1.5 ml 管为 Wash 1；   
b.  向每管中加入 1 ml PWB1。   
c.  将 Wash 1 管置于冰上。   
### 实验步骤
#### 破乳
1.  将 CPIP 管从干浴器中取出，放入管架。 
<mark><b>注：</b>管内出现凝结物是正常的，切勿离心乳液。</mark> 

2.  使用新的安装在 1 mL 注射器上的 G22 钝头注射针，按照如下步骤吸取并弃去剩余的CLB3。  
a.  将注射器针头缓缓穿过乳液（如图 A）降至试管底部。   
b.  等待 5 s。  
c.  抽吸下层液相，直至 CPIP 乳液顶部接近<b>管架 A 层</b>，注意不要抽吸到任何乳液。  
d.  移除针头时，在管子内壁擦拭一下。  
e.  弃取针头和注射器到利器盒中 
<img :src="$withBase('/picture/PerturbSeq/006.png')" />

<mark><b>注：</b>尽可能多地移除底部相。</mark> 

3.  沿管壁向每个样本加入 300 μL BBF（澄清液） 
4.  沿管壁向每个样本加入 100 μL DPR （粉色） 
5.  将 PIP 管盖紧 
6.  颠倒混匀 10 - 20 次以破乳 
7.  瞬时离心 10s 
<b>8.  通过肉眼观察粉红色底层相与上层均匀的水溶液（含 PIP）之间有明显的分界面从而确保乳液已完全破乳。 </b>

9.  检查<mark>上层不透明相是否有任何不均匀现象</mark>，代表有乳液未破乳。 
a.  若观察到未破乳的乳浊液，加入 10 μL DPR，然后重复步骤 5-7。 
b.  若仍残留有未破乳的乳浊液，加入 50 μL 的 DPR，然后重复步骤 5-7。 
10.  使用新的安装在 1 mL 注射器上的 G22 钝头注射针，移去所有底部的粉色液相层。若观察到
粉色液滴，与粉色液相层一并移去 
<img :src="$withBase('/picture/PerturbSeq/007.png')" />

11.  弃取针头和注射器 
12.  瞬时离心 10s 
13.  使用新的安装在 1 mL 注射器上的 G22 钝头注射针，移去所有剩余的粉色液相层 
14.  如果在离心管侧壁出现粉红色下层相的拖痕（残留液痕），则离心 1 min 
15.  用注射器尽可能移去所有粉色液相层 
<mark><b>注：</b>即使少量移除部分透明上层液（水相）也是可以接受的，但绝不能残留粉色液相层，否则会抑制逆转录反应导致 cDNA 产量降低和片段大小变小。</mark> 

#### PIPs 洗涤
1.  使用 200 μL 低残留吸头，将 CPIPs 由 CPIP 管缓慢转移至<b>预冷的 Wash 1 管</b>（内含 1 ml PWB1），为确保移液器吸头内无残留，需在 Wash 1 管中上下混匀至少 3 次。 
2.  瞬时离心回收原 CPIP 管中的残余 CPIPs。 
3.  将 CPIP 管中剩余的所有 CPIP 转移至对应的 Wash 1 管中。 
4.  将 Wash 1 管放入管架 
5.  将管架水平放置在水平涡旋混合器上涡旋混合约 3 s。 
6.  离心 1 分钟，将 Wash 1 管放回管架。 
7.  不要触及沉淀颗粒，弃去上清液至 管架 的“3”体积刻度处。 
<mark><b>注：</b>此时颗粒呈半透明状，操作时应保持极其小心，去除多余体积可能会导致 PIP 的损失。</mark> 

8.  按以下步骤洗涤第二次： 
a.  向每管中加入 1200 μL 1× PWB1 
b.  将 管架水平放置在平头涡旋混合器上涡旋混合约 3 s 
c.  离心 1 min，然后将管放回管架。 
d.  在不搅动沉淀颗粒的情况下，将上清液吸至 stand 的“4”体积刻度处。 
9.  如步骤 8 洗涤第三次，使用 1000 μL 1× PWB1 
10.  如步骤 8 洗涤第四次，使用 1000 μL 1× PWB1 
## Step 4 标准化 PIP 体积（10 min） 
### 耗材准备
- 0.5 ml Safe-Lock PCR Clean tubes (emulsion safe) 
### 试剂预处理与仪器设置
用记号笔在每个 0.5 ml 管的 0.1 mL 刻度处标记 
### 实验步骤
1.  将每个样品约 200 μL 的 CPIPs 混合物转移至标记的 0.5 ml 管中。 
<b>注：在接下来的离心和弃去上清步骤中每次处理两个样品来确保最佳的 CPIP 沉淀 </b>
2.  离心 1 min 
3.  倾斜 0.5 ml 管，使用 200 μL 低残留枪头立即弃去 0.1 ml 标记下的上清 
<mark><b>注：</b>不要触及 CPIPs</mark> 
<img :src="$withBase('/picture/PerturbSeq/008.png')" />

4.  将管置于冰上，然后立即进行 cDNA 合成。 

# Stage 2 cDNA Prep 
## Step 5 cDNA 合成（2 hr 30 min） 
### 耗材准备
- RTAM (RT Additive Mix)
- RTEM (RT Enzyme Mix) 
- RTF 
- TSO2 
### 试剂预处理与仪器设置
1.  按照以下步骤处理试剂： 
- RTAM (RT Additive Mix)——吹吸混匀 
- RTEM (RT Enzyme Mix) ——吹吸混匀 
- RTF——吹吸混匀 
- TSO2——涡旋混匀后瞬时离心 
2.  干浴器选择 Prog. E，然后将盖子温度按照以下操作设置为 105 ℃。   
选择 Edit   
选择 LidMode 切换到 105 ℃   
选择 Save/Return   
3.  选择“Run”，将干浴器预热至 42℃。 
4.  选择“Lid On”预热干浴器盖子 
当控制盖子温度时显示的是 LidOff，仅当孵育温度高于 35℃时，盖子温度才会升至 105℃ 
### 实验步骤
1.  RT Master Mix 配制： 

| Reagent | Volume Per Reaction(μL) | 4.4X Reaction Master Mix(μL) | 8.8X Reaction Master Mix(μL) |
| :-----: | :---------------------: | :--------------------------: | :--------------------------: |
|  RTAM   |           80            |             352              |             704              |
|  TSO2   |            8            |              35              |              70              |
|  RTEM   |           12            |              53              |             106              |
|  Total  |           100           |             440              |             880              |

2. 吹打混匀 
3.  短暂离心，使液体沉至管底。 
4.  向每个 CPIP 管中加入 100 μL RT Master Mix。 
5.  涡旋 5s 混匀 
6.  瞬时离心 
7.  将 CPIP 管置于干浴器中 
8.  选择 Skip，然后选择 Yes 运行 cDNA 合成程序 
注：当干浴器温度达到 25℃时移去样品 
9.  从干浴器中移去样品 
10.  每个反应管加 20 μL RTF 
11.  涡旋混匀 
12.  若需要可瞬时离心收集管壁液体 
13.  干浴器选择 Prog.F，然后手动将盖子温度按照以下操作设置为 +5.0。   
a.  选择 Edit   
b.  选择 LidMode 切换到+5.0   
c.  选择 Save/Return   
14.  选择“Lid On”预热干浴器盖子，当控制盖子温度时显示的是 LidOff 
15.  选择“Run”，将干浴器预热至 37℃ 
16.  将样品放入干浴器 
17.  选择 Skip，然后选择 Yes 运行程序 
18.  当程序运行完成后立即准备 CPIP 清洗 
## Step 6 PIP 洗涤（30 min） 
### 耗材准备
- PWB1 
- 无核酶水（实验室自备）
- 0.5/1.5 ml 管架（蓝色） 
### 试剂预处理与仪器设置
配制 0.5 × Washing Buffer： 
- PWB1（625 μL） 
- 无核酸酶水（625 μL） 
每个样品使用 1250 μL 0.5 × PWB1
### 实验步骤
1.  离心 CPIP 管 1 min 
2.  不触及 CPIP 的情况下弃去 130 μL 上清 
3.  按以下步骤清洗 CPIPs：   
a.  加入 450 μL 0.5 × PWB1   
b.  涡旋 5 s。   
c.  离心 1 min 后置于管架上   
d.  不要触及沉淀，弃去上清至管架 A 刻度线处。   
4.  重复步骤 3 第二次清洗 PIPs。使用 350 μL 0.5 × PWB1 
5.  重复步骤 3 第三次清洗 PIPs。使用 350 μL 0.5 × PWB1 
6.  第四次清洗 PIPs。使用 150 μL 0.5 × Washing Buffer。 
7.  离心 1min。 
8.  保持管子的角度，立即弃去上清至 0.1 ml 标记处 
9.  冰上放置样品并<mark>立即进行 cDNA 扩增</mark> 
## Step 7 cDNA 扩增（1 hr） 
### 耗材准备 
- PMM4 (4X PCR Master Mix) 
- WTA2  
- 0.2 ml 8-tube strips and caps 
### 试剂预处理与仪器设置
1.  按照以下步骤处理试剂： 
- PMM4——吹吸混匀后瞬时离心 
- WTA2——吹吸混匀后瞬时离心 
2.  在 PCR 仪中设置<b> cDNA Amplication </b>程序： 
Set the lid temperature to 105 ℃ 
Set the reaction volume to ？ 

<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Denaturation</td>
    <td>95℃ </td>
    <td>15 s </td>
  </tr>
  <tr>
    <td rowspan="3">5 Cycles </td>
    <td>98℃ </td>
    <td>15 s </td>
  </tr>
  <tr>
    <td>65℃</td>
    <td>1 min </td>
  </tr>
  <tr>
    <td>71℃ </td>
    <td>9 min </td>
  </tr>
  <tr>
    <td>Final Extension </td>
    <td>72℃ </td>
    <td>5 min </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>4℃ </td>
  </tr>
</table>
<mark>注：指定的程序参数对于检测性能至关重要。请勿更改 PCR 循环次数。更改程序会导致结果无法使用。</mark>（<span style="color: red;">注意设置程序时循环数-1</span>） 

### 实验步骤
1.  将以下试剂混合于 1.5 mL EP 管中，制备 WTA Master Mix： 

| Reagent | Volume Per Reaction(μL) | 4.4X Reaction Master Mix(μL) | 8.8X Reaction Master Mix(μL) |
| :-----: | :---------------------: | :--------------------------: | :--------------------------: |
|  PMM4   |           34            |             149              |            299.2             |
|  WTA2   |           1.4           |              6               |             12.3             |
|  Total  |          35.4           |             155              |            311.5             |
2.  涡旋混匀然后瞬时离心。 
3.  向每个样品管中加入 35 μL WTA Master Mix 
4.  轻弹管壁使沉淀分散，然后涡旋混匀 5s 
5.  用低残留 200 μL 枪头，将每个样品的 WTA 反应混合物分装在 8 联排的两个管中，每管
68 μL（x 2） 
6.  标记每个样品的 8 联排管 
7.  将其置于 PCR 仪上，运行 <b>cDNA Amplication </b>程序。 
<span style="color: red;"><b>安全停止点：如果您要停止操作，请将样本置于4°C 的PCR仪中，或者将样本在2°C 至 8°C 下保存过夜。</b></span>

## 直至下一安全停止点前需要的准备工作
### 解冻试剂（2-8℃储存 ） 

<table>
  <tr>
  <th colspan="4">2-8℃储存</th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th></th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>CEB </td>
    <td>cDNA Extraction Buffer </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 2 </td>
    <td>室温使用  </td>
  </tr>
  <tr>
    <td>IPB2 </td>
    <td>Illumina Purification Beads 2 </td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 2 </td>
    <td>放置 30min 至室温 </td>
  </tr>
  <tr>
    <td>PWB1</td>
    <td>Washing Buffer</td>
    <td>illumina Single Cell CRISPR Prep Capture, T10, Box 2 </td>
    <td>冰上放置 </td>
  </tr>
  <tr>
  <th colspan="4">-25--15℃储存 </th>
  </tr>
  <tr>
    <td>PMM4 </td>
    <td>4X PCR Master Mix </td>
    <td>illumina Single Cell 3’ RNA Capture, T2, Box 3 </td>
    <td>冰上放置 </td>
  </tr>
  <tr>
    <td>WTA2</td>
    <td>WTA Primer Mix 2 </td>
    <td>illumina Single Cell 3’ RNA Capture, T2, Box 3 </td>
    <td>冰上溶解 </td>
  </tr>
</table>

## Step 8  从 CPIPs 中分离 cDNA（20 min）
### 耗材准备 
- CEB
-  0.5 ml Safe-Lock PCR Clean tubes (emulsion safe) 

### 试剂预处理与仪器设置

1.  为每个样本标记两个新的 1.5 mL 管 
2.  CEB——颠倒混匀 

### 实验步骤
1.  <mark>如果您在安全停止点后重新开始，请将样本管瞬时离心。</mark> 
2.  向八联排中每个 cDNA 反应管中加入 100 μL CEB 
3.  将每个样品的两个反应管 Mix 转移到同一个新 1.5 mL 管中 
4.  将八联排瞬时离心，转移所有残留的液体到同一 1.5 mL 管中 
5.  涡旋后瞬时离心 1 min 
6.  不要触及沉淀，转移 200 μL 上清到一个新的 1.5 mL 离心管中 
7.  向每个含 CPIPs 的 1.5 mL 管中加入 200 μL CEB 
8.  涡旋后瞬时离心 1 min 
9.  不要触及沉淀，转移含 CPIP 管的 200 μL 上清到原已含有上清的管中 
<mark><b>注：</b>总上清体积 400 μL </mark>

10.  瞬时离心含上清的 1.5 mL 管，检查官底是否含 CPIPs 
11.  如果存在剩余的 CPIP，转移上清到新离心管中，测量转移上清的体积，从而调整后续清洗
过程的磁珠添加量 
12.  <mark><b>冰上放置</b></mark> CPIPs 准备做 gRNA 扩增 
## Step 9 cDNA清洗（30 min）
### 耗材准备 
-  IPB2
-  IDTE Buffer（自配）
- 无水乙醇（EtOH）
- 无核酶水（实验室自备）
- 0.2 ml 8-tube strips and caps
### 试剂预处理与仪器设置
1. IPB2——涡旋30s混匀
2. 每个反应需用无水乙醇和无核酶水配置2 mL新鲜的85%乙醇溶液
### 实验步骤
1.  对于每 400 µL的反应体积，加入 320 µL IPB2。 
<b>如有需要，可按 IPB2 体积的 0.8 倍调整磁珠体积。 </b>

2.  涡旋至完全混合均匀，然后瞬时离心使液体沉至管底 
<mark><b>注：</b>不要使磁珠沉淀，或吹打混匀 </mark>

3.  室温孵育 5 min。 
4.  置于磁力架上 
5.  静置 5min 至液体澄清。 
6.  如果 5 min 后磁珠仍未聚集，继续置于磁力架上，直至液体澄清。 
7.  不要搅动磁珠，移除并丢弃上清液。 
8.  按如下方法清洗磁珠：   
a. 加入 1 mL 新鲜的 85% 乙醇。   
b. 等待 30 s。   
c. 不要搅动磁珠，移除并丢弃 1 mL 乙醇。   
9. 重复步骤 8 再次清洗磁珠。 
10. 不要触及磁珠，用 20 μL 移液器吸除残留的乙醇。 
11. 自然风干至珠子表面仍有轻微光泽（约 5 min）。 根据湿度水平的不同，风干可能需要长达 10 min 的时间。 
<mark><b>注：</b>过度干燥珠子会导致其开裂并降低洗脱效率。</mark> 

12.   从磁力架上取下。 
13.   加入 42 μL IDTE 缓冲液。 
14.   涡旋混匀。 
15.  瞬时离心，使液体沉至管底 
注：不要使磁珠沉淀。 
16.   在室温下孵育 5 min。  
<mark><b>注：</b>如果磁珠过度干燥，在孵育过程中应频繁用移液管混匀，以尽量减少样品损失。</mark> 

17.   放入磁力架上 
18.   等待混合液澄清（约 2 min） 
19.   保持 1.5 mL 管置于磁力架上。 
20.   将 40 μL 上清液转移至新的 PCR 管中 
21.   立即置于冰上。 
<mark><span style="color: red;">此 cDNA 用作文库制备的输入</span></mark>。 
磁力架上的管中剩余的 2 μL 上清液用于 cDNA QC。   
<mark><b>用于文库制备的cDNA最多在-80中储存72h，储存环境一定要清洁无DNA污染</b></mark>

## Step 10 cDNA QC PCR（1 hr 20 min）
此步骤使用磁珠沉淀物中剩余的洗脱体积（2 μL）来评估 cDNA 的质量。
### 耗材准备
- PMM4（4× PCR Master Mix）
- PWB1
- WTA2（WTA Primer Mix 2）
- Nuclease-free water
- 0.2 ml 8-tube strips and caps
### 试剂预处理与仪器设置
准备以下试剂：
1. 配制0.5× PWB1—将以下各体积分别乘以样本数量。
-  PWB1（7 μL）  
-  无核酶水（7 μL）   
每个样品总计 14 μL 0.5× PWB1   
PMM4—吸吹混匀，瞬时离心。   
WTA2—吸吹混匀，瞬时离心。   
2.  将以下 QC Amplication 程序保存在热循环仪上, 此程序中，退火和延伸都在 69 ℃进行：   
Set the lid temperature to 105 ℃   
Set the reaction volume to 25 μL   
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Denaturation</td>
    <td>95℃ </td>
    <td>15 s </td>
  </tr>
  <tr>
    <td rowspan="3">X Cycles </td>
    <td>98℃ </td>
    <td>15 s </td>
  </tr>
  <tr>
    <td>65℃</td>
    <td>1 min </td>
  </tr>
  <tr>
    <td>71℃ </td>
    <td>9 min </td>
  </tr>
  <tr>
    <td>Final Extension </td>
    <td>72℃ </td>
    <td>5 min </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>4℃ </td>
  </tr>
</table>

调整程序以针对不同的输入质量和浓度进行优化
<table border="1">
  <tr>
    <th>Sample Input </th>
    <th>Number of QC PCR Cycles(X)</th>
  </tr>
  <tr>
    <td>High RNA sample types(eg, cell lines) </td>
    <td>10  </td>
  </tr>
  <tr>
    <td>Low RNA sample types(eg, primary cells and nuclei)</td>
    <td>12</td>
  </tr>
</table> 

### 实验步骤
1.  保持 cDNA 置于磁力架上，加入 10 μL 无核酶水。 
2.  不要触及沉淀，吸吹混匀 
3.  在室温下孵育 1 min。 
4.  不要搅动磁珠，从样品管中移取 10 μL 至新的 8 联排管中。 
5.  将样本置于冰上。 
6.  将以下各体积混合以制备 QC Master Mix： 

|  Reagent  | Volume Per Reaction(μL) | 4.4X Reaction Master Mix(μL) | 8.8X Reaction Master Mix(μL) |
| :-------: | :---------------------: | :--------------------------: | :--------------------------: |
|   PMM4    |          6.25           |             27.5             |              55              |
|   WTA2    |            1            |             4.4              |             8.8              |
| 0.5X PWB1 |          7.75           |             34.1             |             68.2             |
|   Total   |           15            |              66              |             132              |
7.  涡旋混匀，然后瞬时离心。 
8.  向每个样本中加入 15 μL 的 QC Master Mix。 
每个样本的总体积为 25 μL。 
9.  瞬时离心。 
10.  置于 PCR 仪上运行 QC Amplification 程序。 
<span style="color: red;"><b>安全停止点：如果您要停止操作，请将样本置于 4°C 的PCR仪中，或者将样本在 2°C 至 8°C 下保存过夜。</b></span>

## 直至下一安全停止点前需要的准备工作
解冻试剂： 
<table>
  <tr>
  <th colspan="3">2-8℃储存</th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
  <td>IPB2 </td>
  <td>illumina Single Cell CRISPR Prep Capture, T10, Box 2 </td>
  <td>放置30min至室温 </td>
</table> 

## Step 11 QC产物清洗（30 min）
### 耗材准备
- IPB2 
- IDTE Buffer 
- 无水乙醇（EtOH） 
- 无核酸酶水（客户自备） 
- 0.2 ml 8-tube strips 
### 试剂预处理与仪器设置
1.  IPB2 涡旋混匀 
2.  每个反应使用无水乙醇配制 400 µL新鲜的 85%乙醇 
### 实验步骤
1.  向每个样本中加入 15 μL 无核酶水，每个样本的总体积为 40 μL。 
2.  加入 32 μL IPB2，使其比例为 0.8X 
3.  吸吹 15 次以混匀 
4.  室温孵育 5 min。 
5.  置于磁力架上 
6.  静置至液体澄清（约 5 min）。 
7.  不要触及磁珠，移除并丢弃所有上清液。 
8.  按如下方法清洗磁珠： 
a. 加入 200 μL 新鲜的 85% 乙醇。 
b. 等待 30 s。 
c. 不要搅动磁珠，移除并丢弃上清。 
9.  重复步骤 8 再次清洗磁珠。 
10. 不要触及磁珠，用 20 μL 移液器吸除残留的乙醇。 
11. 自然风干至珠子表面仍有轻微光泽（约 2 min）。   
根据湿度水平的不同，风干可能需要长达 5 min 的时间。   
<mark><b>注：</b>过度干燥珠子会导致其开裂并降低洗脱效率。</mark> 

12. 从磁力架上取下。 
13. 加入 11 μL IDTE 缓冲液洗脱磁珠。 
14. 吸吹混匀。 
15. 瞬时离心，使液体沉至管底 
注：不要使磁珠沉淀。 
16. 在室温下孵育 5 min。    
<mark><b>注：</b>如果磁珠过度干燥，在孵育过程中应频繁用移液管混匀，以尽量减少样品损失。 </mark>

17. 放入磁力架上 
18. 等待混合液澄清（约 2 min） 
19. 将 10 μL 上清液转移至新的 八连排管中 
## Step 12 QC 产物分析（20 min）
执行以下操作以检查 QC 产物质量。   
QC 产物在 -25°C 至 -15°C 的条件下可稳定保存长达四周。 
### 实验步骤
1.  使用 Qubit 1X dsDNA High Sensitivity 试剂盒对每个样本进行 2 μL 的定量检测。 
2.  使用 Qsep 100 评估平均片段大小。   
上样浓度为 1-2 ng/μL。 
3.  cDNA QC 成功后，进行文库制备。片段分析仪结果图显示（设置为 200 - 5000 bp）， cDNA 的平均片段大小应 ＞ 400 bp。平均大小可能因细胞类型和实验条件而有所不同。 
<img :src="$withBase('/picture/PerturbSeq/009.png')" />

The following image is a representative cDNA trace for a 17,000 human cell input of HEK 293 CRISPRCas9 perturbed cell line on a high sensitivity D5000 ScreenTape. Input material is purified cDNA following cDNA amplification prior to QC
# Stage 3 gRNA Library Prep 
## 直至下一安全停止点前需要的准备工作
1. 取出已完成 cDNA 分离（cDNA isolation）并保存在冰上的 CPIP。 
2. 若 CPIPs 储存于-20℃，冰上溶解	
3.	取出下表试剂	
<table>
  <tr>
  <th colspan="4">2-8℃储存</th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th></th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>PWB1  </td>
    <td>Wash Buffer  </td>
    <td>illumina Single Cell CRISPR Prep, Box 2  </td>
    <td>冰上放置 </td>
  </tr>
  <tr>
  <th colspan="4">-25 - -15℃储存 </th>
  </tr>
  <tr>
    <td>CAPM   </td>
    <td>CRISPR Amp Primer Mix   </td>
    <td>illumina Single Cell CRISPR Prep, Box 3   </td>
    <td>冰上溶解  </td>
  </tr>
  <tr>
    <td>PMM4  </td>
    <td>4X PCR Master Mix  </td>
    <td>illumina Single Cell CRISPR Prep, Box 3   </td>
    <td>冰上放置  </td>
  </tr>
</table> 

## Step 13 清洗 CPIPs 用于 gRNA 扩增 
### 耗材准备
- PWB1 
- 无核酸酶水（自备） 
- 0.5 ml Safe-Lock PCR Clean tubes (emulsion safe) 
- 0.5/1.5 ml combination tube stand (blue) 
### 试剂预处理与仪器设置
1.  CPIP 处理：   
a.  瞬时离心使样品聚集在管底；   
b.  冰上放置   
2.  配制 0.5X PWB1：   
- PWB1（600μL）   
- 无核酶水（600μL）   
- 每个样品准备 1200μL 0.5X PWB1   
3. 按以下步骤将 CPIPs 从 1.5 mL 离心管转移至 0.5 mL 离心管中：   
a.  每个样品标记一个新的 0.5 mL 离心管   
b.  用记号笔在 0.1 ml 刻度处标记   
c.  用 200μL 低残留枪头转移 CPIPs 到 0.5ml 离心管中   
### 实验步骤
1.  按以下步骤清洗 CPIPs   
a.  每个样品加入 450 μL 0.5X PWB1   
b.  涡旋 5s   
c.  离心 1min   
d.  将 CPIP 管放置在管架 0.5 ml 侧，确保管子完全放置在架上   
e.  不要触及 CPIP，弃去管架 A 刻度以上上清   
2.  重复步骤 1 进行二次清洗，使用 350 μL 0.5X PWB1 
3.  重复步骤 1 进行三次清洗，使用 350 μL 0.5X PWB1 
4.  离心 1min 
5.  弃去管上 0.1 ml 刻度以上上清 
6.  样品置于冰上立即准备 gRNA 扩增 
## Step 14 gRNA cDNA 扩增
### 耗材准备
- CAPM 
- PMMA 
- 0.2 ml PCR 8-tube strip 
### 试剂预处理与仪器设置
1.  试剂处理：   
PMM4——吹吸混匀后瞬时离心   
CAPM——吹吸混匀后瞬时离心   
2.  将以下 <mark>gRNA Amplication </mark>程序保存在 PCR 仪上   
Set the lid temperature to 105 ℃   
Set the reaction volume to  135 μL   
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Denaturation</td>
    <td>95℃ </td>
    <td>15 s </td>
  </tr>
  <tr>
    <td rowspan="2">10-14 Cycles </td>
    <td>98℃ </td>
    <td>15 s </td>
  </tr>
  <tr>
    <td>69℃</td>
    <td>1 min </td>
  </tr>
  <tr>
    <td>Final Extension </td>
    <td>72℃ </td>
    <td>5 min </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>4℃ </td>
  </tr>
</table>
最佳循环数需要根据样品调整，<mark>每个样品的产出浓度应该在 1-2 ng/μL </mark>

### 实验步骤
1.  配制 gRNA Amplification Master Mix： 

| Reagent | Volume Per Reaction(μL) | 4.4X Reaction Master Mix(μL) | 8.8X Reaction Master Mix(μL) |
| :-----: | :---------------------: | :--------------------------: | :--------------------------: |
|  PMM4   |          33.8           |             149              |             297              |
|  CAPM   |           1.4           |              6               |              12              |
|  Total  |          35.2           |             155              |             309              |
2.  涡旋 10s，然后瞬时离心 
3.  向每个含 100 μL CPIPs 的样品管中加入 35 μL gRNA Amplification Master Mix   
<b>总体积：135 μL </b>

4.  轻弹管壁混匀样品，然后涡旋 5s 
5.  将 gRNA 反应混合液以每管 68 μL 分装进两个八连排管中 
6.  分装最后一管前瞬时离心混合液，然后转移所有剩余样品 
7.  为每个样品管做好标记 
8.  置于 PCR 仪上运行 gRNA Amplification 程序 
<span style="color: red;"><b>安全停止点：如果您要停止操作样本在 2°C 至 8°C 下保存过夜。</b></span>

## 直至下一安全停止点前需要的准备工作
取出以下试剂： 
<table>
  <tr>
  <th colspan="4">2-8℃储存</th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th></th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>CEB </td>
    <td>cDNA Extraction Buffer </td>
    <td>illumina Single Cell CRISPR Prep, Box 1  </td>
    <td>室温使用  </td>
  </tr>
  <tr>
    <td>IPB2 </td>
    <td>Illumina Purification Beads 2   </td>
    <td>illumina Single Cell CRISPR Prep, Box 1 </td>
    <td>放置 30min 至室温 </td>
  </tr>
</table>

## Step 15 从 CPIPs 分离 gRNA cDNA 
### 耗材准备
- CEB 
- 0.2 ml PCR 8-tube strip 
- 1.5 ml Safe-Lock PCR Clean tubes (emulsion safe)
### 试剂预处理与仪器设置
- CEB——颠倒混匀
### 实验步骤
1.  瞬时离心样品管； 
2.  向每个反应的八联排管中加入 50 μL CEB 
3.  将每个样品的两个反应管 Mix 转移到同一个新 1.5 mL 管中 
4.  将八联排瞬时离心，转移所有残留的液体和 CPIPs 到同一 1.5 mL 管中 
5.  涡旋后瞬时离心 
6.  不要触及沉淀，每个样品转移 100 μL 上清到一个新的 0.2 mL 离心管中 
<mark><b>注：</b>总上清体积 100 μL </mark>

7.  瞬时离心含上清的 0.2 mL 离心管，检查管底是否含 CPIPs 
8.  如果存在剩余的 CPIP，转移上清到新 0.2 ml 离心管中，测量转移上清的体积，从而调整后续gRNA cDNA 清洗过程的磁珠添加量 
## Step 16 gRNA cDNA 清洗（30 min） 
### 耗材准备
-  IPB2 
- 无水乙醇（EtOH） 
- 无核酶水（实验室自备） 
- 0.2 ml 8-tube strips and caps 
### 试剂预处理与仪器设置
1.  IPB2——涡旋 30s 混匀 
2.  每个反应需用无水乙醇和无核酶水配置 400 μL 新鲜的 85%乙醇溶液 
### 实验步骤
1.  对于每 100 μL 的反应体积，加入 100 μL IPB2。   
<b>如有需要，可按 IPB2 体积的 1.0 倍调整磁珠体积。 </b>

2.  吹吸混匀，然后瞬时离心使液体沉至管底 
3.  室温孵育 5 min。 
4.  置于磁力架上，静置 5min 至液体澄清。 
5.  如果 5 min 后磁珠仍未聚集，继续置于磁力架上，直至液体澄清。 
6.  不要搅动磁珠，移除并丢弃上清液。 
7.  按如下方法清洗磁珠：   
a. 加入 200 μL 新鲜的 85% 乙醇。   
b. 等待 30 s。   
c. 不要搅动磁珠，移除并丢弃 200 μL 乙醇。   
8.  重复步骤 7 再次清洗磁珠。 
9.  不要触及磁珠，用 20 μL 移液器吸除残留的乙醇。 
10.  自然风干至珠子表面仍有轻微光泽（约 2 min）。 
根据湿度水平的不同，风干可能需要长达 5 min 的时间。 
<mark><b>注：</b>过度干燥珠子会导致其开裂并降低洗脱效率。</mark> 

11.  从磁力架上取下。 
12.  加入 22 μL IDTE 缓冲液。 
13.  吹洗混匀。 
14.  瞬时离心，使液体聚至管底 
15.  在室温下孵育 5 min。  
注：如果磁珠过度干燥，在孵育过程中应<mark>频繁用移液管混匀</mark>，以尽量减少样品损失。 
16.  放入磁力架上，等待混合液澄清（约 2 min） 
17.  将 20 μL 上清液转移至新的 0.2 ml PCR 管中，<mark>立即置于冰上直至进行 gRNA Library 扩增 </mark>
<span style="color: red;"><b>安全停止点：如果您要停止操作样本请将纯化的gRNA cDNA在 -25°C 至-15°C 下保存，之至多保存7天。</b></span>

## 直至下一安全停止点前需要的准备工作
取出以下试剂按顺序解冻:
<table>
  <tr>
  <th colspan="4">-25--15℃储存 </th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th></th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>PMM4  </td>
    <td>4X PCR Master Mix  </td>
    <td>illumina Single Cell CRISPR Prep, Box 2  </td>
    <td>冰上放置  </td>
  </tr>
  <tr>
    <td>UDIC  </td>
    <td>UDI Mix Strip CRISPR   </td>
    <td>illumina Single Cell CRISPR Prep, Box 3 </td>
    <td>冰上溶解  </td>
  </tr>
</table>

## Step 17  gRNA Library 扩增（1 h）
### 耗材准备
-  PMM4 
-  UDIC 
- 无核酶水（实验室自备） 
### 试剂预处理与仪器设置
1.  PMM4——吹吸 10 次，瞬时离心 
2.  保存以下 PCR 程序：   
Set the lid temperature to 105 ℃   
Set the reaction volume to   μL   
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Denaturation</td>
    <td>98℃ </td>
    <td>45 s </td>
  </tr>
  <tr>
    <td rowspan="3">10-12 Cycles </td>
    <td>98℃ </td>
    <td>15 s </td>
  </tr>
  <tr>
    <td>67℃</td>
    <td>30s </td>
  </tr>
  <tr>
    <td>69℃ </td>
    <td>45s </td>
  </tr>
  <tr>
    <td>Final Extension </td>
    <td>72℃ </td>
    <td>1 min </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>4℃ </td>
  </tr>
</table>
根据样品调整最佳循环数

3. 按以下步骤准备 CRISPR index strip：   
a. 将条带侧面带有 index 的孔的方向与盒盖上的 index 图以及以下图表中的 index 图对齐：  
<img :src="$withBase('/picture/PerturbSeq/010.png')" />
 
b. 为每个样品选择唯一一种 index   
### 实验步骤
1.  使用 Qubit 1X dsDNA High Sensitivity Kit 定量 2 μL 扩增出的样品； 
2.  在 8 联 PCR 管各孔中，分别加入 5–10 ng gRNA cDNA，并用无核酶水补足至 32.5 μL。 
3.  如果由于产量过低导致不足 5 ng，将 5μL   gRNA cDNA 加入到 27.5 μL 无核酶水中，PCR 循
环数至少提升至 11 个循环 
4.  用 20 μL 枪头刺穿 CRISPR UDI 管上封膜 
5.  将以下试剂加入到含 32.5 μL gRNA cDNA 的八联排管中：   
a.  UDIC（5 μL）   
b.  PMM4 （12.5 μL）   
总计 50 μL 每管     
6.  吹吸 10 次后瞬时离心 
7.  在 PCR 仪中运行已设置的程序 
<span style="color: red;"><b>安全停止点：如果您要停止操作, 请将样品在PCR仪中4°C储存或在2-8°C 下保存，至多过夜。</b></span>

## 直至下一安全停止点前需要的准备工作
取出以下试剂 
<table>
  <tr>
  <th colspan="4">-25--15℃储存 </th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th></th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>IPB2  </td>
    <td>Illumina Purification Beads 2  </td>
    <td>illumina Single Cell CRISPR Prep, Box 1   </td>
    <td>放置 30min 至室温  </td>
  </tr>
</table>

## Step 18 gRNA Library 清洗（30 min） 
### 耗材准备
-  IPB2 
-  无水乙醇 
- 无核酶水（实验室自备） 
- IDTE Buffer 
- 0.2 ml 8-tube strips and caps 
### 试剂预处理与仪器设置
1. IPB2——涡旋 30s 以充分混匀 
2. 每个样品准备 400 μL 新鲜 85%乙醇 
### 实验步骤
1.  对于每个 50 μL 样品管，加入 50 μL IPB2，保证磁珠比例 1.0 X 
2.  吹洗 15 次 
3.  如果有磁珠残留在盖子上或管壁，瞬时离心 
4.  室温孵育 5min 
5.  置于磁力架上，静置 5min 至液体澄清。 
如果 5 min 后磁珠仍未聚集，继续置于磁力架上，直至液体澄清。 
6.  不要搅动磁珠，移除并丢弃上清液。 
7.  按如下方法清洗磁珠：   
a. 加入 200 μL 新鲜的 85% 乙醇。   
b. 等待 30 s。   
c. 不要搅动磁珠，移除并丢弃 200 μL 乙醇。   
8.  重复步骤 7 再次清洗磁珠。 
9.  不要触及磁珠，用 20 μL 移液器吸除残留的乙醇。 
10.  自然风干至珠子表面仍有轻微光泽（约 2 min）。 
根据湿度水平的不同，风干可能需要长达 5 min 的时间。 
<mark><b>注：</b>过度干燥珠子会导致其开裂并降低洗脱效率。 </mark>
11.  从磁力架上取下。 
12.  加入 21 μL IDTE 缓冲液。 
13.  吹洗 10 次混匀，瞬时离心，使液体聚至管底 
14.  在室温下孵育 5 min。  
<b>注：</b>如果磁珠过度干燥，在孵育过程中应<mark>频繁用移液管混匀</mark>，以尽量减少样品损失。 
15.  有需要的话再次瞬时离心 
16.  放入磁力架上，等待混合液澄清（约 2 min） 
17.  将 20 μL 上清液转移至新的 0.2 ml PCR 管中   
<mark>本上清即为送测的 gRNA 文库 </mark>
<span style="color: red;"><b>安全停止点：如果您要停止操作, 请将纯化的gRNA文库在-25-15°C 下保存，至多14天。</b></span>

## 直至下一安全停止点前需要的准备工作
1. 如果你从安全停止点后开始， 将 cDNA 取出并置于冰上 
<mark>文库制备需要用从 cDNA 纯化步骤得到的全部 40 μL cDNA</mark>，而不是 QC 产物 

2. 取出以下试剂按顺序解冻： 
<table>
  <tr>
  <th colspan="4">2-8℃储存  </th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th></th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>IPB2   </td>
    <td></td>
    <td>illumina Single Cell Library Prep, Box 1   </td>
    <td>放置 30min 至室温   </td>
  </tr>
  <tr>
    <td>NFW </td>
    <td>Nuclease-free water    </td>
    <td>illumina Single Cell Library Prep, Box 1 </td>
    <td>室温使用 </td>
  </tr>
  <tr>
  <th colspan="4">-25 - -15℃储存  </th>
  </tr>
  <tr>
    <td>PMM4 </td>
    <td>4X PCR Master Mix  </td>
    <td>illumina Single Cell Library Prep, Box 2 </td>
    <td>冰上放置 </td>
  </tr>
  <tr>
    <td>LAM </td>
    <td>Library Adapter Mix </td>
    <td>illumina Single Cell Library Prep, Box 2 </td>
    <td>冰上溶解 </td>
  </tr>
  <tr>
    <td>LPB </td>
    <td>Library Prep Buffer </td>
    <td>illumina Single Cell Library Prep, Box 2 </td>
    <td>冰上溶解 </td>
  </tr>
  <tr>
    <td>LPE </td>
    <td>Library Prep Enzymes </td>
    <td>illumina Single Cell Library Prep, Box 2 </td>
    <td>冰上溶解 </td>
  </tr>
  <tr>
    <td>LPMA </td>
    <td>Library Prep Mix A </td>
    <td>illumina Single Cell Library Prep, Box 2 </td>
    <td>冰上溶解 </td>
  </tr>
</table>

1. 解冻 index 
<table>
  <tr>
  <th colspan="3">-25- -15℃储存  </th>
  </tr>
  <tr>
    <th></th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>illumina Single Cell Prep UDI Mix Strip </td>
    <td>illumina Single Cell Library Prep, Box 2  </td>
    <td>冰上溶解  </td>
  </tr>
  <tr>
    <td>illumina Single Cell Unique Dual Indexes Plate  </td>
    <td>illumina Single Cell Unique Dual Indexes(96 Indexes, 96 Samples) </td>
    <td>冰上溶解 </td>
  </tr>
</table>

# Stage 4:GEX Library Prep 
## Step 19 片段化、末端修复与 A 尾添加（FEA）（50 min） 
### 耗材准备
-  LPB(Library Prep Buffer) 
-  LPE(Library Prep Enzymes) 
### 试剂预处理与仪器设置
1.  LPB——涡旋混匀，瞬时离心，置于冰上保存 
2.  LPE——吹洗混匀，瞬时离心，置于冰上保存 
3.  保存 <mark>cDNA Fragmentation </mark>程序在 PCR 仪中：   
Set the lid temperature to 105 ℃   
Set the reaction volume to ？    
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td>Hold</td>
    <td>4℃  </td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td>30℃  </td>
    <td>6min </td>
  </tr>
  <tr>
    <td></td>
    <td>67℃</td>
    <td>30s </td>
  </tr>
  <tr>
    <td>65℃ </td>
    <td>30min </td>
  </tr>
  <tr>
    <td>Hold </td>
    <td>4℃ </td>
    <td></td>
  </tr>
</table>

4.  运行 cDNA Fragmentation 程序，<mark>将 PCR 仪先预冷至 4℃</mark>，盖子预热至 105℃ 
### 实验步骤
1.  按以下体积混合制备 Library Prep Master Mix。 

| Reagent | Volume Per Reaction(μL) | 4.4X Reaction Master Mix(μL) | 8.8X Reaction Master Mix(μL) |
| :-----: | :---------------------: | :--------------------------: | :--------------------------: |
|   LPB   |            4            |             17.6             |             35.2             |
|   LPE   |            6            |             26.4             |             52.8             |
|  Total  |           10            |              44              |              88              |
2.  涡旋混匀，瞬时离心 
3.  向每个含有 40 μL cDNA 的管中加入 10 μL Library Prep Master Mix。   
总体积为 50 μL。 
4.  吸吹 10 次混匀，然后瞬时离心。   
每次吸吹 25 μL，一定要充分混匀。 
5.  将样本置于冰上。 
6.  将样本置于预冷的 PCR 仪上， 
7.  点“Skip”运行 cDNA Fragmentation 程序的后续步骤。 
8.  当热循环仪程序达到 4°C 时，<mark>立即取出样本</mark>，然后进行下一步操作。 
## Step 20 Adapter 连接（30 min）
### 耗材准备
-  LAM(Library Adapter Mix) 
-  LPMA(Library Prep Mix A) 
-  NFW（Nuclease-Free Water, 试剂盒提供） 
### 试剂预处理与仪器设置
1.  LPMA   
a.  缓慢吹打 15 次混匀，瞬时离心；   
b.  置于冰上保存   
2.  LAM   
a.  涡旋混匀   
b.  瞬时离心   
3.  保存以下 Ligation 程序于 PCR 仪中： 
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td></td>
    <td>20℃ </td>
    <td>20min</td>
  </tr>
</table>
<mark>确保热盖是关闭的 </mark>

### 实验步骤
1.  制备稀释的 Library Adapter Mix：   
若处理多个样本，请将每种体积乘以样本数量，并增加 10% 的余量。 
-  LAM（0.75 μL） 
-  NFW（4.25 μL）   
每份样本 5 μL 
<mark><b>注：</b>Library Adapter Mix 稀释液在 -25°C 至 -15°C 下可保存长达一周。 </mark>

2.  向每个反应管中加入 5 μL 稀释的 LAM 
3.  向每个反应体系中加入 20 μL LPMA   
总体积：75 μL 
4.  吹吸 10 次混匀，然后瞬时离心 
5.  将其放入热循环仪中 
6.  运行 Ligation 程序。 
7.  当 PCR 程序完成后，<b>立即进行连接产物的清洗</b> 
## Step 21 清洗连接产物（20 min）
此步骤使用磁珠来纯化接头连接的片段。 
### 耗材准备
- IPB2 
- NFW（试剂盒提供） 
- 无水乙醇（EtOH） 
- 0.2 ml PCR 8-tube strip 
### 试剂预处理与仪器设置
1.  IPB2——涡旋 30s 以充分混匀 
2.  每个反应需用无水乙醇配置 400 µL新鲜的 85%乙醇溶液 
### 实验步骤
1.  向每个样本管中加入 60 μL IPB2。 
2.  吸吹 15 次以混合（移液器调至 125 μL ） 
3.  室温孵育 5 min。 
4.  将其置于磁力架上 
5.  静置至液体澄清（约 5 min） 
6.  不要搅动磁珠，将每管中的所有上清液移除并丢弃。 
7.  按如下方法清洗磁珠。   
a.  加入 200 μL 新鲜的 85% 乙醇。   
b.  等待 30 s。   
c.  不要搅动磁珠，移除所有上清液。   
8.  重复步骤 7 进行二次清洁 
9.  不要搅动磁珠，用 20 μL 移液器吸除残留的乙醇。 
10. 自然风干至珠子表面仍有轻微光泽（约 2 min） 
根据湿度水平的不同，风干可能需要 长达 5 min 的时间。   
<mark><b>注：</b>过度干燥珠子会导致其出现裂纹并降低洗脱效率。</mark> 

11. 从磁力架上取下。 
12. 向管内的磁珠沉淀中加入 34 μL NFW 
13. 吸吹 10 次混匀（移液器调至 32.5 μL） 
14. 室温孵育 5 min。 
15. 置于磁力架上 
16. 静置至液体澄清（约 2 min） 
17. 转移 32.5 μL 上清液至新的 0.2 ml PCR 管中。 

## Step 22 文库扩增与 UDI 标记（1 hr） 
### 耗材准备
- PMM4 
- 以下 index 选项之一：   
  - Illumina Single Cell Prep UDI Mix Strip 
  - Illumina Single Cell Unique Dual Indexes plate 
  - 本试剂盒提供 8 种不同的 index 组合，对于超出 8 个文库的实验请使用 Illumina Single Cell 
  - Unique Dual Indexes plate 
### 试剂预处理与仪器设置
1.  PMM4——吹吸 10 次，然后瞬时离心 
2.  PCR 仪上保存以下程序：   
Set the lid temperature to 105℃   
Set the reaction volume to ？   
<table border="1">
  <tr>
    <th>STEP</th>
    <th>TEMP</th>
    <th>TIME</th>
  </tr>
  <tr>
    <td></td>
    <td>98℃  </td>
    <td>45s</td>
  </tr>
  <tr>
    <td rowspan="3">X Cycles of </td>
    <td>98℃   </td>
    <td>15s </td>
  </tr>
  <tr>
    <td></td>
    <td>67℃</td>
    <td>30s </td>
  </tr>
  <tr>
    <td>69℃  </td>
    <td>45s  </td>
  </tr>
  <tr>
    <td></td>
    <td>72℃ </td>
    <td>1min </td>
  </tr>
  <tr>
    <td></td>
    <td>4℃ </td>
    <td></td>
  </tr>
</table>

| Sample Input                                       | Number of PCR Cycles(X) |
| -------------------------------------------------- | ----------------------- |
| High RNA sample types(eg, cell lines)              | 10                      |
| Low RNA sample types(eg, primary cells and nuclei) | 15                      |

<span style="color: red;">设置时注意循环数-1</span>  
若 cDNA 浓度>200 ng/μL 则需要降低 1-2 循环数 

3. 按以下操作准备 index 管 
a. 将条带侧面带有 index 的孔的方向与盒盖上的 index 图以及以下图表中的 index 图对齐   
<img :src="$withBase('/picture/PerturbSeq/011.png')" />

b. 为每个样品选择唯一一种 index     
### 实验步骤
1.  用 20 μL 枪头刺穿 UDI 管上封膜 
2.  将以下试剂加入到含 32.5 μL cDNA 的八联排管中：   
a.  Unique Library Index Mix（5 μL）   
b.  PMM4 （12.5 μL）   
总计 50 μL 每管     
3.  吹吸 10 次后瞬时离心 
4.  将样品置于 PCR 仪中 
5.  运行已设置的程序 
<span style="color: red;"><b>安全停止点：如果您要停止操作，请将样本置于 4°C 的PCR仪中，或者将样本在 2°C 至 8°C 下保存过夜。</b></span>

## 直至下一安全停止点前需要的准备工作
解冻试剂： 
<table>
  <tr>
  <th colspan="3">2-8℃储存  </th>
  </tr>
  <tr>
    <th>Reagent</th>
    <th>Box Name  </th>
    <th>解冻方法  </th>
  </tr>
  <tr>
    <td>IPB2   </td>
    <td>illumina Single Cell Library Prep, Box 1   </td>
    <td>放置 30min 至室温   </td>
  </tr>
</table>

## Step 23 文库清洗（30 min）
### 耗材准备
- IPB2 
- IDTE Buffer 
- 无水乙醇（EtOH） 
- NFW 
- 0.2 ml PCR 8-tube strip 
### 试剂预处理与仪器设置
1.  IPB2—涡旋 30s 充分混匀。 
2.  对于每个反应，使用无水乙醇配制 400 μL 新鲜的 85% 乙醇溶液。 
### 实验步骤
1.  如果从安全停止点重新开始，将样品管瞬时离心。 
2.  加入 45 μL NFW。 
3.  对于 95 μL 的样品体积，加入 76 μL IPB2。   
如有需要，调整磁珠体积为 0.8 倍。 
4.  吸吹 15 次以混匀（移液器调至 160 μL ） 
5.  如果磁珠残留在管盖或管壁上，瞬时离心。 
6.  室温孵育 5 min。 
7.  将其置于磁力架上 
8.  静置至液体澄清（约 5 min）。 
9.  不要触及磁珠，将每管中的所有上清液移除并丢弃。 
10. 按如下方法清洗珠子。   
a.  加入 200 μL 新鲜的 85% 乙醇。   
b.  等待 30 s。   
c.  不要搅动磁珠，移除并丢弃乙醇。   
11. 重复步骤 10 进行二次清洁。 
12. 不要触及磁珠，用 20 μL 移液器吸除残留的乙醇。 
13. 自然风干至珠子表面仍有轻微光泽（约 2 min）。 
根据湿度的不同，自然风干可能需要 长达 5 min。    
<mark><b>注：</b>过度干燥珠子会导致其开裂并降低洗脱效率。 </mark>
14. 从磁力架上取下。 
15. 加入 21 μL IDTE 缓冲液。 
16. 用 20 μL 的移液器吸吹 10 次以重悬。 
17. 室温孵育 5 min。 
18. 置于磁力架上，静置至液体澄清（约 2 min）。 
19. 将 20 μL 上清液转移至新的 0.2 ml PCR 管中。 
<span style="color: red;"><b>安全停止点：如果停止操作请密封管子并在 -25°C 至 -15°C 的条件下保存，最长可保存 30 天。</b></span>

## Step 24  文库检查（25 min） 
这一步骤会检测最终文库的浓度和质量。
### 实验步骤
1. 使用 Qubit 1X dsDNA High Sensitivity Assay Kit 试剂盒对每个样本进行 2 μL 的定量检测。 
2. 使用 Qsep 100 评估文库平均片段大小，上样浓度为 1-2 ng/μL。   
<mark>mRNA Library（GEX Library）预期大小 400-600bp</mark>   
The following image is a representative mRNA library trace for a 17,000 human cell input of HEK 293. CRISPR-Cas9 perturbed cell line on a high sensitivity D1000 ScreenTape. Expected average size is 400–600 bp  
<img :src="$withBase('/picture/PerturbSeq/012.png')" />
 
<mark>gRNA Library 预期大小 260-300bp</mark>   
The following image is a representative gRNA library trace for a 17,000 human cell input of HEK 293 CRISPR-Cas9 perturbed cell line on a high sensitivity D1000 ScreenTape. Size varies depending on the structure of the gRNA vector, but expected average size is typically 260–300 bp. 
<img :src="$withBase('/picture/PerturbSeq/013.png')" />


<b>文库混合与稀释</b>

1.	根据gRNA Library，mRNA Library Qbit值（ng/μL），Qseq数据（片段大小bp）换算单位
<img :src="$withBase('/picture/PerturbSeq/014.png')" />

2.	根据两个文库的Molarity将mRNA Library与gRNA Library按9:1混合后送测   
推荐测序深度：  
mRNA Library：20000 reads/target cell  
gRNA Library：5000 reads/target cell（1 guide/cell）  

<b>CRISPR Library Index Sequences</b>
| Well | i7         | Bases in Adapter | i7 Bases for Sample Sheet | i5 Bases in Adapter	i5 Bases for Sample Sheet in Forward Orientation | i5 Bases for Sample Sheet in Reverse Compliment Orientation |
| ---- | ---------- | ---------------- | ------------------------- | -------------------------------------------------------------------- | ----------------------------------------------------------- |
| 1    | CTGACCGGCA | TGCCGGTCAG       | CCTGATACAA                | CCTGATACAA                                                           | TTGTATCAGG                                                  |
| 2    | GAATTGAGTG | CACTCAATTC       | TTAAGTTGTG                | TTAAGTTGTG                                                           | CACAACTTAA                                                  |
| 3    | GCGTGTGAGA | TCTCACACGC       | CGGACAGTGA                | CGGACAGTGA                                                           | TCACTGTCCG                                                  |
| 4    | TCTCCATTGA | TCAATGGAGA       | GCACTACAAC                | GCACTACAAC                                                           | GTTGTAGTGC                                                  |
| 5    | ACATGCATAT | ATATGCATGT       | TGGTGCCTGG                | TGGTGCCTGG                                                           | CCAGGCACCA                                                  |
| 6    | TTGAAGCTAG | CTAGCTTCAA       | TGTGTAAGCT                | TGTGTAAGCT                                                           | AGCTTACACA                                                  |
| 7    | ACATAACGGA | TCCGTTATGT       | TTGTAGTGTA                | TTGTAGTGTA                                                           | TACACTACAA                                                  |
| 8    | TTAATAGACC | GGTCTATTAA       | CAACGACACG                | CAACGACACG                                                           | CGTGTCGTTG                                                  |

