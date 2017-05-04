防忽悠咨询热线
==============

根据赵大忽悠、范德彪 2005 年的小品《功夫》实现的 Asterisk 语音流程，可用来搞笑、将诈骗电话转接到此流程。


使用方法
========

Asterisk 服务器拨号规则的配置
-----------------------------

* 将 “防忽悠咨询热线.conf” 放到 asterisk 的配置文件目录下，例如： `/etc/asterisk` (CentOS)
* 将小品《卖拐》《卖车》《功夫》的语音剪辑准备好，并放到 asterisk 的语音目录下，例如： `/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线` (CentOS)

http://tv.cntv.cn/video/C13407/ac4eee3c4959440d947b29f66a65b154

	# ll /var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线
	total 16948
	-rw-rw-r-- 1 1000 1000   169878 6月  12 16:16 主菜单_范伟.wav
	-rw-rw-r-- 1 1000 1000   145036 6月  16 09:39 你不按套路出牌啊_范德彪.wav
	-rw-rw-r-- 1 1000 1000    14902 6月  13 15:03 先杀猪_范伟.wav
	-rw-rw-r-- 1 1000 1000    14360 6月  13 15:04 先杀驴_范伟.wav
	-rw-rw-r-- 1 1000 1000  3088680 7月  12 13:35 卖车_剪辑_范伟、赵本山、高秀敏.wav
	-rw-rw-r-- 1 1000 1000 11718330 6月  13 18:28 小品《功夫》剩下的部分_赵本山、范伟、蔡维利、王晓虎.wav
	-rw-rw-r-- 1 1000 1000   538200 6月  13 15:51 恭喜你，答对了，猪__也是这么想滴_蔡维利、范伟、赵本山.wav
	-rw-rw-r-- 1 1000 1000   740550 6月  12 18:32 拐了，卖了，拐卖了_高秀敏.wav
	-rw-rw-r-- 1 1000 1000   245122 6月  12 16:15 欢迎语_范伟.wav
	-rw-rw-r-- 1 1000 1000   301492 6月  16 09:42 脑筋急转弯菜单_范伟、赵本山.wav
	-rw-rw-r-- 1 1000 1000    15282 6月  13 14:58 请按1_范伟.wav
	-rw-rw-r-- 1 1000 1000    15698 6月  13 14:58 请按2_范伟.wav
	-rw-rw-r-- 1 1000 1000    15864 6月  13 14:59 请按3_范伟.wav
	-rw-rw-r-- 1 1000 1000   309036 6月  13 15:56 那_驴_也是这么想滴_王晓虎、赵本山.wav

	# file /var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/*
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/主菜单_范伟.wav:                                           RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/你不按套路出牌啊_范德彪.wav:                               RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/先杀猪_范伟.wav:                                           RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/先杀驴_范伟.wav:                                           RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/卖车_剪辑_范伟、赵本山、高秀敏.wav:                        RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/小品《功夫》剩下的部分_赵本山、范伟、蔡维利、王晓虎.wav:   RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/恭喜你，答对了，猪__也是这么想滴_蔡维利、范伟、赵本山.wav: RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/拐了，卖了，拐卖了_高秀敏.wav:                             RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/欢迎语_范伟.wav:                                           RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/脑筋急转弯菜单_范伟、赵本山.wav:                           RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/请按1_范伟.wav:                                            RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/请按2_范伟.wav:                                            RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/请按3_范伟.wav:                                            RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz
	/var/lib/asterisk/sounds/zh_CN/防忽悠咨询热线/那_驴_也是这么想滴_王晓虎、赵本山.wav:                     RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 8000 Hz

* 在 asterisk 的拨号规则为你的电话所在的 context 中增加一条类似 `exten => 44444444,1,Goto(防忽悠咨询热线,s,1)` 的拨号规则，你也可以把 `44444444` 换成你自定义的接入号码
* (可选) 购买语音卡，语音卡用来将 PSTN 公共电话网络或办公分机接入到 Asterisk 服务器，俗称“落地”。
* 用SIP IP 电话或者固定电话或者手机拨打上面你设置的号码(`44444444`)，然后根据语音提示操作就好了，或者参照 ![防忽悠咨询热线 流程图.png](https://github.com/moontide/Anti-fooling-Hot-Line/raw/master/防忽悠咨询热线%20流程图.png)
	* 如果用 SIP 电话拨打，请先在 Asterisk 中配置好你的帐号，然后用此帐号从 SIP 电话中登录到你的 Asterisk 服务器
	* 如果用办公分机拨打，请确认设置的号码能够接入进来

* (可选，建议配置) 为 Asterisk 增加“呼叫转移（盲转）”的配置： 修改 `features.conf`， 启用 [featuremap] 下的 `blindxfer => #1` (呼叫盲转) 配置

诈骗电话已经接到，如何转到“防忽悠咨询热线”
--------------------------------------------
* 如果是话机（模拟话机或者 SIP 话机）直接连到 Asterisk 的，则可以使用 Asterisk 内置的“呼叫转移（盲转）”功能进行转移： 通话过程中按 `#1` (或者其他按键，参见上一节“呼叫转移”配置)，然后输入防忽悠咨询热线的接入号。
* 如果话机是通过传统交换机转接到 Asterisk 的，只能利用传统交换机的呼叫转移功能进行转移：通话过程中，迅速按一下模拟话机的“叉簧”（或者按一下模拟话机的“FLASH/闪断”按钮，如果有的话……），然后输入防忽悠咨询热线的接入号。
