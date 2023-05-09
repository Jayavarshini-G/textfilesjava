# textfilesjava



mvn archetype:generate -DgroupId=com.kgisl.springxml1 -DartifactId=springxml1 -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false

blocking-servlet
nonblocking-react programming language
servlet id synchronous ie.one request runs at a time

objet creation by third party-IOC Container
Dependency Injection-inserting line
IOC Container-When we give bean model+meta data it will give READY TO USE OBJECT


bean-
Resuable component which is mainatained by the spring IOC Container




ComponentScan in a Spring Application. With Spring, we use the @ComponentScan annotation along with the @Configuration annotation to specify the packages that we want to be scanned. 
@ComponentScan without arguments tells Spring to scan the current package and all of its sub-packages.
<!-- Add support for component scanning -->
<context:component-scan base-package="com.poc" />


stereo type-
service
controller-process our request to create model then pass to front controller
component
repository





web container-html+java,web application
servlet container-inside tomcat server which identify server which is catalina,only java file
spring container-
spring conteext
spring ioc container



@RequestMapping(method = RequestMethod.GET)
    public String printHello(Model model) {
          model.addAttribute("message", "Hello World!!");
          return "hello";
       }
|
^
Model is an container(entire page data)we can add attribute


@RequestMapping("/helloworld")
public String hello(ModelMap map) {
    String helloWorldMessage = "Hello world!";
    String welcomeMessage = "Welcome!";
    map.addAttribute("helloMessage", helloWorldMessage);
    map.addAttribute("welcomeMessage", welcomeMessage);
    return "hello";

@RequestMapping("/welcome")
public ModelAndView helloWorld() {
        String message = "Hello World!";
        return new ModelAndView("welcome", "message", message);
    }



spring mvc:
model view controll
root:dao and service class(first empty class will be created)
Bean Factory is Root interface and ApplicationContext is a sub interface.
//webxml complete after configuration run
@configration:no proper order compiler itselkf run any file first
Example:
package com.kgisl.springxml1.config;

import org.springframework.context.annotation.Configuration;

@Configuration
public class springConfig1 {
    static {
        System.out.println("config 1 class loader");
    }
}

package com.kgisl.springxml1.config;

import org.springframework.context.annotation.Configuration;


@Configuration
public class SpringJdbcConfig {
    static {
        System.out.println("config class loader");
    }
}
Here output may be config1class loader and config class loader or config class loader and config1 class loader


local inner class
member inner class-class creat and method create and call-property above autowired put


Dependency injection-3 types
multiple framework
method level-constructor injection
constructor,setter,field





bean-ready to use object
====>configurationC:\Users\jayavarshini.g\springtest\src\main\java\com\kgisl\springtest\config\Student.java
app initializer 
web config
mvc




hibernate c3p0=conncection pooling framework
service class-Transactionl(business logic)



Angular-support two way communication(text box typing also refelect in component and control also variablebind)
MVC-FEATURES
>Unit testing
>Code reusability
>DI


SPA-Single Page Application
          Mostly have index page we call it as shell page  .Now mostly used by all

MPA-Master Page Application(C# use)
            we call it as Master Page-menu tag-(not loding entire page displaying only necessary details) dynamically loaded it have only div portion
    

npm init
npm int -y(it dont ask questions like artifact id like that)package.json only create
dependencies-normal dependency
devdependicies for Plugin
ecma same as ES6
angular support typescript	


main.ts is root module
transpiling-converting .ts file to .js
webpack-pakaging tool
iv for ompiling
rxjs-java stream in library
jasmine-ubnit testing framework
jasminewd2-web driver browers imolementation
js-node js
nodejs environmrnt-node
jasmine-html-repoter-Spec generator
karma-test runner tool
protractor-end to end test tool
subscribe-observable(return somethimg)





GIT-Working copy+Local Repositoty
SUBVERSION-Working copy


SDLC-Planning,analysis,design,implementation,integration and testing,maintanence

code+build=agile development
integration+test-continous integration
release-continous delivery
Deploy-continous deployment
Operate-Devops
Testing:unit,integration,end to end
Unit test-every build run
Integration-only once in a day without user interface
End to end-with user interface run weekly twice or weekend


                   onpremises                   cloud

code            sonarcube                 sonarcloud
build           ngbuild,etc
Integrate    jenkins/teamcity       travisci              
Test            junit,testnj,etc
Release      arifact server             docker image
Deploy      Ansible                         paas
Operate



set PATH=%PATH%;C:\Program Files\Git\bin;











SCRUM-stories+todo+in progress+test+done
Portfolio backlog-epic+feature
epic ex:need to create login page
feature:button click means gettiing from user or database or etc(sign in ,sign up or forgot password etc)these all combined is epic
Backlog Item-Full Stack Developer itself writing code for clicking button
Task:screen disigning like that
Issue tracking tool:identifying the bug



backlog is called as user stories

mvn archetype:generate -DgroupId=com.kgisl.BookJsonDao -DartifactId=BookJsonDao -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false


ctrl+shift+r
ctrl+shift+i






@ParameterizedTest annotation marks this method as a parameterized test, which means it will be executed multiple times with different input values.
 The @ArgumentsSource annotation specifies the MyArgumentsProvider class as the provider for generating the input arguments.
The testAddition method takes three integer arguments (a, b, and expected), which correspond to the input values and expected output of the addition operation. The method performs addition on the first two arguments (a and b) and then asserts that the result matches the expected third argument (expected) using the assertEquals method.

Parameterized tests can be helpful when you need to test a method with a large number of inputs or input combinations. 
Instead of writing individual tests for each input value, you can define a single parameterized test that can test a wide range of inputs. The ArgumentsSource feature in JUnit 5 provides a flexible way to generate input arguments for parameterized tests, making it easier to write expressive, concise, and maintainable tests.















What is Spring Framework and what are its advantages?
Frame to create web application.

What is Inversion of Control (IoC) in Spring Framework?
=>Objet creation by third party.When we give bean model+meta data it will give ready to use object


What is Dependency Injection (DI) in Spring Framework?
=>There are 2 types
Constructor
Getter,Setter injection


What is a Bean in Spring Framework?
=>Bean is Ready to Use Object.Resuable componenet which is maintained by string IoC container.


What are the different scopes of Beans in Spring Framework?
=>Singleton,prototype,request,application


What is a BeanFactory in Spring Framework?
=>It is used to manage number of Beans


What is an ApplicationContext in Spring Framework?
=>Root
=>To access Ioc Container

What is the difference between BeanFactory and ApplicationContext in Spring Framework?
=>Bean Factory is Root interface and ApplicationContext is a sub interface.

What is Spring MVC and how does it work?
model view controll

What is the DispatcherServlet in Spring MVC?
=>Its a Front controller which load first


What is a Controller in Spring MVC?
=>It Process our request to create model then pass to front controller


What is a View in Spring MVC?


What is a Model in Spring MVC?
=>Model is an container we can add attribute


What is a ViewResolver in Spring MVC?
What is the difference between @Component, @Service, and @Repository annotations in Spring Framework?

What is the purpose of @Autowired annotation in Spring Framework?
=>To inject object

What is the purpose of @RequestMapping annotation in Spring MVC?
To map the servlet

What is the purpose of @PathVariable annotation in Spring MVC?
What is the purpose of @RequestParam annotation in Spring MVC?
What is the purpose of @ResponseBody annotation in Spring MVC?

What is the purpose of @Valid annotation in Spring MVC?
=>To check the condition i.e whether the given data matches to the condition or not


What is the purpose of @Configuration annotation in Spring Framework?
=>@Configuration - path which given this annotation will run first.

What is the purpose of @Bean annotation in Spring Framework?
=>used to create ready to use object

What is the difference between @Configuration and @Component annotations in Spring Framework?
=>@Configuration - path which given this annotation will run first.
=>@Component- here we give our file path.


How many ways can Dependency Injection be done in Spring framework ?
=>3 ways
constructor , Getter&Setter,Method level
