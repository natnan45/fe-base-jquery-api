# jquery api
## ajax
### ȫ��ajax�¼�
####ajaxSetup()
  ȫ������ajax���󣬲��Ƽ����ã�
  
  ����
  ```
  $(document).ajaxSetup({
    url:'/text.html',
    global:false, //�ر�ȫ���¼�
    type:'POST'
  })
  ```
  
#### ajaxStart(hander)
  
  hander
  
    type:function()
  
  ȫ�����õ�����һ��ajax����ʼʱ��ִ��hander
  
#### ajaxSend(hander)
  
  hander
  
    type:Function( Event event, jqXHR jqXHR, PlainObject ajaxOptions )
  
  ȫ����������һ��ajax������ǰ��ִ��hander;
  event�Ǵ���ajax���¼���jqXHR��XMLHttpRequest;
  ajaxOptions��ajax��������
  
#### ajaxComplete(hander)
  
   hander
    
    type:Function( Event event, jqXHR jqXHR, PlainObject ajaxOptions )
    
   ȫ����������һ��ajax������ɺ�ִ��hander;
    
#### ajaxStop(hander)

  ...
  
#### ajaxError(hander)

  hander
      
      type:Function( Event event, jqXHR jqXHR, PlainObject ajaxOptions, String thrownError)
      
     ȫ����������һ��ajax������ɺ�ִ��hander;
     throwError ��ȡhttp��Ӧ���Ӧ����ʾ������404��'Not found'

#### ajaxSuccess()

  ...

### �Ͳ�ӿ�
