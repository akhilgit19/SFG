# SFG

ESP- Enterprise Service protocol
SI- Sterling Integrator

http://jau-dd7dff74eeb:50000/dashboard/
User id - admin
password - password


http://jau-dd7dff74eeb:50000/dashboard/portal

SI -Hello World Process:
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
==============================================================
- now, click on Manager,click on go near  process definition
  Process Name
- Name: Batch3HeloWorld2
       check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, nextclick on finish

- now, click on Manager, In process name- serach for Helloworld, you will see Batch3HeloWorld2
- click on execute
- click on go
- click on info on


-  click on assign ,drag it and put it in the white page
-  connect the dots between the points from assing  to sequence end

- click on annother assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      
    from          /ProcessData/FirstSession/text()
    to            yYY
- click on build , click on validate
- click on file, click on save
- click on view, click on  source copy the code

- now, click on Manager, In process name- serach for Helloworld, you will see Batch3HeloWorld
- click on source  manager
- click on edit
- Description 2222
- business process
   <process name='default'>
      <sequence>
        <assign to="FirstSession">HelloWorld</assign>
         <assign to="Jay">Good Batch</assign>
         <assign to="YY" from ="/ProcessData/FirstSession/text()"></assign>
      </sequence>
   </process>
- click on validate, click ok, click on finish, click on return, click on execution manager
- click on execute in 222 change, click on ok
- you can see the assign services

  <ProcessData>
    <FirstSession>HelloWorld</FirstSession>
    <Jay>GoodBatch</Jay>
     <yy>HelloWorld</yy>                
  </ProcessData>


- click on same  assign and double click, it will paramaeters to configure the activity
    Name         value
    append       true
    constant      1
    from          
    to            x

- click on same  assign and double click, it will paramaeters to configure the activity
    Name         value
    append       true
    constant      2
    from          
    to            x

- click on same  assign and double click, it will paramaeters to configure the activity
    Name         value
    append       true
    constant      3
    from          
    to            x
- click on build , click on validate
- click on file, click on save
- click on view, click on  source copy the code


- now, click on Manager, In process name- serach for Helloworld, you will see Batch3HeloWorld
- click on source  manager
- click on edit
- Description 222222
- business process
   <process name='default'>
      <sequence>
        <assign to="x" append="true">1</assign>
        <assign to="x" append="true">2</assign>
        <assign to="x" append="true">3</assign>
      </sequence>
   </process>
- click on validate, click ok, click on finish, click on return, click on execution manager
- click on execute in 222 change, click on ok
- you can see the assign services
  <ProcessData>
    <x>1</x>
    <x>2</x>
    <x>3</x>
  </ProcessData>


- you can add another sequence start --- assign --sequence end

eg
start --sequence-start-- assign- choice start- sequence start --- assign --sequence- choice end- sequence end- end

- click on same  assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      web order form
    from          
    to            Found

- click on tools, click on rule manager
- click on add
- Name- Ordertype, click on expression
- Expression - orderTupe/text()='webOrder'
- click on ok,ok select ordertype,click on okay
- selct the arrrow which is linking choice start and sequence start
- value webOrderFound
- click on add

choice start:
----------------
add another sequence start --- assign --sequence end

start --sequence-start-- assign- choice start- sequence start --- assign --sequence end- choice end- sequence end- end
                                            |                                               |
                                              sequence start --- assign --sequence end---

                                              
- selct the arrrow which is linking choice start and sequence start
- name        value
Ordertype     true

- click on same  assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      This is not web order
    from          
    to            Found


- click on build , click on validate
- click on file, click on save as DecisionBP
- click on view, click on  source copy the code
- 


- now, click on Manager,click on go near  process definition
  Process Name
- Name: DecisionBP
       check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- 1111
  business process- here copy paste your xml code
- click on next, next, next, next, click on finish

- now, click on Manager, In process name- serach for  DecisionBP, you will see  DecisionBP
- click on execute manager, click on exeucte
- click on go
- click on info on

SI -Session BP Activities
----------------------
- open cmd promt and run as administrator
- cd cd:\SI Install\install\bin
- stopWindowsService.cmd  ( to stop the sterling intergrator )(In unix you can use hardstop.cmd)
- startWindowsService.cmd (it will take the back up of log files and preserve in archieve folder)
- LOGS_Sat08_18_2018_12140 archive file of old logs
- 


- click on business process, click on monitor, clck on centeral search
- In business process, give HelloWorld
-  You will see 3 business process matches in sterling b2b integrator as we run 3 timeds yesterday
-  

If there is any issue, With the business process
- click on monitor, click on advanced search, click on business process
- process id -715018
- click on 155018
- you can see the assign servicess logss

- variable is create inside the processdaya
  <ProcessData>
    <FirstSession>HelloWorld</FirstSession>
    <Jay>GoodBatch</Jay>
  </ProcessData>

  




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
