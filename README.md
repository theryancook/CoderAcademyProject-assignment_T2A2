## T2A1 Workbook - Ryan Cook

### Q1 - Describe the architecture of a typical Rails application.

The Model in MVC is responsible for the relationship between objects and the database. The Model inherits its capability from ActiveRecord (which is a predefined class within Rails) that enables the retrieval, saving, editing and deletion of data from a table within a given database. Model objects act as a layer between the application and the database. Models are also able to manage validation and any associations between other Models.

The View is the front end part of the application. Views are the part of the application which tells Rails which HTML content should be sent back to the browser after each request & how to render the response. The unique thing about the Views in Rails, is that you can embed Ruby within HTML and have those languages interact together within the browser.

The Controller contains the information on how the Models and the Views interact with each other. It directs traffic within your app by querying Models for required data, as well as organising that data into the required format for the View.

### Q2 - Identify a database management system (DBMS) commonly used in web applications (including Rails) and discuss the pros and cons of this database

I’ve decided to take a look at the pros and cons for the DBMS SQLite.

As the name suggests, SQLite is a very light weight database. What this means, is that it is well suited for use in devices that require embedded software such as televisions & mobile phones, as well as certain web applications, such as the proposed Marketplace Web App. It has fantastic performance due to being ‘lite’. This is achieved by only loading data which is needed, rather than reading the entire file. If you edit small parts, it will only overwrite the parts of the file which were changed. SQLite is also very reliable as it updates your content continuously, which means little work would be lost in the case of power failure or a system crash. Another big advantage is portability. SQLite is portable across all 32-bit and 64-bit operating systems, as well as being able to be used with all programming languages without any compatibility issues. It’s uncomplex and can reduce cost because the content can be accessed and updated using concise SQL queries instead of lengthy procedural queries.

The main disadvantages are that it does not do well when handling a high volume of HTTP requests, and that the size of the database is almost always restricted to 2GB.

### Q3 - Discuss the implementation of Agile project management methodology

As you are surely aware, there are a couple of different options for us to go in terms of the methodology used to manage the project. Namely, we could go with either Waterfall or an Agile methodology. Taking into consideration the scope of the project, I propose that we’d move forward using an Agile project management methodology.

There’s a couple of different reasons for this decision. Firstly, this enables us to keep our development very flexible. In my experience, the spec and the requirements from the client (yourself) may change over time, or need to be tweaked. Using Agile, we’ll have no issue to incorporate those new decisions into the development. Being flexible also helps us on our end. If we run into any roadblocks, we’re able to be creative and flexible in terms of the solution. This will help save time for both parties, as well as keeping the overall cost of the project down, ultimately saving you both time and money.

Secondly, Agile will also let us be able to be more iterative, and present to you the software as it becomes available. You won’t need to wait for the entire project to be finished to be able to first have users test and see the product. Based on your feedback and consultation, we’ll then be able to make improvements and changes mid development, as well as be able to change development priorities around what you feel as though is most important.

Thirdly, since we’ll be using fortnightly sprints, you’ll also have access to very current updates on the status of the project and whether time estimates are being adhered to. This will ensure we’re able to be very transparent about the progress and ultimate success of the project.

### Q4 - Provide an overview and description of a standard source control workflow

There’s a couple of different ways teams can manage their source control workflow, but one method that I've seen work well in practice is the Feature Branch Workflow.

How it works, is that the master branch is considered to be the source of truth as the main code base. If any work is to be done to the main code base, such as a new feature, this work would take place on a completely separate branch. This separate branch would then be merged back into the main code base once it’s been tested and given the tick of approval.

The workflow for creating a new feature would therefore look something like, firstly, creating a new branch. All work done on this feature is then pushed onto this branch for the time being. Others may also be working on this branch/feature at the same time, so it’s good practice to regularly pull and push updates to what you’ve done. Once it’s looking pretty solid, someone will create a Pull Request in order to have someone else review the code and get any feedback (perhaps from a Senior Developer or Team Lead). There may be some back and forth here, making some final tweaks to the submitted code. Once the PR has been accepted, the code then needs to be merged from the feature branch into the master branch and voila, we have a newly implemented feature for you!

