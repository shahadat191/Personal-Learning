<h2> Communicating Between Services </h2>
<ul>
  <li>RPC - Remote Procedure Call </li>  
  <li>SOAP - Remote Procedure Call </li>  
  <li>REST - Represent</li>
  <li>Messaging</li>
 </ul>
 
 <h2> Messaging </h2>
 Example - Mail Service 
 
 Messaging Patterns
 
 Point-To-Point
 
 Service ---RegisterOrderCommand---> Service
 
 RPC
 
 Service <-------------> Serice
 
 Event Broadcasting
 
            ------- Service
            ------- Service
 Service-----
            ------- Service
            ------- Service
            
            
Microservice vs MSSQ

Microservice
  A software archtectural style
    Compose of small, highly decoupled independent processes.
   Focus on one task.
   Message broker -> Not required same programming language
