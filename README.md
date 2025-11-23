# SFG

ESP- Enterprise Service protocol
SI- Sterling Integrator

http://jau-dd7dff74eeb:50000/dashboard/
User id - admin
password - password


http://jau-dd7dff74eeb:50000/dashboard/portal

Hello World Process:
----------------------
Business processes
- Manager
   - Bussiness Process Manager
     Graphical Modeling
        run graphical process modeler      go
     create
        process definition                 go
     search
        process name                       go
     list
        alphabetically ALL                 go

- click on Business processes
- click on Manager,click on go near run graphical process modeler ,click on ok
- it will install grphical process modular , click on close, click on okay, user credentials
-  Graphic Process modular will open
-  click one view, click on stencil- click on BPML
-  click on file , click on new
-  click on start , drag it and put it in the white page
-  click on sequence start ,drag it and put it in the white page
-  connect the dots between the points from to start  to sequence start
-  click on sequence end ,drag it and put it in the white page

-  click on assign ,drag it and put it in the white page
-  connect the dots between the points from sequence start to  assign to sequence end
  
-  click on end , drag it and put it in the white page
-  connect the dots between the points from to sequence end to end
-  
-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      HelloWorld
    from
    to             FirstSession
- click on file, click on save

  
- now, click on Manager,click on go near  process definition
  Process Name
- Name: Batch3HeloWorld
 choose check in business process created by the graphical modeling tool
        Business process texteditor
- click on next
- Filename- give the path ofHelloWorld.bp
- Description - this is BP for 3 SI Batch
- click on next 3 times and , click on finish

- now, click on Manager, In process name- serach for Helloorld, you will see Batch3HeloWorld
- click on excution manager
- click on execute
- click on go
- click on info on


-  click on assign ,drag it and put it in the white page
-  connect the dots between the points from assing  to sequence end

- click on annother assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      GoodBatch
    from
    to             Jay
- click on file, click on save


- now, click on Manager, In process name- serach for Helloworld, you will see Batch3HeloWorld
- click on source  manager
- click on checkout and then click checkin go,
-  file name- browse file name hellowworkld
- Description second version
- click on next, next next, chooser version ,click on next and click on finish
- click on retun,clickk on exectue ,click on go

Now the new business process has checked in SI 
- now clic on view, click on source
- you will se XML code that GPM has generated  for you


If you have the XML code  you  can do it without GPM.

- now, click on Manager,click on go near  process definition
  Process Name
- Name: Batch3HeloWorld2
       check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, next
- Filename- give the path ofHelloWorld.bp
- Description - this is BP for 3 SI Batch
- click on next 3 times and , click on finish

- now, click on Manager, In process name- serach for Helloworld, you will see Batch3HeloWorld2
- click on execute
- click on go
- click on info on




- 
1:44:05

- Monitor
- Message Entry Workstation
- Trading partner
- Deployment
- services
- Installation Setup
- Configuration
- Schedules
- Maps
- Standards
- Extended Rule Libraries
- 
