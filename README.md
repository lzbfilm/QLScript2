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
	
