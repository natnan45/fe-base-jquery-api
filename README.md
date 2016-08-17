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

### �ӿ�

#### ajax();
   ...
#### get();post();load();getJson();getScript();
   ...



## Attribute
#### html()
 (1) ��ȡƥ���һ��Ԫ�صĵ�һ��Ԫ�ص����ݣ�����ƥ��һ��Ԫ�ص�����;

 (2) ���ò���������һ��htmlStirng,����һ��function;

#### addClass()
 (1) �ո�ָ��Ӷ��class,����ʹ��removeClassɾ�����;

 (2) ����Ϊfunction,����һ��Ԫ�ص�index,��currentClass;