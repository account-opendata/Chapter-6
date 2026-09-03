## Chapter-6
第六章算例中涉及的数据

# 概述
本项目是博士论文 《智能配电网产消者能量共享优化方法研究》-“ 第六章 基于私桩共享的非网络依赖优化方法” 中案例研究参数的说明文档。

> _**Toy Case（测试案例）**_：测试案例中 PCPS（私人充电桩共享）匹配与基于 PCPS 的能源共享问题的参数，包含 4 个家庭。  
> _**ShenZhen Case（深圳案例）**_：深圳案例中 PCPS 匹配与基于 PCPS 的能源共享问题的参数，包含 1615 个家庭。

<div align="center">
  <img src = "Schematic diagram of Cases.png" width="800" height="380">
</div> 
图1. 案例示意图。（深圳案例中，红点代表私人充电桩 PCP，蓝点代表电动汽车 EV）

# 参数说明 (Parameters Description)
每个案例的参数分别记录在 **六个** Excel 文件中，包括 ***PCPParameters.xlsx***、***EVParameters.xlsx***、***HouseholdParameters.xlsx***、***HouseholdLoad.xlsx***、***HouseholdPV.xlsx*** 以及 ***TOU&FIT.xlsx***。

## PCPParameters.xlsx
该文件包含每个私人充电桩（PCP）的所有参数，其中：

>_**'PCP_Index'**_ : 每个 PCP 的索引；  
>_**'Household_index'**_ : 与 PCP 关联的家庭索引；  
>_**'T_ksta'**_ : PCP 的可用开始时间；  
>_**'T_kend'**_ : PCP 的可用结束时间；  
>_**'P_powermax'**_ : PCP 的最大充/放电功率；  
>_**'p_sermin'**_ : PCP 每千瓦时可接受的最低服务费；  
>_**'x and y'**_ : PCP 的位置坐标；  

## EVParameters.xlsx
该文件包含每辆电动汽车（EV）的所有参数，其中：

>_**'EV_Index'**_ : 每辆 EV 的索引；  
>_**'Household_index'**_ : 与 EV 关联的家庭索引；  
>_**'t_arp'**_ : EV 到达 PCP 的时间；  
>_**'t_lep'**_ : EV 离开 PCP 的时间；  
>_**'t_arh'**_ : EV 到家的时间；  
>_**'t_leh'**_ : EV 离家的时间；  
>_**'EEVexp'**_ : EV 在匹配的 PCP 处的期望充电量；  
>_**'p_serHmax'**_ : EV 每千瓦时可接受的最高服务费；  
>_**'x and y'**_ : EV 的位置坐标；  
>_**'ItaEV'**_ : EV 的充放电效率；  
>_**'aEV, bEV and cEV'**_ : EV 的放电退化（损耗）成本系数；  
>_**'EEVarh'**_ : EV 到家时的初始电量；  
>_**'EEVlehmin'**_ : EV 离家时的最低电量要求；  
>_**'EEVtra'**_ : EV 在 _**'t_leh'**_ 到 _**'t_arp'**_ 期间（行驶过程）的耗电量；  
>_**'EEVup'**_ : EV 的最大电池容量；  
>_**'EEVlow'**_ : EV 的最小电池容量。  


## HouseholdParameters.xlsx
该文件包含每个家庭的微型发电机组（TG）和储能（ES）参数，其中：

>_**'Household_index'**_ : 每个家庭的索引；  
>_**'aTG, bTG, and cTG'**_ : TG 的二次、一次和常数成本系数；  
>_**'PTGup'**_ : TG 的最大功率限制；  
>_**'PTGlow'**_ : TG 的最小功率限制；  
>_**'PTGraup'**_ : TG 的最大向下爬坡速率；  
>_**'PTGralow'**_ : TG 的最大向上爬坡速率；  
>_**'aES, bES, cES'**_ : ES 的充放电退化（损耗）成本系数；  
>_**'ItaES'**_ : ES 的充放电效率；  
>_**'PESup'**_ : ES的最大充放电功率限制；
>_**'EESup'**_ : ES 的最大电量（容量）限制；  
>_**'EESlow'**_ : ES 的最小电量（容量）限制；  
>_**'EESinit'**_ : ES 的初始电量；

特别地，当家庭不包含相关资源时，相应的参数为空。

## HouseholdLoad.xlsx

该文件包含家庭的电力负荷需求数据，其中每一列代表一个家庭。 

## HouseholdPV.xlsx

该文件包含家庭的光伏发电数据，其中每一列代表一个家庭。 

## TOU&FIT.xlsx

该文件包含向上层电网的购电价格和售电价格。
