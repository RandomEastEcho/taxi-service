# Taxi-Service imitation
This project is imitation of Taxi-Service. Created with usage of Tomcat and SQL.
## Features
<ul>
  <li> Authentication service</li>
  <li> Create and delete manufacturer</li>
  <li> Create and delete driver</li>
  <li> Create and delete car</li>
  <li> Ability to add drivers to specific car</li>
  <li> Ability to display all cars belonging to the current driver</li>
  <li> Display all existent cars, manufacturers and drivers</li>
  <li>Project supports CRUD (Create Read Update Delete) operations</li>
</ul>

## Getting Started
<ol>
  <li> Clone this reprositority</li>
  <li> Initialize data base with SQL script that located in <code>src/main/resources/init_db.sql</code></li>
  <li> Establish connection to your SQL database</li>
  <li> Build project using Maven <code> mvn clean install</code></li>
  <li> Deploy the WAR file to a servlet container (for example Tomcat)</li>
  <li> Navigate to <code>http://localhost:8080/taxi_service_war_exploded/</code> in your web browser to access the taxi service</li>
  <li> Create a new Driver at <code>http://localhost:8080/taxi_service_war_exploded/drivers/add</code> to get acces to various functions of Taxi-Service</li>
</ol>

## Structure
<ul>
  <li>controller - contains servlet that handle various HTTP requests</li>
  <ul>
    <li>IndexController - shows all aviable pages</li>
    <li>LoginController - authentication to Taxi-Service</li>
    <li>LogoutController - exit from current driver account (invalidate current session)</li>
    <li>AddCarController - add new car</li>
    <li>AddDriverToCarController - add driver to existent car</li>
    <li>DeleteCarController - delete existent car</li>
    <li>GetAllCarsController - display all cars</li>
    <li>AddDriverController - add new driver</li>
    <li>DeleteDriverController - delete existent driver</li>
    <li>GetAllDriversController - display all drivers</li>
    <li>GetMyCurrentCarController - display all cars belonging to the current driver</li>
    <li>AddManuctarurerController - add new manufacturer</li>
    <li>DeleteManufacturerController - delete existent manufacturer</li>
    <li>GetAllManufacturersController - display all manufacturers</li>
  </ul>
  <li>dao - contains Data Access Object interfaces and their implementations</li>
  <li>exception - contains custom exceptions</li>
  <li>lib - contains injector</li>
  <li>model - contains structure that represent car, driver, manufacturer objects</li>
  <li>service - contains service interfaces and their implementations that perform business logic</li>
  <li>util - to establish connection to database</li>
  <li>web.filter - contains filter to prevent access of unregistered drivers</li>
  <li>resources - contains sql-script to create scheme and tables of taxi-service</li>
  <li>webapp - contains web resourses like JSP and CSS files</li>
</ul>

## Used technologies
<ul>
  <li>Java <code>v.17.0.5</code></li>
  <li>Maven <code>v.3.8.6</code></li>
  <li>JDBC <code>v.4.2</code></li>
  <li>MySql <code>v.8.0.24</code></li>
  <li>Java Servlets <code>v.4.0.1</code></li>
  <li>Tomcat <code>v.9.0.73</code></li>
</ul>

## Authors
<a href="https://github.com/RandomEastEcho">Gleb Iaroshevych</a>
