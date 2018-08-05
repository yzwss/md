
## 表单验证
controller  
service  
domain  
repository  

@Valid  
@Min  

## AOP
OOP 对象集合通过方法调用实现通信  
@Aspect  
@Component  
@PointCut  
@Before  
@After  

## 异常处理
return {
    code:
    message/msg:
    data: {}
}

@ControllerAdvice  
@ExceptionHandler  
@ResponseBody  

## 单元测试
@RunWith(SpringRunner.class)  
@SpringBootTest  
@Autowired  
@Test  
@AutoConfigureMockMvc  

MVC需要开发模板，并且需要把数据放入模型中，让他们自动绑定。href跳转，里面也是补充参数数据。  
前后端分离后端只管给数据，数据放入前端的模型中，然后由前端来自动绑定。  
区别就是数据放入后端模型中，那没办法只能模板这块后端一起开发了。而放入前端模型中，则可以放手不管了。  
前端框架Vue需要关注事件，而MVC则不需要关注事件，因为Controller中的api其实就是事件了，Controller相当于和一个页面对应，以前只能请求一个页面，而MVC实现了请求一个方法。