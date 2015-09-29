笔记
字面量
对象是属性的集合，
var sl={"first":"1","second":"2"};
si.first="cure";
si[first]="cure";
每个对象都边连接到一个原型对象，我们从中继承属性

减少全局变量的污染
1，把多个全局变量整理在一个命名空间下，
var MYAPP={};

MYAPP.stooge={
     "first-name":"JOE",
     "last-name":"PETER";
};
MYAPP.flight={
     airline:"american",
     number:"456",
     arrival:{
data:"2233",
city:"english"
}
}
另一种方法是闭包
闭包很根本
当一个函数保存为对象的一个属性时，我们称它为方法
一，加载文件
a.加载HTML文件；     load
b.加载JSON文件；     getJSON
c.加载Javascript文件；     getScript
d.加载XML文件。     get
二，向服务器获取数据
$.ajax的一般格式
$.ajax({
     type: 'POST',
     url: url ,
    data: data ,
    success: success ,
    dataType: dataType
});
url必需。规定把请求发送到哪个 URL。data可选。映射或字符串值。规定连同请求发送到服务器的数据。success(data, textStatus, jqXHR)可选。请求成功时执行的回调函数。dataType可选。规定预期的服务器响应的数据类型。
默认执行智能判断（xml、json、script 或 html）。
实例：
$(document).ready(function() {
          $.ajax({
               url: '/reqxml',
               type: 'post',
               data: {
                    action:'46101',
                    menu_id:'20001',
                    stockCode:'600600',
                    npage:'1',
                    maxcount:'5',
                    ReqLinkType:'2'
               },
               error: function(){alert("请求数据时，出现错误！")},
               success: function(data){       }
          })         
     });
在文档对象模型 (DOM) 中，每个节点都是一个对象。DOM 节点有三个重要的属性 ：
1. nodeName : 节点的名称
2. nodeValue ：节点的值
3. nodeType ：节点的类型
一、nodeName 属性: 节点的名称，是只读的。
1. 元素节点的 nodeName 与标签名相同
2. 属性节点的 nodeName 是属性的名称
3. 文本节点的 nodeName 永远是 #text
4. 文档节点的 nodeName 永远是 #document
二、nodeValue 属性：节点的值
1. 元素节点的 nodeValue 是 undefined 或 null
2. 文本节点的 nodeValue 是文本自身
3. 属性节点的 nodeValue 是属性的值
三、nodeType 属性: 节点的类型，是只读的。以下常用的几种结点类型:
元素类型    节点类型
  元素          1
  属性          2
  文本          3
  注释          8
  文档          9
