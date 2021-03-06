！！各种缩写的意思:
Impact: 效果总称
DI: 一次性效果
IOT: 多次发作的效果
SOT: 在一段时间内一直生效的效果
DS: 伤害盾性质的效果

！！规范：
百分比用0~100之间的整数表达
时间单位是毫秒
整数型用0表示无效（即没有用到这个域），正数表示增加，负数表示减少
布尔型用-1表示无效（即没有用到这个域），0表示非，1表示真
特定的ID用-1表示无效（即没有用到这个域），非负数表示一个有效的ID

逻辑列表：
-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_000
逻辑ID: 0
文件: StdImpact000.h, StdImpact000.cpp
类型：DI
功能说明：只是显示一次性特效用
数据域说明：|无

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_001
逻辑ID: 1
文件: StdImpact001.h, StdImpact001.cpp
类型：DI
功能说明：无类型的一次性伤害（值伤害）
数据域说明：|伤害数值|无。。。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_002
逻辑ID: 2
文件: StdImpact001.h, StdImpact001.cpp
类型：DI
功能说明：无类型的一次性伤害（HP百分率伤害）
数据域说明：|伤害百分率|无。。。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_003
逻辑ID: 3
文件: StdImpact003.h, StdImpact003.cpp
类型：DI
功能说明：六种类型的一次性伤害
数据域说明：|物理伤害|魔法伤害|冰系伤害|火系伤害|电系伤害|毒系伤害|无。。。
注：攻击力加成的技能用这个效果。具体填法：
如果是物理攻击力加成---->填写“物理伤害域”， 其他域填0；
如果是魔法攻击力加成---->填写“魔法伤害域”， 其他域填0；
如果是冰系攻击力加成---->填写“冰系伤害域”， 其他域填0；
如果是火系攻击力加成---->填写“火系伤害域”， 其他域填0；
如果是电系攻击力加成---->填写“电系伤害域”， 其他域填0；
如果是毒系攻击力加成---->填写“毒系伤害域”， 其他域填0；
然后再技能里面填写这个效果的索引就可以了。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_004
逻辑ID: 4
文件: StdImpact004.h, StdImpact004.cpp
类型：DI
功能说明：HP,MP,Rage, StrikePoint的一次性修改
数据域说明：|HP修改量|MP修改量|Rage修改量|StrikePoint修改量|无。。。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_005
逻辑ID: 5
文件: StdImpact005.h, StdImpact005.cpp
类型：DI
功能说明：HP,MP,Rage, StrikePoint的一次性百分率修改
数据域说明：|HP修改百分率|MP修改百分率|Rage修改百分率|StrikePoint修改百分率|无。。。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_006
逻辑ID: 6
文件: StdImpact006.h, StdImpact006.cpp
类型：DI
功能说明：宠物的HP,Happiness的一次性值修改
数据域说明：|HP修改量|Happiness修改量|无。。。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_007
逻辑ID: 7
文件: StdImpact007.h, StdImpact007.cpp
类型：DI
功能说明：宠物的HP,Happiness的一次性百分率修改
数据域说明：|HP修改百分率|Happiness修改百分率|无。。。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_008
逻辑ID: 8
文件: StdImpact008.h, StdImpact008.cpp
类型：DI
功能说明：强制怪物攻击施法者， 或强制怪物回避施法者，只对怪物有效；
数据域说明：|攻击还是回避；0：回避，1：攻击。|无。。。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_009
逻辑ID: 9
文件: StdImpact009.h, StdImpact009.cpp
类型：DI
功能说明：传送角色到指定位置
数据域说明：|场景ID|X坐标|Z坐标|无。。。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_010
逻辑ID: 10
文件: StdImpact010.h, StdImpact010.cpp
类型：IOT, 间隔发作驻留效果
功能说明：每个时间间隔将所有子效果发给效果所有者
数据域说明：|子效果1数据索引|子效果2数据索引|。。。|子效果15数据索引|子效果16数据索引|无。。。， 一共可以填16个子效果，不用的子效果域请填-1。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_011
逻辑ID: 11
文件: StdImpact011.h, StdImpact011.cpp
类型：SOT, 驻留效果
功能说明：在驻留期间，所有者的2级属性（所有攻击，所有防御，HP,MP,Rage, StrikePoint的最大值）会得到修整
数据域说明：|物理攻击修正|物理防御修正|魔法攻击修正|魔法防御修正|冰系攻击修正|冰系抗性修正|火系攻击修正|火系抗性修正|电系攻击修正|电系抗性修正|毒系攻击修正|毒系抗性修正|MAX_HP修正|MAX_MP修正|MAX_RAGE修正|MAX_STRIKE_POINT修正||无。。。， 注: 不需要修正的请填0。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_012
逻辑ID: 12
文件: StdImpact012.h, StdImpact012.cpp
类型：SOT, 驻留效果
功能说明：在驻留期间，所有者的2级属性（所有攻击，所有防御，HP,MP,Rage, StrikePoint的最大值）会得到百分率修整
数据域说明：|物理攻击修正率|物理防御修正率|魔法攻击修正率|魔法防御修正率|冰系攻击修正率|冰系抗性修正率|火系攻击修正率|火系抗性修正率|电系攻击修正率|电系抗性修正率|毒系攻击修正率|毒系抗性修正率|MAX_HP修正率|MAX_MP修正率|MAX_RAGE修正率|MAX_STRIKE_POINT修正率||无。。。， 注: 不需要修正率的请填0。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_013
逻辑ID: 13
文件: StdImpact013.h, StdImpact013.cpp
类型：SOT, 驻留效果
功能说明：在驻留期间，所有者的2级属性（命中，闪避，会心）会得到修正
数据域说明：|命中修正|闪避修正|会心修正|无。。。， 注: 不需要修正的请填0。

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_014
逻辑ID: 14
文件: StdImpact014.h, StdImpact014.cpp
类型：SOT, 驻留效果
功能说明：在驻留期间，效果所有者的控制标记（可否使用技能、可否移动、无敌否）会得到修正
数据域说明：|可否使用任何技能（CanAction1标记，-1为无效）|可否使用任何技能（CanAction2标记,-1为无效）|可否移动（CanMove标记,-1为无效）|无敌否（Unbreakable标记,-1为无效）|移动速度修正%（0为无效）|隐身级别修正（0为无效）|反隐级别修正（0为无效）|变身ID(-1为无效)|骑乘ID(-1为无效)|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_015
逻辑ID: 15
文件: StdImpact015.h, StdImpact015.cpp
类型：SOT, 驻留效果
功能说明：在驻留期间，值修正效果所有者Str, Con, Spr, Int, Dex
数据域说明：|STR修正(0为无效)|Con修正(0为无效)|SPR修正(0为无效)|INT修正(0为无效)|DEX修正(0为无效)|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_016
逻辑ID: 16
文件: StdImpact016.h, StdImpact016.cpp
类型：SOT, 驻留效果
功能说明：在驻留期间，百分比修正效果所有者Str, Con, Spr, Int, Dex
数据域说明：|STR修正%(0为无效)|Con修正%(0为无效)|SPR修正%(0为无效)|INT修正%(0为无效)|DEX修正%(0为无效)|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_017
逻辑ID: 17
文件: StdImpact017.h, StdImpact017.cpp
类型：SOT, 驻留效果
功能说明：在驻留期间，免疫特定集合内的级别低于免疫级别的效果
数据域说明：|免疫级别|免疫集合1|免疫集合2|免疫集合3|免疫集合4|免疫集合5|免疫集合6|免疫集合7|免疫集合8|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_018
逻辑ID: 18
文件: StdImpact018.h, StdImpact018.cpp
类型：DI, 非驻留效果，瞬发生效
功能说明：驱散特定集合内的级别低于驱散级别的效果
数据域说明：|驱散级别|驱散个数|驱散集合1|驱散集合2|驱散集合3|驱散集合4|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_019
逻辑ID: 19
文件: StdImpact019.h, StdImpact019.cpp
类型：SOT, 驻留效果
功能说明：在一段时间内修正后发出的效果的威力和持续时间
数据域说明：|激活次数，-1是无限次|目标效果集合ID|威力修正率|持续时间修正率|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_020
逻辑ID: 20
文件: StdImpact020.h, StdImpact020.cpp
类型：SOT, 驻留效果
功能说明：角色死亡后可以有一次原地复活的机会
数据域说明：|复活后的HP%|复活后的MP%|复活后的Rage%|无。。。， 