### Q5 - Provide an overview and description of a standard software testing process (e.g. manual testing)

A typical software testing process can be broken down into 6 different elements - requirement analysis, test planning, test case development, environment setup, test execution and finally test cycle closure.

Requirement analysis is the first phase, and involves going through the proposed requirements of the feature in order to determine the testable requirements. This process usually involves stakeholders across the business & the client themselves.

Test planning is the logical next step. The QA manager (or other responsible person) develops a test plan, as well as a test strategy. This includes the approach, resource planning, tooling and documentation.

Test case development involves the QA team writing the test cases. Testing may be able to be automated with scripts, or done manually by the QA team.

As the name suggests, test environment setup includes installing the required software and/or hardware components to be able to complete the testing of the application. This environment itself is then also tested in order to verify it’s working as per requirements.

Moving onto the test execution phase, this is where QA runs the test cases and reports any bugs that come up during this process. Bugs are passed onto the developers, who attempt to fix the bugs, and then the code is retested in the same environment to ensure they are fixed properly.

The final part of the cycle is the test closure. This is an important aspect of the testing cycle where we reflect on what worked well, what didn’t and how we can improve the process in the future.

### Q6 - Discuss and analyse requirements related to information system security and how they relate to the project

According to the Australian Attorney-General’s Office, there are 4 main requirements to take into consideration when you’re looking at information security. 

The first requirement is concerning sensitive and classified information. What this means is that we must identify what information we’re holding & collecting, then analyse the sensitivity of that data. Depending on those assessments, we’ll scope out and implement the appropriate controls for the Marketplace App. 

The 2nd main requirement is access to information. This concerns how we plan to share information with relevant parties (namely, users). If any information is particularly sensitive, also ensuring that only people who need to see this information can do so. This could be managed in the app by implementing an identity management system, and only providing the minimum level of permissions necessary. 

The third requirement is safeguarding information from cyber threats. This includes developing a strategy to respond to, and mitigate cyber attacks to the entity (app). This is done by following established best practices in the area. As an example for the Marketplace app, we would be backing up all data on a separate system so that if we are ever compromised (by ransomware for example), we can move straight onto the backup without impacting users. 

Lastly, we must have robust ICT systems. This requirement means that it's imperative for strict security measures to be in place for all stages of development. There are industry standard guidelines to follow, and we plan to do so for the Marketplace app.


### Q7 - Discuss common methods of protecting information and data and how you would apply them to the project

In the context of building the Marketplace app, there are a lot of things to consider to create a secure and safe product.

The app is driven by users, and as a result we’re going to be asking for a lot of user input. This is somewhere applications have been susceptible to cyber attacks in the past. It would be imperative for us to implement some form of data validation on those user inputs. There are different elements that we’re able to validate for: the data type & specific data values, as well as the format of the data. For this app specifically, as an example, we’d be ensuring that prices were in realistic ranges & are numbers, we can reference addresses against a real database of addresses & verifying the name of buyers and sellers only contain letters & not special characters etc.

Authentication is another way in which we can protect both ourselves and the users. Authentication is the practice of setting up user accounts with specific permissions associated with those accounts. Since we’re going to be facilitating exchange between users, we want to be able to guarantee the users are who they say they are. In the app, we’ve got a couple of authentication measures we’d implement. Firstly for the accounts themselves, users would be required to use advanced passwords including special characters, capitals, minimum lengths etc. We’d require a 2nd form of identification in the form of government issued ID upload, as well as email account verification. Beyond account creation, the permissions of users once their account is created would be the absolute bare minimum in order to functionally use the app. This means that there’s less avenues for us to be attacked, and if an account is compromised, the hacker would have a limited scope in which to attack us & the users.

### Q8 - Research what your legal obligations are in relation to handling user data and how they can be met for the project

The Australian Government has a detailed outline available online of legal obligations for handling user data. While it would be impractical to go through the whole list of requirements, i’ll highlight some key requirements and how these would be met for the Marketplace app.

