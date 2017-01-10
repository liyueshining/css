html 如下：

~~~
<div className="converter-pos">
     <a href="#" >
          <span className="language_icon"></span>
          Switch to OKI in English
     </a>
</div>
~~~

css 如下：

~~~
.converter-pos {
    float: right;
    height: 43px;
    line-height: 39px;

    vertical-align: top;
    padding-top: 2px;

    border: 1px solid white;

    color: gray;
}

.converter-pos a {
    color: lightgray;

    font-family: Arial;
    font-size: 14px;
}

.converter-pos a:hover {

    text-decoration: none;
    color: darkgrey;
}

.language_icon {

    width: 20px;
    height: 30px;
    display: inline-block;

    vertical-align: text-top;
    margin-right: 8px;

    background-image: url(../img/language-icon.png);
    background-repeat:no-repeat;
    background-position: -35px -5px;
}

.converter-pos a:hover .language_icon{
    background-position: -5px -5px;
}
~~~

结论：

1. 当class为当前标签中一个属性时，则样式写为：标签+class名
2. 当class为子标签的一个属性时，则样式写为：标签+空格+class名

另外：

关于background-posotion的坐标的使用： 组件的左上角是 坐标的起点，可以结合组件的大小和图片的大小，来改变显示一张大图中的某个部分。如上例
组件的大小是 20px  30px, 背影图片是 60px 30px, 内有两小图 都是 20 20，padding是5。改变背影的坐标就可以显示不同的图片。
