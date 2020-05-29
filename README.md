## T2A1 Workbook - Ryan Cook

### Q1 - Describe the architecture of a typical Rails application.

The Model in MVC is responsible for the relationship between objects and the database. The Model inherits its capability from ActiveRecord (which is a predefined class within Rails) that enables the retrieval, saving, editing and deletion of data from a table within a given database. Model objects act as a layer between the application and the database. Models are also able to manage validation and any associations between other Models.

The View is the front end part of the application. Views are the part of the application which tells Rails which HTML content should be sent back to the browser after each request & how to render the response. The unique thing about the Views in Rails, is that you can embed Ruby within HTML and have those languages interact together within the browser.

The Controller contains the information on how the Models and the Views interact with each other. It directs traffic within your app by querying Models for required data, as well as organising that data into the required format for the View.

### Q2 - Identify a database management system (DBMS) commonly used in web applications (including Rails) and discuss the pros and cons of this database

I’ve decided to take a look at the pros and cons for the DBMS SQLite.

As the name suggests, SQLite is a very light weight database. What this means, is that it is well suited for use in devices that require embedded software such as televisions & mobile phones, as well as certain web applications, such as the proposed Marketplace Web App. It has fantastic performance due to being ‘lite’. This is achieved by only loading data which is needed, rather than reading the entire file. If you edit small parts, it will only overwrite the parts of the file which were changed. SQLite is also very reliable as it updates your content continuously, which means little work would be lost in the case of power failure or a system crash. Another big advantage is portability. SQLite is portable across all 32-bit and 64-bit operating systems, as well as being able to be used with all programming languages without any compatibility issues. It’s uncomplex and can reduce cost because the content can be accessed and updated using concise SQL queries instead of lengthy procedural queries.

The main disadvantages are that it does not do well when handling a high volume of HTTP requests, and that the size of the database is almost always restricted to 2GB.


