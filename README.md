# QLScript_New

本库的一对一通知和Nolan的Mark、Ark(原Nvjdc)登录产生的备注格式互相兼容，且只有使用Ark(原Nvjdc)登录的才会在资产查询中显示预计过期时间.

如果遇到什么问题先看看,可能有收获:	https://www.kejiwanjia.com/jiaocheng/61708.html

2.10.3之前版本青龙拉库命令:

	不包含sendNotify:

	ql repo https://github.com/ccwav/QLScript2.git "jd_" "NoUsed" "ql|utils"

	包含sendNotify:

	ql repo https://github.com/ccwav/QLScript2.git "jd_" "NoUsed" "ql|sendNotify|utils"


2.10.3之后版本青龙拉库命令:

	不包含sendNotify:

	ql repo https://github.com/ccwav/QLScript2.git "jd_" "NoUsed" "ql|utils|USER_AGENTS|jdCookie|JS_USER_AGENTS"

	包含sendNotify:

	ql repo https://github.com/ccwav/QLScript2.git "jd_" "NoUsed" "ql|sendNotify|utils|USER_AGENTS|jdCookie|JS_USER_AGENTS"
	
jd_CheckCK.js (已添加支持一对一推送)
(最新的通知脚本已经集成自动禁用失效CK，如不需要自动启用CK功能可以直接禁用此脚本.)

京东CK检测,不正常的自动禁用，正常的如果是禁用状态则自动启用.配合通知脚本CK触发使用.也可以直接task.

兼容jd_bean_change的BEANCHANGE_USERGP2 BEANCHANGE_USERGP3 BEANCHANGE_USERGP4变量.

变量列表:

显示正常CK:  export CHECKCK_SHOWSUCCESSCK="true"
永远通知CK状态:  export CHECKCK_CKALWAYSNOTIFY="true"
停用自动启用CK:  export CHECKCK_CKAUTOENABLE="false"	
服务器空数据等错误不触发通知:  export CHECKCK_CKNOWARNERROR="true"

BEANCHANGE_USERGP2 BEANCHANGE_USERGP3 BEANCHANGE_USERGP4  根据Pt_Pin的值进行分组通知        
分组通知的通知标题为 脚本名+"#"+分组数值
主要用于搭配通知脚本的分组通知使用.

增加CHECKCK_ALLNOTIFY设置温馨提示，推送时在内容末尾添加显示
一对一推送只有推送账户失效时才会添加.用法参考BEANCHANGE_ALLNOTIFY.
