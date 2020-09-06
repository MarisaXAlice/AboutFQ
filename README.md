# AboutFQ
我的github翻墙相关整理

https://www.youtube.com/watch?v=pAcYHlMQrRY&ab_channel=SiemensTutorials
  欢迎关注订阅我的频道！
我的节点站:

1: https://www.xjycloud.xyz
(注册即送50g免费流量)

2:https://www.xjycloud.pw

关于安装失败的请自查操作，同时确认区域是否是达拉斯！东京的话请请切换！切换方式点击账户登陆CLI和API，复制IBM Cloud CLI到shell窗口运行，然后区域选择7，最后重新运行以下1或者2安装脚本！一些很高尚的人请跑路！追求4K的请无视，作为备用且行且珍惜！
【安装脚本】: 

一键安装脚本：wget --no-check-certificate -O install.sh https://raw.githubusercontent.com/CCChieh/IBMYes/master/install.sh && chmod +x install.sh  && ./install.sh

一键安装脚本2:
wget --no-check-certificate -O install.sh https://raw.githubusercontent.com/siemenstutorials/IBMYes/master/install.sh && chmod +x install.sh  && ./install.sh

【注意:建议用脚本2进行安装脚本1的子项目删库了】
2.资源组ID:
ibmcloud resource groups

3.4个secret:
IBM_ACCOUNT // IBM Cloud的登录邮箱和密码
IBM_APP_NAME // 应用的名称
REGION_NUM // 区域编码
RESOURSE_ID // 资源组ID

4:yml文件更改


./IBM_Cloud_CLI/ibmcloud cf install
修改成
./IBM_Cloud_CLI/ibmcloud cf install -v 6.51.0

5.CF反代脚本：
addEventListener(
"fetch",event => {
let url=new URL(event.request.url);
url.hostname="你的域名";
let request=new Request(url,event.request);
event. respondWith(
fetch(request)
)
}
)
