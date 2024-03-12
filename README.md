# Welcome to Campus Area Network System Design!

![hello](https://github.com/LakshmiDeepak9653/resoures1/blob/main/wave.gif) Welcome to Campus Area Network System Project!
 We're thrilled to have you here.

this is a replication of a Campus LAN network of my collage <strong>RGUKT RK Valley</strong>. Did to test my CCNA Knowledge
>The main idea of my project is Replicate my campus LAN design with appropriate Features Like. Main Web server, Email server and DNS server and NTP server and Many more Features included in that design.

Before getting into the details of this project. Lets talk about some common LAN design principles and best practices i followed.
<details>
  <summary>1. Identifying the Needs and Goals</summary>
<div>
  <samp>
   <br>
    <p>
     Before staring the design of our LAN. we need to ask ourself some questions about our Project and find the Answers to them.
     Here are the Questions and my Answers to them as per this Project.
     <b><dl>I. What are the Main functions and applications of our LAN?</b></dl>
       <dt>The main idea of my project is Replicate my campus LAN design with appropriate Features Like. Main Web server, Email server and DNS server and NTP server and Many more Features included in that design</dt>.<br>
     <b><dl>II. How  many Users and devices will access your the Network?</dl></b>
       <dt>There are more than 6000 students and 300+ faculty and many more users are there. Network must be available to users as Wired or Wireless.</dt><br>
     <b><dl>III. What are the expected traffic patterns and bandwidth requirements?</dl></b>
       <dt>In our project we have two traffic patterns thats is faculty traffic and students traffic. The students must not access the faculty devices. The bandwidth requirements will the intra area communications (between the routers) must be fast.</dt><br>
     <b><dl>IV. How will we ensure security and privacy of your data?</dl></b>
       <dt>All the outside intiating connections must be stopped and incoming traffic must be checked.</dt><br>
     These questions will help you determine the scope, size, and structure of your LAN, as well as the hardware and software components you will need.  
    </p>
  </samp>
</div>
</details>
<details>
  <summary>2. Choose the Right Topology and Architecture</summary>
<div>
  <samp>
    <p>
     <br>
     The topology and architecture of our LAN refer to the physical and logical Layout of your network devices and connections.
     Here comes my Campus geographical View.<br>
     <img src="https://github.com/LakshmiDeepak9653/RKV-lan-resources/blob/main/Screenshot%202024-01-26%20124921.png">
     <br>
     By seeing this we can map the Physical Locations or regions of Networks. That are:-
     <strong><dl>Main Campus</dl></strong>
     <dt>1. Facdtty Quaters (6 Quaters)</dt>
     <dt>2. Library (2 Floors)</dt> 
     <dt>3. Lab Complex</dt>
     <dt>4. Academic Block - 1 (4 Floors)</dt> 
     <dt>5. Academic Block - 2 (4 Floors)</dt>
     <dt>6. Boys Hostel - 1 (4 Floors)</dt>
     <dt>7. Girls Hostel - 1 (4 Floors)</dt>
     <dt>8. Girls Hostel - 2 (4 Floors)</dt>
     <dt>9. Boys Hostel - 2 (4 Floors)</dt>
     <dt>10. Guest House</dt>
     <dt>11. C.S.E Department</dt>
     <dt>12. E.C.E Department</dt>
     <dt>13. M.M.E Department</dt>
     <dt>14. CIVIL Department</dt>
     <dt>15. MECH Department</dt>
     <dt>16. E.E.E Department</dt>
     <br>
     <strong><dl>Old Campus</dl></strong>
     <dt>1. PI Class Rooms</dt>
     <dt>2. MU Class Rooms</dt> 
     <dt>3. KAPPA Class Rooms</dt>
     <dt>4. LAMBDA Class Rooms</dt> 
     <dt>5. Girls Hostels RKV (Alpha/Beta)</dt>
     <dt>6. Girls Hostels ONG (Gamma/Delta)</dt>
     <dt>7. Boys Hostels RKV (Rho)</dt>
     <dt>8. Boys Hostels ONG (Teta)</dt>
     <dt>9. S.A.C Building</dt> 
<br>
   Based on the Physical Locations Create a Img that ressembles this LAN Network.<br>
   <img src="https://github.com/LakshmiDeepak9653/RKV-lan-resources/blob/main/rkv%20backgroundpng_Edited%20-%20Copy.png">
    </p>
  </samp>
</div>
</details>
<details>
  <summary>3. Select the appropriate devices and Technologies</summary>
 <div>
  <samp>
    <p>
     <br>
     We successfully design a Map of Network and now we need to choose the appropriate devices that will be a better suit for all network Sections (Physical Locations).<br>
     <br>We start from <b>Faculty Quaters, Hostels(Boys and Girls) and Guest House</b>. we use <b>wireless technologies(WiFi)</b>, Because These places are residance locations in the Campus where setting up a WiFi would be appropriate choice.<br>
     <br>Then Next one are <b>Students Classrooms(Academic Block 1 & 2, PI, MU, Kappa, Lamdba)</b>. Each one have more than 20 classes(each Academic Blocks has 100 classe rooms), but the students presence would be fixed(less than or equal to 100) so <b>Wired Network</b> would be appropriate.<br>
     <br>Next is a some Special Sections Where we need to use <b>Both Wired and Wireless Technolgies</b>. Wired Network to connect to the Departments inside the network sections and Wireless for students, Although students presence is not fixed. They are <b>Library, Lab Complex, CSE Dept, ECE Dept, EEE Dept, Civil Dept, Mech Dept, MME Dept.</b><br>
     <br>As we finished up the decision of technologies being used we fill up the topology with approriate devices in packet tracer.<br>
     that would look like this......<br>
     <img src="https://github.com/LakshmiDeepak9653/RKV-lan-resources/blob/main/deepak.png"></img>
   I think you have to zoom it for better clarity.......
    </p>
  </samp>
</div>
</details>
<details>
  <summary>4. Implement Network segmentation and Addressing</summary>
<div>
  <samp>
    <p>
     <br>
     Network segmentation and addressing are techniques that can help us organize and manage our LAN more effectively. Network segmentation is the process of dividing our LAN into smaller subnetworks, or subnets, based on logical criteria, such as function, location, or department. As per <b>RFC 1918</b> i use <b></b>10.0.0.0/8</b> subnet because i need to connect alot of devices this will provide me that Host address space and i will be using the <b>Subnet Mask of 255.255.255.0</b>  Which means i will be using <b>2^16 subnets</b> and <b>2^8 hosts</b> space. That would be lot more enough.<br>
    <br>Here comes the Address Scheme of This Network.
  <table>
<thead>
  <tr>
    <th align ="center"> Address Space </th>
     <th align="center"> Device </th>
   <th align="center"> Interface </th>
  </tr>
 <tr>
    <td align ="center"> 10.0.0.33 </td>
     <td align="center"> External Router </td>
   <td align="center"> G0/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.0.5 </td>
     <td align="center"> External Router </td>
   <td align="center"> G1/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.0.9 </td>
     <td align="center"> External Router </td>
   <td align="center"> G2/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.0.17 </td>
     <td align="center"> External Router </td>
   <td align="center"> G3/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.2.18 </td>
     <td align="center"> External Router </td>
   <td align="center"> G4/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.2.10 </td>
     <td align="center"> External Router </td>
   <td align="center"> G5/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.2.6 </td>
     <td align="center"> External Router </td>
   <td align="center"> G6/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.1.6 </td>
     <td align="center"> External Router </td>
   <td align="center"> G7/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.1.10 </td>
     <td align="center"> External Router </td>
   <td align="center"> G8/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.1.18 </td>
     <td align="center"> External Router </td>
   <td align="center"> G9/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.1.5 </td>
     <td align="center"> New Router </td>
   <td align="center"> G5/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.1.9 </td>
     <td align="center"> New Router </td>
   <td align="center"> G6/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.5 </td>
     <td align="center"> New Router </td>
   <td align="center"> G7/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.9 </td>
     <td align="center"> New Router </td>
   <td align="center"> G8/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.0.1.17 </td>
     <td align="center"> New Router </td>
   <td align="center"> G9/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.41 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G0/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.37 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G1/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.33 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G2/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.21 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G3/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.29 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G4/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.25 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G5/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.17 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G6/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.6 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G7/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.10 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G8/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.13 </td>
     <td align="center"> Main Router 1 </td>
   <td align="center"> G9/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.42 </td>
     <td align="center"> Quaters SW </td>
   <td align="center"> G0/1 </td>
  </tr>
 <tr>
    <td align ="center"> 10.70.1.1 </td>
     <td align="center"> Quaters SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
 <tr>
    <td align ="center"> 10.70.2.1 </td>
     <td align="center"> Quaters SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
 <tr>
    <td align ="center"> 10.70.3.1 </td>
     <td align="center"> Quaters SW </td>
   <td align="center"> Vlan 13 </td>
  </tr>
 <tr>
    <td align ="center"> 10.70.4.1 </td>
     <td align="center"> Quaters SW </td>
   <td align="center"> Vlan 14 </td>
  </tr>
 <tr>
    <td align ="center"> 10.70.5.1 </td>
     <td align="center"> Quaters SW </td>
   <td align="center"> Vlan 15 </td>
  </tr>
 <tr>
    <td align ="center"> 10.70.6.1 </td>
     <td align="center"> Quaters SW </td>
   <td align="center"> Vlan 16 </td>
  </tr>
 <tr>
    <td align ="center"> 10.70.100.1 </td>
     <td align="center"> Quaters SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
 <tr>
    <td align ="center"> 10.1.1.38 </td>
     <td align="center"> Library Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
 <tr>
    <td align ="center"> 10.24.1.1 </td>
     <td align="center"> Library Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
 <tr>
    <td align ="center"> 10.57.1.1 </td>
     <td align="center"> Library Router </td>
   <td align="center"> Vlan 10 </td>
  </tr>
 <tr>
    <td align ="center"> 10.57.2.1 </td>
     <td align="center"> Library Router </td>
   <td align="center"> Vlan 20 </td>
  </tr>
 <tr>
    <td align ="center"> 10.57.100.1 </td>
     <td align="center"> Library Router </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.1.34 </td>
     <td align="center"> Lab Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.23.1.1 </td>
     <td align="center"> Lab Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.58.1.1 </td>
     <td align="center"> Lab Router </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.58.100.1 </td>
     <td align="center"> Lab Router </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.5 </td>
     <td align="center"> AB1 Router 1 </td>
   <td align="center"> G3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.9 </td>
     <td align="center"> AB1 Router 1 </td>
   <td align="center"> G4/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.21 </td>
     <td align="center"> AB1 Router 1 </td>
   <td align="center"> G5/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.25 </td>
     <td align="center"> AB1 Router 1 </td>
   <td align="center"> G6/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.1.14 </td>
     <td align="center"> AB1 Router 1 </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.13 </td>
     <td align="center"> AB1 Router 1 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.17 </td>
     <td align="center"> AB1 Router 1 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.29 </td>
     <td align="center"> AB1 Router 2 </td>
   <td align="center"> G3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.33 </td>
     <td align="center"> AB1 Router 2 </td>
   <td align="center"> G4/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.45 </td>
     <td align="center"> AB1 Router 2 </td>
   <td align="center"> G5/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.49 </td>
     <td align="center"> AB1 Router 2 </td>
   <td align="center"> G6/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.1.18 </td>
     <td align="center"> AB1 Router 2 </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.37 </td>
     <td align="center"> AB1 Router 2 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.41 </td>
     <td align="center"> AB1 Router 2 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.53 </td>
     <td align="center"> AB2 Router 1 </td>
   <td align="center"> G3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.57 </td>
     <td align="center"> AB2 Router 1 </td>
   <td align="center"> G4/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.69 </td>
     <td align="center"> AB2 Router 1 </td>
   <td align="center"> G5/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.73 </td>
     <td align="center"> AB2 Router 1 </td>
   <td align="center"> G6/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.1.26 </td>
     <td align="center"> AB2 Router 1 </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.61 </td>
     <td align="center"> AB2 Router 1 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.65 </td>
     <td align="center"> AB2 Router 1 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.77 </td>
     <td align="center"> AB2 Router 2 </td>
   <td align="center"> G3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.81 </td>
     <td align="center"> AB2 Router 2 </td>
   <td align="center"> G4/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.93 </td>
     <td align="center"> AB2 Router 2 </td>
   <td align="center"> G5/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.97 </td>
     <td align="center"> AB2 Router 2 </td>
   <td align="center"> G6/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.1.30 </td>
     <td align="center"> AB2 Router 2 </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.85 </td>
     <td align="center"> AB2 Router 2 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.89 </td>
     <td align="center"> AB2 Router 2 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.6 </td>
     <td align="center"> G1 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.101.1.1 </td>
     <td align="center"> G1 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.10 </td>
     <td align="center"> G2 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.101.2.1 </td>
     <td align="center"> G2 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.54 </td>
     <td align="center"> G3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.102.1.1 </td>
     <td align="center"> G3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.58 </td>
     <td align="center"> G4 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.102.2.1 </td>
     <td align="center"> G4 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.26 </td>
     <td align="center"> F1 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.101.51.1 </td>
     <td align="center"> F1 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.22 </td>
     <td align="center"> F2 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.101.52.1 </td>
     <td align="center"> F2 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.74 </td>
     <td align="center"> F3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.102.51.1 </td>
     <td align="center"> F3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.70 </td>
     <td align="center"> F4 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.102.52.1 </td>
     <td align="center"> F4 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.30 </td>
     <td align="center"> S1 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.101.101.1 </td>
     <td align="center"> S1 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.34 </td>
     <td align="center"> S2 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.101.102.1 </td>
     <td align="center"> S2 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.78 </td>
     <td align="center"> S3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.102.101.1 </td>
     <td align="center"> S3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.82 </td>
     <td align="center"> S4 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.102.102.1 </td>
     <td align="center"> S4 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.50 </td>
     <td align="center"> T1 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.101.151.1 </td>
     <td align="center"> T1 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.6 </td>
     <td align="center"> T2 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.101.152.1 </td>
     <td align="center"> T2 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.98 </td>
     <td align="center"> T3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.102.151.1 </td>
     <td align="center"> T3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.94 </td>
     <td align="center"> T3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.102.152.1 </td>
     <td align="center"> T3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.14 </td>
     <td align="center"> FO Router </td>
   <td align="center"> G0/0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.101 </td>
     <td align="center"> FO Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.5.1.1 </td>
     <td align="center"> FO Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.102 </td>
     <td align="center"> Dir Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.3.1.1 </td>
     <td align="center"> Dir Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.105 </td>
     <td align="center"> Tel Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.18 </td>
     <td align="center"> Tel Router </td>
   <td align="center"> G0/2/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.11.1.1 </td>
     <td align="center"> Tel Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.106 </td>
     <td align="center"> SO Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.7.1.1 </td>
     <td align="center"> SO Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.38 </td>
     <td align="center"> Srv1 Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.9.10.1 </td>
     <td align="center"> Srv1 Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.42 </td>
     <td align="center"> Phy Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.109 </td>
     <td align="center"> Phy Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.13.1.1 </td>
     <td align="center"> Phy Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.110 </td>
     <td align="center"> Chem Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.15.1.1 </td>
     <td align="center"> Chem Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.62 </td>
     <td align="center"> EC Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.113 </td>
     <td align="center"> EC Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.6.1.1 </td>
     <td align="center"> EC Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.114 </td>
     <td align="center"> Dean Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.4.1.1 </td>
     <td align="center"> Dean Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.66 </td>
     <td align="center"> Eng Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.117 </td>
     <td align="center"> Eng Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.12.1.1 </td>
     <td align="center"> Eng Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.118 </td>
     <td align="center"> WO Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.8.1.1 </td>
     <td align="center"> WO Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.86 </td>
     <td align="center"> Srv2 Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.10.10.1 </td>
     <td align="center"> Srv2 Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.121 </td>
     <td align="center"> Math Router </td>
   <td align="center"> G0/0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.90 </td>
     <td align="center"> Math Router </td>
   <td align="center"> G0/2/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.14.1.1 </td>
     <td align="center"> Math Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.2.122 </td>
     <td align="center"> Bio Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.16.1.1 </td>
     <td align="center"> Bio Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.57 </td>
     <td align="center"> Main Router 2 </td>
   <td align="center"> G3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.61 </td>
     <td align="center"> Main Router 2 </td>
   <td align="center"> G4/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.53 </td>
     <td align="center"> Main Router 2 </td>
   <td align="center"> G5/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.45 </td>
     <td align="center"> Main Router 2 </td>
   <td align="center"> G6/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.14 </td>
     <td align="center"> Main Router 2 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.1.22 </td>
     <td align="center"> Main Router 2 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.46 </td>
     <td align="center"> Bh1 SW </td>
   <td align="center"> G0/2 </td>
  </tr>
<tr>
    <td align ="center"> 10.60.0.1 </td>
     <td align="center"> Bh1 SW </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.60.1.1 </td>
     <td align="center"> Bh1 SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.60.2.1 </td>
     <td align="center"> Bh1 SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
<tr>
    <td align ="center"> 10.60.3.1 </td>
     <td align="center"> Bh1 SW </td>
   <td align="center"> Vlan 13 </td>
  </tr>
<tr>
    <td align ="center"> 10.60.100.1 </td>
     <td align="center"> Bh1 SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.54 </td>
     <td align="center"> Gh1 SW </td>
   <td align="center"> G0/2 </td>
  </tr>
<tr>
    <td align ="center"> 10.62.0.1 </td>
     <td align="center"> Gh1 SW </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.62.1.1 </td>
     <td align="center"> Gh1 SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.62.2.1 </td>
     <td align="center"> Gh1 SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
<tr>
    <td align ="center"> 10.62.3.1 </td>
     <td align="center"> Gh1 SW </td>
   <td align="center"> Vlan 13 </td>
  </tr>
<tr>
    <td align ="center"> 10.62.100.1 </td>
     <td align="center"> Gh1 SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.58 </td>
     <td align="center"> Gh2 SW </td>
   <td align="center"> G0/2 </td>
  </tr>
<tr>
    <td align ="center"> 10.63.0.1 </td>
     <td align="center"> Gh2 SW </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.63.1.1 </td>
     <td align="center"> Gh2 SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.63.2.1 </td>
     <td align="center"> Gh2 SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
<tr>
    <td align ="center"> 10.63.3.1 </td>
     <td align="center"> Gh2 SW </td>
   <td align="center"> Vlan 13 </td>
  </tr>
<tr>
    <td align ="center"> 10.63.100.1 </td>
     <td align="center"> Gh2 SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.62 </td>
     <td align="center"> Bh2 SW </td>
   <td align="center"> G0/2 </td>
  </tr>
<tr>
    <td align ="center"> 10.61.0.1 </td>
     <td align="center"> Bh2 SW </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.61.1.1 </td>
     <td align="center"> Bh2 SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.61.2.1 </td>
     <td align="center"> Bh2 SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
<tr>
    <td align ="center"> 10.61.3.1 </td>
     <td align="center"> Bh2 SW </td>
   <td align="center"> Vlan 13 </td>
  </tr>
<tr>
    <td align ="center"> 10.61.100.1 </td>
     <td align="center"> Bh2 SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.6 </td>
     <td align="center"> GuestH SW </td>
   <td align="center"> G0/2 </td>
  </tr>
<tr>
    <td align ="center"> 10.71.0.1 </td>
     <td align="center"> GuestH SW </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.71.100.1 </td>
     <td align="center"> GuestH SW </td>
   <td align="center"> Vlan 99 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.22 </td>
     <td align="center"> CSE Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.17.1.1 </td>
     <td align="center"> CSE Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.51.1.1 </td>
     <td align="center"> CSE Router </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.51.100.1 </td>
     <td align="center"> CSE Router </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.26 </td>
     <td align="center"> CIVIL Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.22.1.1 </td>
     <td align="center"> CIVIL Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.56.1.1 </td>
     <td align="center"> CIVIL Router </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.56.100.1 </td>
     <td align="center"> CIVIL Router </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.30 </td>
     <td align="center"> ECE Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.18.1.1 </td>
     <td align="center"> ECE Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.52.1.1 </td>
     <td align="center"> ECE Router </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.52.100.1 </td>
     <td align="center"> ECE Router </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.34 </td>
     <td align="center"> Mech Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.21.1.1 </td>
     <td align="center"> Mech Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.55.1.1 </td>
     <td align="center"> Mech Router </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.55.100.1 </td>
     <td align="center"> Mech Router </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.38 </td>
     <td align="center"> Mme Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.19.1.1 </td>
     <td align="center"> Mme Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.53.1.1 </td>
     <td align="center"> Mme Router </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.53.100.1 </td>
     <td align="center"> Mme Router </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.42 </td>
     <td align="center"> EEE Router </td>
   <td align="center"> G0/1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.20.1.1 </td>
     <td align="center"> EEE Router </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.54.1.1 </td>
     <td align="center"> EEE Router </td>
   <td align="center"> Vlan 10 </td>
  </tr>
<tr>
    <td align ="center"> 10.54.100.1 </td>
     <td align="center"> EEE Router </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.5 </td>
     <td align="center"> Dept Router 1 </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.55 </td>
     <td align="center"> Dept Router 1 </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.21 </td>
     <td align="center"> Dept Router 1 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.9 </td>
     <td align="center"> Dept Router 1 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.34 </td>
     <td align="center"> Dept Router 2 </td>
   <td align="center"> G5/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.29 </td>
     <td align="center"> Dept Router 2 </td>
   <td align="center"> G6/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.10 </td>
     <td align="center"> Dept Router 2 </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.17 </td>
     <td align="center"> Dept Router 2 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.13 </td>
     <td align="center"> Dept Router 2 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.18 </td>
     <td align="center"> Dept Router 3 </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.37 </td>
     <td align="center"> Dept Router 3 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.1.3.41 </td>
     <td align="center"> Dept Router 3 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.5 </td>
     <td align="center"> Old Router  </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.9 </td>
     <td align="center"> Old Router  </td>
   <td align="center"> G1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.0.2.17 </td>
     <td align="center"> Old Router  </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.0.2.5 </td>
     <td align="center"> Old Router  </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.0.2.9 </td>
     <td align="center"> Old Router  </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.33 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G1/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.29 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G2/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.61 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.25 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G4/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.10 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G5/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.21 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G6/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.17 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G7/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.13 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G8/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.6 </td>
     <td align="center"> Main Router 3 </td>
   <td align="center"> G9/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.9 </td>
     <td align="center"> M Router </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.22 </td>
     <td align="center"> M Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.17 </td>
     <td align="center"> P Router </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.14 </td>
     <td align="center"> P Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.25 </td>
     <td align="center"> K Router </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.18 </td>
     <td align="center"> K Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.33 </td>
     <td align="center"> L Router </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.26 </td>
     <td align="center"> L Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.13 </td>
     <td align="center"> M SW </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.21 </td>
     <td align="center"> P SW </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.29 </td>
     <td align="center"> K SW </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.37 </td>
     <td align="center"> L SW </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.1.1 </td>
     <td align="center"> P1 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.20 </td>
     <td align="center"> P1 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.2.1 </td>
     <td align="center"> P2 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.19 </td>
     <td align="center"> P2 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.3.1 </td>
     <td align="center"> P3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.18 </td>
     <td align="center"> P3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.51.1 </td>
     <td align="center"> K1 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.26 </td>
     <td align="center"> K1 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.52.1 </td>
     <td align="center"> K2 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.27 </td>
     <td align="center"> K2 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.53.1 </td>
     <td align="center"> K3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.28 </td>
     <td align="center"> K3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.101.1 </td>
     <td align="center"> M1 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.10 </td>
     <td align="center"> M1 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.102.1 </td>
     <td align="center"> M2 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.11 </td>
     <td align="center"> M2 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.103.1 </td>
     <td align="center"> M3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.12 </td>
     <td align="center"> M3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.151.1 </td>
     <td align="center"> L1 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.34 </td>
     <td align="center"> L1 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.152.1 </td>
     <td align="center"> L2 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.35 </td>
     <td align="center"> L2 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.103.153.1 </td>
     <td align="center"> L3 </td>
   <td align="center"> Vlan 1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.2.36 </td>
     <td align="center"> L3 </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.53 </td>
     <td align="center"> Sac Router </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.62 </td>
     <td align="center"> Sac Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.54 </td>
     <td align="center"> Sac SW </td>
   <td align="center"> G0/2 </td>
  </tr>
<tr>
    <td align ="center"> 10.75.1.1 </td>
     <td align="center"> Sac SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.75.100.1 </td>
     <td align="center"> Sac SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.45 </td>
     <td align="center"> GH Router </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.49 </td>
     <td align="center"> GH Router </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.30 </td>
     <td align="center"> GH Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.46 </td>
     <td align="center"> GHR SW </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.74.1.1 </td>
     <td align="center"> GHR SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.74.2.1 </td>
     <td align="center"> GHR SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
<tr>
    <td align ="center"> 10.74.100.1 </td>
     <td align="center"> GHR SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.50 </td>
     <td align="center"> GHO SW </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.73.1.1 </td>
     <td align="center"> GHO SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.73.2.1 </td>
     <td align="center"> GHO SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
<tr>
    <td align ="center"> 10.73.100.1 </td>
     <td align="center"> GHO SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.57 </td>
     <td align="center"> Bh Router </td>
   <td align="center"> G0/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.41 </td>
     <td align="center"> Bh Router </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.34 </td>
     <td align="center"> Bh Router </td>
   <td align="center"> G0/3/0 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.58 </td>
     <td align="center"> BhR SW </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.76.1.1 </td>
     <td align="center"> BhR SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.76.2.1 </td>
     <td align="center"> BhR SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
<tr>
    <td align ="center"> 10.76.100.1 </td>
     <td align="center"> BhR SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>
<tr>
    <td align ="center"> 10.2.1.42 </td>
     <td align="center"> BhO SW </td>
   <td align="center"> G0/1 </td>
  </tr>
<tr>
    <td align ="center"> 10.77.1.1 </td>
     <td align="center"> BhO SW </td>
   <td align="center"> Vlan 11 </td>
  </tr>
<tr>
    <td align ="center"> 10.77.2.1 </td>
     <td align="center"> BhO SW </td>
   <td align="center"> Vlan 12 </td>
  </tr>
<tr>
    <td align ="center"> 10.77.100.1 </td>
     <td align="center"> BhO SW </td>
   <td align="center"> Vlan 100 </td>
  </tr>

 <tr>
    <td>----------------------------------------</td>
    <td>----------------------------------------</td>
    <td>----------------------------------------</td>
  </tr>
</thead>
</table>
    </p>
  </samp>
</div>
</details>
<details>
  <summary>5. Monitor and Maintain LAN</summary>
<div>
  <samp>
    <p>
     <br>
     Follow network standards and protocols, that are rules and conventions that govern how network devices communicate and interact with each other. Once we have designed and implemented our LAN, we need to monitor and maintain it regularly to ensure its optimal performance, security, and reliability.
    </p>
  </samp>
</div>
</details>

## The Features included .........
<li> Used 10.0.0.0/8 subnet of private address as per RFC1918.</li>
<li> Used Network Address Translation(NAT) for the internet usage in LAN.</li>
<li> Used subnet mask of 255.255.255.0(/24) for endhosts, 255.255.255.252(/30) for point to point connections and 255.255.255.248(/29) for point to multipoint connections.</li>
<li> Each Network Device is Configured with appropriate Hostname and Domain name of RGUKT.</li>
<li> In this LAN, It has DNS Server 10.10.10.10 to resolve the local domain names and use Google DNS(8.8.8.8) for recursive DNS search.</li>
<li> In this LAN, It has WebServer 10.9.10.9(rgukt.com) with the official Collage Website(quite functional).</li>
<li> In this LAN, It has Syslog Server, where all the log msgs from Network Devices will be stored at one place.</li>
<li> In this LAN, It has Email Server with the @rguktrkv.ac.in domain and preconfigured with more than 70 different email address and passwords configured in most of all devices in LAN.</li>
<li> In Switchs for security we have enabled Port-Security, Arp Inspection, DHCP snooping and Portfast for Immediate transition to Forwarding state.</li>
<li> In Switchs all the unused ports are shutdown and moved to Unused VLAN.</li>
<li> In Multilayer Switches enabled routing and Configured appropriate Routed Ports.</li>
<li> Used Open Shortest Path First(OSPF) for Routing protocol with default Route.</li>
<li> Each Department in LAN has its own Ip Phone(fully functional we can call any IP phone in LAN)(Telephone-service & Dial-peerings).</li>
<li> Each Device has login Credentials(either console or vty) that is Username is "admin" password is "deepak".</li>
<li> and the enable password with md5 encryption (default) is "passwd".</li>
<li> Each Device can be remotely login by using only SSH But the access is limited to only Server Room devices(either SRV1 or SRV2) by applying AccessLists.</li>
<li> Each wired and wirelss endhost may get its appropriate address from their DHCP server(configured in nearby routers).</li>
<li> For Wireless Users configured a LightWeight Aps model with Wlc (username:-"admin" password:-"Wifi@123") in FlexConnect mode.</li>
<li> We can connect To any wireless AP by providing SSID and Password(rgukt123) (WPA2+PSK).</li>
<li> Used VLANs in MultiLayer Switchs to providing multiple SSIDs from same Switch and interfaces are Configured as trunk.</li>

Thank you for checking out my project! If you encounter any errors, bugs, or have any ideas on how to make this project better, I'd love to hear from you. Your feedback is incredibly valuable and helps improve the overall quality of the project.

Please feel free to open an issue here on GitHub or reach out to me directly via Contact Details given below with any suggestions, questions, or concerns you may have.

Let's work together to make this project even more awesome!

<b>Your Friend <br>
Karumuri Lakshmi Deepak</b>

## <b> Let's Connect..!</b><img src="https://github.com/LakshmiDeepak9653/RKV-lan-resources/blob/main/handshake.gif" width ="80">
<br>
<div>

[![WhatsApp](https://img.icons8.com/bubbles/100/000000/whatsapp.png)](https://wa.me/+919491184607)
[![LinkedIn](https://img.icons8.com/bubbles/100/000000/linkedin.png)](https://www.linkedin.com/in/lakshmi-deeapk-karumuri-402460207)
[![GitHub](https://img.icons8.com/bubbles/100/000000/github.png)](https://github.com/LakshmiDeepak9653)
[![Instagram](https://img.icons8.com/bubbles/100/000000/instagram-new.png)](https://www.instagram.com/deepakvevo/)
[![FaceBook](https://img.icons8.com/bubbles/100/000000/facebook.png)](https://www.facebook.com/deepak.karumuri.3)

</div>
