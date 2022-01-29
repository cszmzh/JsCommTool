# JsCommTool
## 一. 说明

基于`MyJsCommTool`的串口测试页面，需要运行工具 https://gitee.com/bonn/myjscommtool 

## 二. 使用方法

将`test.html`放入`MyJsCommTool`文件夹下的`myHtml`目录，打开工具，在右侧打开页面即可。

## 三. 参数说明

`type`为每个模块的名字

`childButton`对应每个模块下的按钮

`buttonName`为按钮名字

`desc`为备注

`orderIndex`为首次执行的命令序号

`order`为命令集，可以实现点击按钮循环执行命令集

`style`为按钮的CSS样式参数

例如：

```js
    var data = {
        functionList: [
            {
                type: "距离",
                childButton: [
                    {
                        buttonName: "放大",
                        desc: "变倍加(变倍 + AF)",
                        orderIndex: 0,
                        order: ["FC800101007E","FC8001010060"],
                        style: "color:red"
                    },
                    {
                        buttonName: "缩小",
                        desc: "表示连续键停止，所有的连续键结束时发送",
                        orderIndex: 0,
                        order: ["FC800100007D"]
                    },
                    {
                        buttonName: "自动",
                        desc: "AF + AE",
                        orderIndex: 0,
                        order: ["FC800300007F"]
                    },
                    {
                        buttonName: "远焦",
                        desc: "焦距减(far) 远焦",
                        orderIndex: 0,
                        order: ["FC800200007E"]
                    },
                    {
                        buttonName: "近焦",
                        desc: "焦距加(Near) 近焦",
                        orderIndex: 0,
                        order: ["FC800201007F"]
                    }
                ]
            }
        ]
    };
```

运行效果：

<img src="https://yun.515code.com/ipic/20220129-78affd56.png" style="zoom:67%;" />
