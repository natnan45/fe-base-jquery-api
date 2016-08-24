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

#### ����
-jsoupԭ��

## Attribute
#### html()
 (1)��ȡƥ���һ��Ԫ�صĵ�һ��Ԫ�ص����ݣ�����ƥ��һ��Ԫ�ص�����;

 (2)���ò���������һ��htmlStirng,����һ��function;

#### addClass()
 (1)�ո�ָ��Ӷ��class,����ʹ��removeClassɾ�����;

 (2)����Ϊfunction,����һ��Ԫ�ص�index,��currentClass;

 - removeClass

   removeClass([className]) ��removeClass(function)
 - toggleClass
   toggleClass(className) ��toggleClass(className,state),��toggleClass(function)

#### attr()
 (1)attr(attributeName)��ȡ����ֵ��ƥ��һ��Ԫ���еĵ�һ��Ԫ�أ������Ҫ�����ʹ��each()��map();
 
 (2)attr()��prop()������attr��̬�Ļ�ȡ����,prop��ȡ��̬���ԣ�����selected,checked��;
 
 (3)attr(attributeName,value)��attr(obj),attr(attributeName,function(index,attr))�������Ե�ֵ;
     ע������function�е�this����;

 - removeAttr()

  ��1��ɾ��inline��onclick�¼��󶨣���ie8,9,11�в�֧��ʹ��removeAttr(),�������prop('onclick',null);

#### prop()
  �ӿڷ���������attr()

  - removeProp()

#### val()
  (1)valͨ�����ڱ�Ԫ���ϣ�����input,select,textarea

  (2)���val��ȡselect-multipleʱ����ȡһ�����ѡ�������

  (3)����val(value)��ȡval(function),value����Ϊһ�����飬Ϊһ���Ԫ������ֵ

#### data()
 (1)����ֵ:data(key,value),value�����ǳ���undefined��������;
     data(obj),ֱ������һ������
     
 (2)��ȡֵ:data(key)��data();
 
 (3)Ŀǰ���ṩ�������֧�֣�ע��IE�Ͱ汾��֧��Ԫ�ظ�������
 
 (4)\<div data-role="page" data-last-value="43"\>\</div\>,data-last-value�ᱻ������lastValue��keyֵ

## css
#### addClass() / removeClass() / hasClass() / toggleClass()
  ...
#### css()
  css(propertyName) / css(propertyNames)
  
  - css()���ص���ʽ��Ϥ�����е�λ
  - css(propertyNames) ����һ��propery-value �ԵĶ���
  
  css(propertyName,value) / css(propertyName,function) / css(properties)
  
  - propertyName֧�����ָ�ʽ��һ����'background-color'��css��ʽ,һ����backgroundColor��DOM��ʽ
  - css(propertyName,'')��ɾ����css;
  - ��1.8��ʼ��css()���Զ��������ǰհ������-moz-user-select;
  - 1.6��ʼ��css()֧�����ö�ֵ̬������css('padding-left',"+=15")
  
#### width() / innerWidth() / outerWidth()
  
#### height() / innerHeight() / outerHeight()
  - heigth()��ȡ���ݵĸ߶�
  - innerHeight()��ȡ����+padding�ĸ߶�
  - outerHeight()��ȡ����+padding+border�ĸ߶�/outerHeight(true)��ȡ����+padding+border+margin�ĸ߶�
 
#### offset() / position() / scrollLeft() / scrollTop()
  - offset()�����document��λ��;
  - position()�����offset Parent��λ��;
  
## core
#### jquery()
 jquery(selector[,context]);

 jquery(element)

 jquery(elementArray)

 jquery(object)

 jquery(selection)

 jquery()

 jquery(html[,attributes])

#### jQuery.noConflict
 ɾ��jquery�Ա���$��ʹ�ã�ʹ��jQuery;
 ����ȡһ���±���������q=jQuery.noConflict();

## Deferred
#### jQuery.Deferred()
#### diferred.alwarys()
#### diferred.done();
#### diferred.fail();
 
## Callbacks Object (v1.7)
#### jQuery.Callbacks()
  �๦�ܻص����飬�ṩһ��ǿ��ķ�ʽ����ص����飻
  ���function���ڲ�ʹ�ã���$.ajax()��$.Deferred�ṩ�����Ĺ��ܣ�

  - callbacks.add()
  - callbacks.empty()
  - callbacks.fire() / callbacks.fired()
  - callbacks.fireWidth()
  - callbacks.remove()
  - callbacks.disable() / callbacks.disabled()
  - callbacks.lock() / callbacks.locked()
  - callbacks.has()
  - callbacks.remove()

## С�۷�
 - .filter()
 - .not()
 - .first()
 - .appendTo()
 - parseFloat() / parseInt()