For error handling, sensitive information including system details, session identifiers and account information in error responses is to be withheld from error pages. For authentication and identity management, all passwords and authentication tokens are to be sent over an encrypted connection (for example, SSL). Temporary passwords (or links to temporary passwords) are an exception, which may be transmitted unencrypted. For file management, security-relevant data (for example, passwords & connection strings) are stored server-side rather than client-side. For session management, logout mechanisms must be available to users from all screens that are protected by authorisation, in order to terminate the associated session or connection.

Rails has some of this functionality built in, and for what’s not available in Rails, other methods for following and implementing these guidelines will be followed.

By following these guidelines, it saves both parties from any legal implications, as well as being a good foundation for the overall security of the application.

### Q9 - Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure.

As the name suggests, relational databases are a type of database that stores data points that are related to one another. In a relational database, you have tables that store all the data. Each row in the table is a record with a unique identifier, known as a ‘key’. Since these tables are split up into rows and columns, combined with this unique ID, it’s easy to establish relationships with the data & it’s possible to reference these unique keys across many different data tables.  An important aspect of the structure itself, is that the data structures (the data tables, views & index) are totally separate from the physical storage structures. This means that database administrators are able to manage the physical storage of the data, without impacting any logical data.

### Q10 - Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database.

When we’re referring to data integrity we’re not talking about data security or data quality, we’re looking at the consistency, the accuracy and the completeness of the data.

Different types of data integrity in a relational database include entity integrity, referential integrity, domain integrity and user defined integrity. 

For entity integrity, we’re ensuring that we do not have duplicates of data sitting across our database. This is achieved through the use of primary keys which are unique to each piece of data. 

Referential integrity refers to how our data is manipulated in our database. By creating a set of rules about how data is stored, updated, referenced etc we’re able to keep a really clean and uniform database that we know is accurate. 

Domain integrity is similar, but is more focused on the type of data that can be input. By setting a specific data field to only accept numbers for example, we can avoid false or incorrect data being put into our database. 

User defined integrity refers to any other data integrity we implement, that we feel as though would assist us in our specific case. Since our marketplace app will be different to other Marketplace apps (and other apps in general), it would make sense to add in various extra measures beyond what we’ve discussed but make sense in our own unique context.

### Q11 - Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database.

To look at the ways in which data can be manipulated in a relational database model, it’s important to understand there are key differences between the 2 different database model types. 

SQL is a commonly used language across relational databases. If you’re looking to make any changes to the data (adding, removing etc) you can write those commands using SQL. There are 3 main ways in which you can manipulate the data - you can change which data is being displayed, you can change how the data is being displayed, or you can modify the data itself. There are specific predefined values in SQL such as INSERT, UPDATE or DELETE which enable the user to interact with and modify the data. 

In the other type of database, NoSQL (which are non-relational databases), there’s no specific query syntax. Instead of using tables, NoSQL databases may take the form of key-value, wide-column or graph (just to name a few). 

Some of the other key differences include that SQL databases are vertically scalable, whereas NoSQL are horizontally scalable. SQL requires a predefined schema, whereas NoSQL uses a dynamic schema. SQL also requires specific database hardware.

### Q12 - Identify and explain the workings of TWO sorting algorithms and discuss and compare their performance/efficiency (i.e. Big O)

While there are many more than just two different sorting algorithms, the two that i’m going to explore further are Bubble Sort and Selection Sort.

Bubble Sort is a very simplistic algorithm. How it works is that, starting at index position 0, it moves up 1 index position as it iterates through the list. As it iterates, it’s making a comparison of the adjacent numbers. If the number at index position i + 1 is less than (<) index position i, it will swap those numbers so that i + 1 is greater than (>) i. It will then iterate onto the next index position, and do the same thing. Once the algorithm has gone through the whole list, it will then start again at the start of the list and repeat this sequence, until it goes through the whole list without having to make any swaps. This is when we know that this particular list is sorted.

