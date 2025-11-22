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
- click on Manager,click on go near run graphical process modeler   
- it will install grphical process modular
-  Graphic Process modular will open
-  click on file
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

- -  click on annother assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      GoodBatch
    from
    to             Jay
- click on file, click on save
  
- now, click on Manager,click on go near  process definition
  Process Name
- Name: Batch3HeloWorld
 choose check in business process created by the graphical modeling tool
        Business process texteditor
- click on next
- Filename- give the path ofHelloWorld.bp
- Description - this is BP for 3 SI Batch
- click on next, click on finish

- now, click on Manager, In process name- serach for Helloorld, you will see
- click on excution manager
- click on execute
- click on go
- click on info on


- now, click on Manager, In process name- serach for GoodBatch, you will see
-  click on check out click on go , click on edit
- click on source  manager
- click on execute
- click on go
- click on info on

  
- Now in Process Defintion check in
  Process Batch3HeloWorld
  file nam  --- click on browser
- select the helloworld bp
  clic on next, next next, chooser version ,click on next and click on finish
- click on retun,clickk on exectue ,click on go

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
