# SFG

ESP- Enterprise Service protocol
SI- Sterling Integrator

http://jau-dd7dff74eeb:50000/dashboard/
User id - admin
password - password


http://jau-dd7dff74eeb:50000/dashboard/portal



TCS-XML-COLLECT THE FILE, CHECK IF XML, TRNSALTE THE DATE, RENAME THE FILE, SEND TO MAINFRAME
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
- click on checkout, Click on on cancel and then click checkin go,
-  file name- browse file name hellowworkld
- Description second version
- click on next, next next, chooser version ,click on next and click on finish
- click on return,clickk on exectue manager and click on execute ,click on go
- you can see now 2 assign statment in SI

  
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
    to            YY
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
           or
         <assign to="YY" from ="FirstSession"></assign>
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

  or
  
  <ProcessData>
    <FirstSession>HelloWorld</FirstSession>
    <Jay>GoodBatch</Jay>
     <yy>
        <FirstSession>HelloWorld</FirstSession>
     </yy>                
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
- Name- OrderType, click on expression
- Expression - OrderType/text()='webOrder'
- click on ok,ok select ordertype,click on okay
- selct the arrrow which is linking choice start and sequence start
-  click on add
- give value webOrder

choice start:
----------------
add another sequence start --- assign --sequence end

start --sequence-start-- assign- choice start--- weborder --- assign --sequence end- choice end- sequence end- end
                          OrderType   ------|                                               |
                                             --- Other type orders --- assign --sequence end---

                                              
- selct the arrrow which is linking choice start and sequence start
- name        value
Ordertype     true

- selct the arrrow which is linking choice start and sequence start
- name        value
Ordertype     false

- click on same  assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      This is not web order
    from          
    to            NotFound


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

Business process ID
---------------------
- click on business process, click on monitor, clck on centeral search
- In business process, give HelloWorld
-  You will see 3 business process matches in sterling b2b integrator as we run 3 timeds yesterday
-  

- click on monitor, click on current process
- you can see all business process with id

If there is any issue, With the business process
- click on monitor, click on advanced search, click on business process
- process id -715018
- click on 715018
- you can see the assign servicess logss

- variable is create inside the processdaya
  <ProcessData>
    <FirstSession>HelloWorld</FirstSession>
    <Jay>GoodBatch</Jay>
  </ProcessData>

  
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





Session3_ Activities On Fault Loop All start ALL
=================================================

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


START - Sequentstart- assign-choicstart-sequencestart-assing- repeat-sequence end - choicend- squence end- end

- click on tools, click on rule manager
- click on add
- Name- testLoop, click on expression
- Expression - x/text()<5 
- click on ok,ok select ordertype,click on okay
- selct the arrrow which is linking choice start and sequence start
-  click on add
- give name testloop


- selct first choice 
- name        value
Ordertype     looptest?


-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      0
    from          
    to             x
- click on file, click on save



-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      
    from           x+1
    to             x
- click on file, click on save



-  click on repeat and double click, it will paramaeters to configure the activity
   Name      value
   ref       looptest?
   
- click on file, click on save




- click on build , click on validate
- click on file, click on save as DecisionBP
- click on view, click on  source copy the code
- 
If you have the XML code  you  can do it without GPM.
==============================================================
- now, click on Manager,click on go near  process definition
  Process Name
- Name: looptest
       check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, nextclick on finish

- now, click on Manager, In process name- serach for Helloworld, you will see looptest
- click on execute
- click on go
-

click on monitor, click on advanced search, click on business process
- process id -715018
- click on 715018
- you can see the assign servicess logss

- variable is create inside the processdaya
  <ProcessData>
    <FirstSession>HelloWorld</FirstSession>
    <Jay>GoodBatch</Jay>
  </ProcessData>



  34:26
  

                                      - seqstart-- assign- sequenceend- 

start   -- sequence start --all start -seqstart  - assign- sequenceend-   allend--sequebcebd-end

                                       -seqstart -assign- sequenceend- 

-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant     firstflow
    from          
    to             x1
- click on file, click on save


-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant     secondflow
    from          
    to             x2
- click on file, click on save


-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant     thirdflow
    from          
    to             x3
-
-  click on file, click on save



  -  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant     At the End
    from          
    to             lastAssign
-
-  click on file, click on save


<process name  ="ALLstartALL end"?
<seq>
  <all>
    <seq>
      <assing to ="x1">1111</assug>
    </seq>
      <seq>
      <assing to ="x1">2222</assug>
    </seq>
   <seq>
      <assing to ="x1">3333</assug>
    </seq>
 </all>
 <assunbg to "lastassing">at the nd<a/assiung>
 </seq>
