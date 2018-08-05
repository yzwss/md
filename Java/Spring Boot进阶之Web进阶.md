
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
前后端分离只管给数据。