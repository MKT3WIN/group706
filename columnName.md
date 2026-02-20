🔹 第一类：客户身份

Cust_ID → 客户唯一编号

SCF_Code → 地区/邮编区域代码

👉 只是识别用，一般不直接进模型（除非做地理分析）

🔹 第二类：实体店消费（Ret = Retail）

比如：

RetF07Dollars

RetF07Trips

RetF07Lines

解释：

字段 含义
Dollars 消费金额
Trips 购物次数
Lines 购买商品种类数

F07 = Fall 2007
S07 = Spring 2007
F06 = Fall 2006
S06 = Spring 2006
Pre04 = 2004年前

👉 这是线下门店消费历史

🔹 第三类：网络消费（Int = Internet）

比如：

IntF07GDollars

IntF07NGDollars

IntF07Orders

解释：

| G | Gift |
| NG | Non-gift |
| Orders | 订单数 |
| Lines | 商品行数 |

👉 这是线上消费数据

🔹 第四类：目录购买（Cat = Catalog）

和 Internet 类似：

CatF07GDollars

CatF07Orders

👉 这是目录营销销售渠道

🔹 第五类：营销接触记录

EmailsF07 → 发过多少邮件

CatCircF07 → 目录寄送次数

GiftRecF07 → 收到礼品次数

NewGRF07 → 新礼品接收

👉 这是营销曝光强度

🔹 第六类：客户兴趣标签（非常重要）

比如：

Travel

Wines

Exercise

Cooking

DogOwner

Fashion

Camping

Hunting

👉 这些是客户兴趣标签（0/1变量）

这类变量非常适合做：

客户细分

消费预测

🔹 第七类：人口统计变量（建模核心）

非常关键：

AgeCode → 年龄分段

IncCode → 收入分段

HomeCode → 房屋类型

Child0_2, Child3_5… → 是否有孩子

Dwelling → 住宅类型

LengthRes → 居住年限

HomeValue → 房屋估值

👉 这些是你回归模型的黄金变量。

🔹 第八类：首次购买信息

FirstYYMM → 第一次购买时间

FirstChannel → 首次购买渠道

FirstDollar → 首次消费金额

AcqDate → 获客时间

StoreDist → 离店距离

👉 可以做客户生命周期分析
