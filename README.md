
<div align="center">  <img src="https://imgs.lfeng.tech/images/2023/09/ip.png" width = "100" height = "100" alt="图片名称" align=center /> </div>


<center>IP Check是一个简单高效的Alfred Workflow，可以方便的一键查询ip的归属地等详细信息。</center>


## 使用体验

直接打开Alfred输入框，键入**ip + 空格 + 需要查询的IP地址**即可，下面会显示该ip所在的城市，所属机构，时区，邮编，经纬度。更多的信息大家可以在workflow中自行添加。

![YE0p9P](https://imgs.lfeng.tech/images/2023/09/YE0p9P.png)


## 如何安装

> 前提条件：
> 1. 安装好了Alfred并且激活了Powerpack。
> 2. 本机安装好了`jq`，因为workflow会使用jq解析json，这个直接brew安装就行。
### 1. 直接下载后双击安装

目前在Alfred 5上测试安装没问题。

### 2. 打开IP Checker并替换token

安装好之后，双击打开IP Check的Script Filter，将其中的11111111替换为你自己的token。

> 这里使用到了`https://ipinfo.io/` 提供的免费接口，大家直接注册就可以获得免费的token，免费的额度足够个人的使用了。

![sAuCRK](https://imgs.lfeng.tech/images/2023/09/sAuCRK.png)

![9m82T7](https://imgs.lfeng.tech/images/2023/09/9m82T7.png)

## Workflow实现

直接使用了现成的Script Filter，然后在用户每次输入之后会调用ipinfo提供的API去获取ip的详细信息，接着会使用jq对结果进行解析，并把信息放在相关的行作为展示。整体比较简洁高效。

大家可以根据自己的需求进行相关的调整。

---

欢迎关注我的个人公众号【码老思】，这里会分享关于编程的一切，和你一起成长。

<div align="center">  <img src="https://imgs.lfeng.tech/images/2023/09/JwgHMm.png" width = "300" height = "300" alt="图片名称" align=center /> </div>
