## Spring MVC Archetecture

FrontController <-> Controller (model) <-> Services(Busisness logic) <-> database
FrontController <-> View Template (model)

## Spring MVC Request Flow

1. DispatcherServlet(Front Controller) receives HTTP request
2. DispatcherServlet identifies the right Controller based on the URL
3. Controller executes Business Logic
4. Controller returns a)Model b)View Name back to DispatcherServlet
5. DispatcherServlet identifies the correct view (ViewResolver)
6. DispatcherServlet makes the model available to view and executes it
7. DispatcherServlet returns HTTP Response bak

## General web applicatin in java: Architecture

### Model 1 JSP
Everything is in JSP
No servelets or controllers

### Model 2 MVC
Model - Todo.java
View - login.jsp
Controller - Servlet(controlls the flow) LoginServelt.java, TodoServlet.java, Servlet3.java

Controller populates the model and then post to view

### Model 3 Modified MVC

Front Controller: will be in front of all request
For example, the DispatcherServelet decides which servlet to go to