Now looking at Selection Sort, it works in a slightly different way. Here, the original list is divided up into 2 parts - an unsorted part, and a sorted part. Initially the sorted part is empty, and every item in the list is placed into the unsorted part. You iterate through the whole unsorted part, until you’ve determined the smallest item by the end. Once this is identified, this item is placed in the left-most position of the sorted portion of the list. This process is repeated on the unsorted list to find the next smallest item, which is placed 1 to the right of the smallest item in the sorted list. This is then repeated, until eventually each smallest item has been placed into the sorted list, in order from smallest to the largest. This could also be done in reverse from largest to smallest.

Looking at a comparison of the 2, while Bubble Sort is simple, it’s also very slow and considered to be impractical for most applications. It has a time complexity of O(n²). Similarly, selection sort also has a time complexity of O(n²). The reason for this is that in both scenarios, we have to go through the list n number of times to be able to complete the sorting. There are more efficient alternatives out there.

### Q13 - Identify and explain the workings of TWO search algorithms and discuss and compare their performance/efficiency (i.e. Big O)

While there are many more than just 2 different search algorithms, the two that i’m going to explore further are Binary Search and Linear Search.

Binary Search is a common search methodology. The key idea behind Binary Search is that you find the middle point of a sorted list. You then compare whether that middle number is higher or lower than the number we’re looking for, and if the middle number is higher for example, you can remove every single number to the right of that number in the list as the numbers on the right hand side are all going to be higher. Every iteration, you’re able to remove half of the numbers you’re searching through.  You repeat this process until you hit on the number you’re searching for. It’s important to note that the list must already be sorted before being able to use a Binary Search.

Another type of search that you’re able to perform is a Linear Search. This is a very simplistic type of search. Starting at index position 0, you move through list 1 by 1, until you reach a point when the number you’re searching for is equal to the number in the list, or you reach the end. The list does not need to have any particular order for this type of search to work.

Comparing the 2 different types of searches, there’s really 2 key differences. At each step in a Binary Search, we’re able to remove half of all possibilities. This means that the time complexity is going to be significantly lower than a linear search. A Binary Search has the time complexity of O(log n), whereas the time complexity of a linear search is O(n) (which carries a higher cost). The other big important difference is that in order to use a Binary Search algorithm, the data in the list needs to be sorted. You do not have that prerequisite for a Linear Search function, as it’ll iterate over every value regardless of whether it’s sorted or not.

### Q14 - Conduct research into a marketplace website (app) and answer the following parts: 
###  a. List and describe the software used by the app.
###  b. Describe the hardware used to host the app.
###  c. Describe the interaction of technologies within the app
###  d. Describe the way data is structured within the app
###  e. Identify entities which must be tracked by the app
###  f. Identify the relationships and associations between the entities you have identified in part (e)
###  g. Design a schema using an Entity Relationship Diagram (ERD) appropriate for the database of this website (assuming a relational database model)

I chose the Marketplace website (app) 'Gumtree'
#### a. List and describe the software used by the app.
According to the website Stackshare, Gumtree uses the following software stack:
* jQuery - Javascript library
* NGNIX - Web server
* React - Javascript library for the front end
* Bootstrap - CSS framework
* jQuery UI - Javascript library for the front end
* Mondernizr - Javascript library
* Amazon Cloudfront - CDN offered by AWS

####  b. Describe the hardware used to host the app.
Stackshare also reveals that Gumtree is hosted using Google Cloud Platform (GCP). It’s hard to determine specifically the hardware that GCP uses (beyond the general fact that it includes computers, hard disk drives, solid state drives and networking), but what we do know is that there’s a range of distributed server locations, including here in Sydney.

####  c. Describe the interaction of technologies within the app
Using the list of software and hardware provided so far - A user would firstly visit the website (app). The UI of the app, what users can see, would have in part been or wholly created using Bootstrap & jQuery UI. When the user clicks on the search bar, or uses any type of functionality, they would be interacting with Javascript written using the React framework & jQuery. Modernizr is also working in the background to make sure the browser supports all features and so the user has a seamless experience. All this information has to be hosted somewhere, and we know that Gumtree uses GCP. To make sure the site can handle increased usage of features and higher traffic at any time, NGINX is the software used on the web server. Finally, CloudFront is a CDN which ensures larger media files (images, videos etc) are cached somewhere locally for users around the world.

