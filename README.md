# Mobile-order-screenshot-template-generation
手机订单图截图模板生成

## 背景

有很多做电商的客户，需要用到订单图生成，借这个业务需求，今天给大家带来一款扒站实战教程，百分百还原。

**文章仅供技术学习，法律风险责任与本人无关。侵权联系我删除。**

## 目标站点

把目标站点的整个功能拔下来，为自己所用，并在基础上进行功能开发。

![](https://files.mdnice.com/user/42685/65e71501-4fe9-480d-8e3b-ac3c038cfba1.png)

## 核心步骤

使用wget将整个页面功能进行爬取下载到本地。具体参数如下命令
```bash
wget \
  --mirror \                         # 递归下载整个网站
  --convert-links \                  # 转换链接为本地路径
  --adjust-extension \               # 补充文件扩展名（如 .html）
  --page-requisites \                # 下载 CSS/JS/图片等依赖
  --no-parent \                      # 不下载上级目录
  -e robots=off \                    # 忽略 robots.txt
  --span-hosts \                     # 跨域名下载（如 CDN 资源）
  --user-agent="Mozilla/5.0" \       # 模拟浏览器 UA
  --directory-prefix=./offline_site \ # 指定保存目录
  --wait=1 \                         # 避免被封禁
  --reject-regex "logout|admin|api" \ # 排除敏感路径
  https://example.com
```

## 效果演示

去除多余元素，个性化页面后，把项目跑起来，功能都是正常的，整体效果如下：

![](https://files.mdnice.com/user/42685/47d95d29-968e-479e-a231-13954e0a4c2e.png)

生成订单图效果：

![](https://files.mdnice.com/user/42685/ee869675-8082-43cb-96da-39b247e58af2.jpg)


移除具体内容，抽离框架作为下一次二次开发，具体效果如下：

![](https://files.mdnice.com/user/42685/0306a44a-b3ad-435d-9813-c194c90e9394.png)

## 联系方式

email: 646997146@qq.com

公众号：CodeRevolt