------------------------------------------------------------------------------------- 
效果逻辑：STD_IMPACT_021 
逻辑ID: 21 
文件: StdImpact021.h, StdImpact021.cpp 
类型：SOT, 驻留效果 
功能说明：强化特定的技能 
注：命中和会心修正是直接替换原有的命中和会心。 
数据域说明：|生效次数，无效值：-1 
			|目标技能集合ID, 无效值：-1
			|命中修正，无效值：0
			|会心修正率，无效值：0
			|威力值修正，无效值: 0
			|威力%修正，无效值: 0
			|消耗值修正，无效值: 0
			|消耗%修正，无效值: 0
			|效果或陷阱的时间值修正，无效值: 0
			|效果或陷阱的时间%修正，无效值: 0
			|冷却值修正，无效值: 0
			|冷却%修正，无效值: 0
			|聚气时间值修正，无效值: 0
			|聚气时间%修正，无效值: 0
			|引导时间值修正，无效值: 0
			|引导时间%修正，无效值: 0 
			
-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_022
逻辑ID: 22
文件: StdImpact022.h, StdImpact022.cpp
类型：SOT, 驻留效果
功能说明：宠物的复仇效果
数据域说明：|生效几率|反击次数|伤害反弹率|吸血效率|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_023
逻辑ID: 23
文件: StdImpact023.h, StdImpact023.cpp
类型：SOT, 驻留效果，瞬发生效
功能说明：宠物的防御效果
数据域说明：|生效几率|伤害免疫率|吸魔效率|驱散怒气效率|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_024
逻辑ID: 24
文件: StdImpact024.h, StdImpact024.cpp
类型：SOT, 驻留效果
功能说明：宠物的护主技能(一定几率免疫特定的效果)
数据域说明：|生效几率|可以免疫的效果集合1|可以免疫的效果集合2|可以免疫的效果集合3|可以免疫的效果集合4|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_025
逻辑ID: 25
文件: StdImpact025.h, StdImpact025.cpp
类型：SOT, 驻留效果
功能说明：宠物的护主技能(一定几率抵消致命一击)
数据域说明：|生效几率|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_026
逻辑ID: 26
文件: StdImpact026.h, StdImpact026.cpp
类型：DS, 驻留效果, 伤害盾
功能说明：伤害盾, 吸收,免疫,反弹
数据域说明：|盾的生命|吸收率|免疫率|反射率|反射发生几率|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_027
逻辑ID: 27
文件: StdImpact027.h, StdImpact027.cpp
类型：DS, 驻留效果, 伤害盾
功能说明：伤害盾, 将对主人的一部分伤害转移到宠物身上
数据域说明：|伤害转移率|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_028
逻辑ID: 28
文件: StdImpact028.h, StdImpact028.cpp
类型：DS, 驻留效果, 伤害盾
功能说明：伤害盾, 宠物特性盾, 修正率>0表示此项伤害将被放大，修正率<0表示此项伤害被吸收并转换成生命。
数据域说明：|冰系伤害修正%|火系伤害修正%|电系伤害修正%|毒系伤害修正%|无...


