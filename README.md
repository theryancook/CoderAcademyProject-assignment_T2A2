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

