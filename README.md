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

### 低层接口