-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_029
逻辑ID: 29
文件: StdImpact029.h, StdImpact029.cpp
类型：DS, 驻留效果, 伤害盾
功能说明：伤害盾, 峨嵋技能虚冲养气的效果
数据域说明：|护体生命值|伤害吸收率|消耗修正的目标技能集合|消耗修正率|聚气时间修正的目标技能集合|聚气时间修正率|消散产生的怒气值|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_030
逻辑ID: 30
文件: StdImpact030.h, StdImpact030.cpp
类型：DS, 驻留效果, 伤害盾
功能说明：伤害盾, 峨嵋技能易筋锻骨的效果
数据域说明：|护体生命值|伤害吸收率|修正的目标效果集合ID|效果修正率|自爆扫描半径|作用对象数目|自爆效果索引|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_031
逻辑ID: 31
文件: StdImpact031.h, StdImpact031.cpp
类型：DS, 驻留效果, 伤害盾
功能说明：伤害盾, 武当虎抱头
数据域说明：|伤害吸收几率|伤害反射比率|物理防御修正|魔法防御修正|冰系防御修正|火系防御修正|电系防御修正|毒系防御修正|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_032
逻辑ID: 32
文件: StdImpact032.h, StdImpact032.cpp
类型：DS, 驻留效果, 伤害盾
功能说明：伤害盾, 
数据域说明：|迟缓发作几率|迟缓效果数据索引|迟缓发作的冷却时间|自爆扫描半径|作用对象数目|冰封效果数据索引|物理防御修正|魔法防御修正|冰系防御修正|火系防御修正|电系防御修正|毒系防御修正|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_033
逻辑ID: 33
文件: StdImpact033.h, StdImpact033.cpp
类型：SOT, 驻留效果
功能说明：策反怪物, 
数据域说明：|策反后怪物AI类型|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_034
逻辑ID: 34
文件: StdImpact034.h, StdImpact034.cpp
类型：SOT, 驻留效果
功能说明：死后自爆buff, 
数据域说明：|自爆扫描半径|作用对象数目|自爆效果数据索引|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_035
逻辑ID: 35
文件: StdImpact035.h, StdImpact035.cpp
类型：SOT, 驻留效果
功能说明：恐惧, 不能使用技能 
数据域说明：|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_036
逻辑ID: 36
文件: StdImpact036.h, StdImpact036.cpp
类型：SOT, 驻留效果
功能说明：探测陷阱
数据域说明：|探隐级别修正|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_037
逻辑ID: 37
文件: StdImpact037.h, StdImpact037.cpp
类型：SOT, 驻留效果
功能说明：恐惧, 不能使用技能 
数据域说明：|激活次数，-1是无限次|目标效果集合ID|峨嵋护体HP修正率%|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_038
逻辑ID: 38
文件: StdImpact038.h, StdImpact038.cpp
类型：SOT, 驻留效果
功能说明：持续性特效，没有真正的效果
数据域说明：|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_039
逻辑ID: 39
文件: StdImpact039.h, StdImpact039.cpp
类型：SOT, 驻留效果
功能说明：少林铁布衫：会心率增加，怒气产生率增加
数据域说明：|会心率修正|怒气产生率修正%|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_040
逻辑ID: 40
文件: StdImpact040.h, StdImpact040.cpp
类型：SOT, 驻留效果
功能说明：少林一苇渡江的效果，移动速度增加，和下次打击带有子效果
数据域说明：|生效次数|移动速度修正%|子效果数据索引|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_041
逻辑ID: 41
文件: StdImpact041.h, StdImpact041.cpp
类型：SOT, 驻留效果
功能说明：明教五星连珠
数据域说明：|物理攻击修正|物理防御修正|魔法攻击修正|魔法防御修正|怒气增量修正%（0%为不长怒气）|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_042
逻辑ID: 42
文件: StdImpact042.h, StdImpact042.cpp
类型：SOT, 驻留效果
功能说明：明教七星落长空
数据域说明：|攻击速度修正|会心率修正|免疫效果集合1|免疫效果集合2无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_043
逻辑ID: 43
文件: StdImpact043.h, StdImpact043.cpp
类型：SOT, 驻留效果
功能说明：明教怒发冲冠
数据域说明：|怒气增长修正|冰抗修正|火抗修正|电抗修正|毒抗修正|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_044
逻辑ID: 44
文件: StdImpact044.h, StdImpact044.cpp
类型：SOT, 驻留效果
功能说明：丐帮飞龙在天
数据域说明：|移动速度修正%|激发几率|连击点增量|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_045
逻辑ID: 45
文件: StdImpact045.h, StdImpact045.cpp
类型：SOT, 驻留效果
功能说明：丐帮天下无狗
数据域说明：|怒气额外增长量|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_046
逻辑ID: 46
文件: StdImpact046.h, StdImpact046.cpp
类型：SOT, 驻留效果
功能说明：大理非枯非荣标记
数据域说明：|影响的技能集合ID|威力修正率|怒气转换率|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_047
逻辑ID: 47
文件: StdImpact047.h, StdImpact047.cpp
类型：SOT, 驻留效果
功能说明：大理少泽剑标记
数据域说明：|影响的技能集合ID|激发几率|子效果数据索引|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_048
逻辑ID: 48
文件: StdImpact048.h, StdImpact048.cpp
类型：SOT, 驻留效果
功能说明：大理白虹贯日
数据域说明：|子效果数据索引|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_049
逻辑ID: 49
文件: StdImpact049.h, StdImpact049.cpp
类型：SOT, 驻留效果
功能说明：逍遥神光离合
数据域说明：|影响技能集合ID|激发几率|子效果数据索引|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_050
逻辑ID: 50
文件: StdImpact050.h, StdImpact050.cpp
类型：SOT, 驻留效果
功能说明：逍遥欲擒故纵
数据域说明：|怒气产生率修正|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_051
逻辑ID: 51
文件: StdImpact051.h, StdImpact051.cpp
类型：SOT, 驻留效果
功能说明：天山分身专用Buff
数据域说明：|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_052
逻辑ID: 52
文件: StdImpact052.h, StdImpact052.cpp
类型：SOT, 驻留效果
功能说明：逍遥陷阱专用Buff
数据域说明：|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_053
逻辑ID: 53
文件: StdImpact053.h, StdImpact053.cpp
类型：DI, 瞬发效果
功能说明：所有技能冷却,除了指定的冷却ID
数据域说明：|不被冷却的冷却ID|无...

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_054
逻辑ID: 54
文件: StdImpact054.h, StdImpact054.cpp
类型：DI, 瞬发效果
功能说明：复活效果
数据域说明：|复活后的HP%|复活后的MP%|复活后的Rage%|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_055
逻辑ID: 55
文件: StdImpact055.h, StdImpact055.cpp
类型：DI, 瞬发效果
功能说明：转移不良效果到分身上
数据域说明：|转移数目|转移效果集合1|转移效果集合2|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_056
逻辑ID: 56
文件: StdImpact056.h, StdImpact056.cpp
类型：SOT, 驻留效果
功能说明：宠物特性，修改会心、命中、闪避、生命上限、物理和魔法攻防
数据域说明：|命中|闪避|会心|生命最大|物理攻击|物理防御|魔法攻击|魔法防御|无。。。， 

-------------------------------------------------------------------------------------
效果逻辑：STD_IMPACT_057
逻辑ID: 57
文件: StdImpact057.h, StdImpact057.cpp
类型：SOT, 驻留效果
功能说明：宠物生命转换成主人的生命和魔法
数据域说明：|伤害百分率|生命转换百分率|魔法转换百分率|子效果ID(转换到主人的效果，用STD_IMPACT_004)|无。。。， 
