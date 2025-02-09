#### open-data

用于展示平台开放的数据。

**平台差异说明**

|App|H5|微信小程序|支付宝小程序|百度小程序|字节跳动小程序、飞书小程序|QQ小程序|快应用|360小程序|快手小程序|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|x|x|√|x|√|x|√|x|x|x|

**Tips**

该功能为各小程序平台提供的开放能力。App端和H5端不涉及此概念。

支付宝和字节跳动没有open-data组件，但提供了API方式获取相关信息。支付宝[参考](https://docs.alipay.com/mini/api/ch8chh)、字节跳动[参考](https://developer.toutiao.com/dev/cn/mini-app/develop/open-capacity/user-information/getuserinfo)

**属性说明**

|属性名|类型|默认值|说明|平台差异说明|
|:-:|:-:|:-:|:-:|:-:|
|type|String||开放数据类型||
|open-gid|String||当 type="groupName" 时生效, 群id|微信小程序、QQ小程序|
|lang|String|en|当 type="user*" 时生效，以哪种语言展示 userInfo，有效值有：en, zh_CN, zh_TW|微信小程序、QQ小程序|

**type 有效值**

|值|说明|平台差异说明|
|:-:|:-:|:-:|
|userNickName|用户昵称||
|userAvatarUrl|用户头像||
|userGender|用户性别||
|groupName|拉取群名称|微信小程序、QQ小程序|
|userCity|用户所在城市|微信小程序、QQ小程序|
|userProvince|用户所在省份|微信小程序、QQ小程序|
|userCountry|用户所在国家|微信小程序、QQ小程序|
|userLanguage|用户的语言|微信小程序、QQ小程序|

**示例**

```html
<open-data type="userNickName"></open-data>
<open-data type="userAvatarUrl"></open-data>
<open-data type="userGender"></open-data>
```
