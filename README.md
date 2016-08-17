# jquery api
## ajax
### 全局ajax事件
####ajaxSetup()
  全局设置ajax请求，不推荐采用；
  
  比如
  ```
  $(document).ajaxSetup({
    url:'/text.html',
    global:false, //关闭全局事件
    type:'POST'
  })
  ```
  
#### ajaxStart(hander)
  
  hander
  
    type:function()
  
  全局设置当任意一个ajax请求开始时，执行hander
  
#### ajaxSend(hander)
  
  hander
  
    type:Function( Event event, jqXHR jqXHR, PlainObject ajaxOptions )
  
  全局设置任意一个ajax请求发送前，执行hander;
  event是触发ajax的事件，jqXHR即XMLHttpRequest;
  ajaxOptions即ajax请求设置
  
#### ajaxComplete(hander)
  
   hander
    
    type:Function( Event event, jqXHR jqXHR, PlainObject ajaxOptions )
    
   全局设置任意一个ajax请求完成后，执行hander;
    
#### ajaxStop(hander)

  ...
  
#### ajaxError(hander)

  hander
      
      type:Function( Event event, jqXHR jqXHR, PlainObject ajaxOptions, String thrownError)
      
     全局设置任意一个ajax请求完成后，执行hander;
     throwError 获取http响应码对应的提示，比如404的'Not found'

#### ajaxSuccess()

  ...

### 接口

#### ajax();
   ...
#### get();post();load();getJson();getScript();
   ...



## Attribute
#### html()
 (1) 获取匹配的一组元素的第一个元素的内容；设置匹配一组元素的内容;

 (2) 设置参数可以是一个htmlStirng,或者一个function;

#### addClass()
 (1) 空格分割，添加多个class,或者使用removeClass删除多个;

 (2) 参数为function,接受一个元素的index,和currentClass;

#### attr()
 (1) attr(attributeName)获取属性值，匹配一组元素中的第一个元素，如果需要多个，使用each()或map();
 
 (2) attr()与prop()的区别，attr静态的获取属性,prop获取动态特性，比如selected,checked等;
 
 (3) attr(attributeName,value)，attr(obj),attr(attributeName,function(index,attr))设置属性的值;
     注意其中function中的this引用;

#### data()
 (1) 设置值:data(key,value),value可以是除了undefined任意类型;
     data(obj),直接设置一个对象。
     
 (2) 获取值:data(key)或data();
 
 (3) 目前不提供跨浏览器支持，注意IE低版本不支持元素附加属性
 
 (4) \<div data-role="page" data-last-value="43"\>\</div\>,data-last-value会被解析成lastValue的key值