</process>




In other case- Error handling:
-
- click on view, click on stencil, click on applications, click on all services

- start -sequence start -file system adapter -assign- sequence end- end
                        -Onfaultgroup
                                         onfault start- sequence start- assign- sequence stop- enonfault end
  
- click on file system adapter
  Name- file system adapter
  config- AS3FSAdapter

  Message to Service  Messsage from servcie

  click on Message to service

  output Msg
  Message name

 name                 value        usxpath          append
 action             collection
 cllectionfolder    c:/test/
 bootstrap           no
 collectionmultiple  no
 deleteafter collect no
 filter              abc.txt



   -  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant     this will run after FSA
    from          
    to             lastAssign
-
-  click on file, click on save



   -  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant     this will run if fsa failed
    from          
    to             onfault
-
-  click on file, click on save



Session 4 Doc TO DOM DOM TO DOC BP persistance
===============================================



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

START----- Sequence start------ assign-------assign----assign----Sequence end---- End


-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      55
    from          
    to             x
- click on file, click on save




- click on build , click on validate
- click on file, click on save as PrimaryDocument
- click on view, click on  source copy the code
- 
If you have the XML code  you  can do it without GPM.
==============================================================
- now, click on Manager,click on go near  process definition
  Process Name
- Name: PrimaryDocument
        check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, nextclick on finish

- now, click on Manager, In process name- serach for PrimaryDocument, click on executiion manager
- 
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-
  <?xml version="1.0" encoding="UTF-8"?>
  <ProcessData>
    <PrimaryDocument>SCIObjectID ="AJFJADFJAJFAJJAJJAJ> </PrimaryDocument> 
  </ProcessData>



-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant      
    from          PrimaryDocument/@SCIObjectID
    to             Document1
- click on file, click on save


-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant       
    from          PrimaryDocument/@SCIObjectID
    to             x2
- click on file, click on save

- click on build , click on validate
- click on file, click on save as PrimaryDocument
- click on view, click on  source copy the code

  <Process name "defailt >
    <sequence>
     
      <assign to= "Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"></assin>
      <assign to "x2" from=" PrimaryDocument/@SCIObjectID"></assign>
      
    </sequence>
  </Process>


If you have the XML code  you  can do it without GPM.
==============================================================
- now, click on Manager,click on go near  process definition
  Process Name
- Name: PrimaryDocument
        check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, nextclick on finish

- now, click on Manager, In process name- serach for PrimaryDocument, click on executiion manager
- 
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-

- now go to click on Manager, In process name- serach for PrimaryDocument,
- click on source manager
- click on edit
- short description
- paste the xml code
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-


    <?xml version="1.0" encoding="UTF-8"?>
  <ProcessData>
    <PrimaryDocument>SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/> 
     <Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"/>
     <x2 SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/
  </ProcessData>



Now if you have this order file
--------------------------------------
<order>
  <orderType>web</orderType></orderType>
  <itemName>12223</itemName>
  <userName>JP</userName>
</order>




-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant       
    from          DocToDom(PrimaryDocument)
    to             .
- click on file, click on save

- click on build , click on validate
- click on file, click on save as PrimaryDocument
- click on view, click on  source copy the code


 <Process name "defailt >
    <sequence>
     
      <assign to= "Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"></assin>
      <assign to "x2" from=" PrimaryDocument/@SCIObjectID"></assign>
       <assign to "." from=" DocToDom(PrimaryDocument)"></assign>
    </sequence>
  </Process>



If you have the XML code  you  can do it without GPM.
==============================================================
- now, click on Manager,click on go near  process definition
  Process Name
- Name: PrimaryDocument
        check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, nextclick on finish

- now, click on Manager, In process name- serach for PrimaryDocument, click on executiion manager
- 
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-

- now go to click on Manager, In process name- serach for PrimaryDocument,
- click on source manager
- click on edit
- short description
- paste the xml code
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-


    <?xml version="1.0" encoding="UTF-8"?>
  <ProcessData>
    <PrimaryDocument>SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/> 
     <Docuemnt1" SCIObjectID ="AJFJADFJAJFAJJAJJAJ"//>
     <x2 SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/
   <order>
  <orderType>web</orderType></orderType>
  <itemName>12223</itemName>
  <userName>JP</userName>
  </order>
  </ProcessData>




