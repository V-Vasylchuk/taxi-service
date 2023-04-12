# ![logo.png](logo.png)Taxi - Service![logo.png](logo.png)
This web application is designed to imitation taxi service. 
The user(driver) can add vehicle manufacturers, add car models, add drivers, connect drivers and cars
## Features
- Authentication
- Create and delete car manufacturer
- Create and delete cars
- Create and delete drivers
- Add drivers to specific cars
- View all cars belonging to the current driver
- View all cars, drivers, manufacturers
## How to start?
- Clone the project repository to your local machine
- Run the SQL script located in `src/main/resources/init_db.sql` to initialize the database
- Replace the values of the `URL`, `USERNAME`, `PASSWORD` and `JDBC_DRIVER` properties with the appropriate values for your database setup
- Build the project using Maven: `mvn clean install`
- Deploy the generated WAR file to servlet container such as Tomcat
## Project structure:
- **controller: Servlets that handle HTTP requests and responses**
    -  LoginController - `POST` `/login` - authentication
    -  LogoutController - `GET` `/logout` - invalidate current session
    -  IndexController - `GET` `/index` - show all corresponding pages
    -  AddCarController - `POST` `/cars/add` - adds a new car
    -  AddDriverToCarController - `POST` `/cars/drivers/add` - adds a driver to a certain car
    -  DeleteCarController - `GET` `/cars/delete` - deletes car
    -  GetAllCarsController - `GET` `/cars` - views all cars
    -  AddDriverController - `POST` `/drivers/add` - adds a driver
    -  DeleteDriverController - `GET` `/drivers/delete` - deletes driver
    -  GetAllDriversController - `GET` `/drivers` - views all drivers
    -  GetMyCurrentCarsController - `GET` `/drivers/cars` - views all cars for the current driver
    -  AddManufacturersController - `POST` `/manufacturers/add` - adds new manufacturer
    -  DeleteManufacturerController - `GET` `/manufacturers/delete` - deletes manufacturer
    -  GetAllManufacturersController - `GET` `/manufacturers` - views all manufacturers
- **dao: Data Access Object interfaces and their implementations**
- **filter: Servlet Filters used to intercept requests and responses**
- **model: Plain Old Java Objects (POJOs) that represent data**
- **service: Service interfaces and their implementations that perform business logic**
- **util: Utility class used in a project to create a database connection**
- **resources: Non-Java files such as database scripts and configuration files**
- **webapp: Contains web resources such as CSS, and JSP files**
- **WEB-INF: Contains configuration files for the web application**
- **views: Contains JSP files used as views in the application for cars, drivers, manufacturers, authentication**
## Used technologies:
- Java `v.17.0.5`
- Maven `v.3.8.6`
-  JDBC `v.4.2`
-  MySql `v.8.0.28`
-  Java Servlets `v.4.0.1`
-  Tomcat `v.9.0.73`
## Author:
_Vasyl Vasylchuk_