-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant       
    from          DocToDom(PrimaryDocument/ordetType/text()
    to            XMLOrderType
- click on file, click on save

- click on build , click on validate
- click on file, click on save as PrimaryDocument
- click on view, click on  source copy the code


 <Process name "defailt >
    <sequence>
     
      <assign to= "Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"></assin>
      <assign to "x2" from=" PrimaryDocument/@SCIObjectID"></assign>
       <assign to "." from=" DocToDom(PrimaryDocument/ordetType/text())"></assign>
    </sequence>
  </Process>



If you have the XML code  you  can do it without GPM.
==============================================================
- now, click on Manager,click on go near  process definition
  Process Name
- Name: PrimaryDocument
        check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, nextclick on finish

- now, click on Manager, In process name- serach for PrimaryDocument, click on executiion manager
- 
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-

- now go to click on Manager, In process name- serach for PrimaryDocument,
- click on source manager
- click on edit
- short description
- paste the xml code
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-




    <?xml version="1.0" encoding="UTF-8"?>
  <ProcessData>
    <PrimaryDocument>SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/> 
     <Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"/>
     <x2 SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/
     <XMLOrderTypew>web</XMLOrderTypew>
  </ProcessData>






-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant       
    from          DocToDom(Document1)
    to            XMLOrderType
- click on file, click on save

- click on build , click on validate
- click on file, click on save as PrimaryDocument
- click on view, click on  source copy the code


 <Process name "defailt >
    <sequence>
     
      <assign to= "Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"></assin>
      <assign to "x2" from=" PrimaryDocument/@SCIObjectID"></assign>
       <assign to "XMLOrderType" from=" DocToDom(Document1)"></assign>
    </sequence>
  </Process>



If you have the XML code  you  can do it without GPM.
==============================================================
- now, click on Manager,click on go near  process definition
  Process Name
- Name: PrimaryDocument
        check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, nextclick on finish

- now, click on Manager, In process name- serach for PrimaryDocument, click on executiion manager
- 
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-

- now go to click on Manager, In process name- serach for PrimaryDocument,
- click on source manager
- click on edit
- short description
- paste the xml code
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-




    <?xml version="1.0" encoding="UTF-8"?>
  <ProcessData>
    <PrimaryDocument>SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/> 
     <Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"/>
     <x2 SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/
     <XMLOrderTypew>
    <order>
  <orderType>web</orderType></orderType>
  <itemName>12223</itemName>
  <userName>JP</userName>
  </order>
     </XMLOrderTypew>
  </ProcessData>




-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant       
    from          DomTodOC(ProcessData)
    to            test
- click on file, click on save

- click on build , click on validate
- click on file, click on save as PrimaryDocument
- click on view, click on  source copy the code


 <Process name "defailt >
    <sequence>
     
      <assign to= "Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"></assin>
      <assign to "x2" from=" PrimaryDocument/@SCIObjectID"></assign>
       <assign to "test" from=" DocToDom(ProcessData)"></assign>
    </sequence>
  </Process>



If you have the XML code  you  can do it without GPM.
==============================================================
- now, click on Manager,click on go near  process definition
  Process Name
- Name: PrimaryDocument
        check in business process created by the graphical modeling tool
 choose Business process texteditor
- click on next
- Description- Give your descript
  business process- here copy paste your xml code
- click on next, next, next, nextclick on finish

- now, click on Manager, In process name- serach for PrimaryDocument, click on executiion manager
- 
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-

- now go to click on Manager, In process name- serach for PrimaryDocument,
- click on source manager
- click on edit
- short description
- paste the xml code
- click on execute
- click on browse, add your test.xml code from your computer
- click on go
-


- you will see everything what is inside the process data

    <?xml version="1.0" encoding="UTF-8"?>
  <PrimaryDocument>SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/> 
     <Docuemnt1" from =" PrimaryDocument/@SCIOjbectID"/>
     <x2 SCIObjectID ="AJFJADFJAJFAJJAJJAJ"/
     <XMLOrderTypew>
    <order>
  <orderType>web</orderType></orderType>
  <itemName>12223</itemName>
  <userName>JP</userName>
  </order>
     </XMLOrderTypew>



shortcut do as above only 

-  click on assign and double click, it will paramaeters to configure the activity
    Name         value
    append       false
    constant       
    from          DomTodOC(ProcessData/XMLOrderType/Order)
    to            test
- click on file, click on save



  <?xml version="1.0" encoding="UTF-8"?>
  <orderType>web</orderType></orderType>
  <itemName>12223</itemName>
  <userName>JP</userName>


  1:29:50
