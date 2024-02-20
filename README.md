# Welcome to Campus Area Network System Design!

![hello](https://github.com/LakshmiDeepak9653/resoures1/blob/main/wave.gif) Welcome to Campus Area Network System Project!
 We're thrilled to have you here.

this is a replication of a Campus LAN network of my collage <strong>RGUKT RK Valley</strong>. Did to test my CCNA Knowledge

Before getting into the details of this project. Lets talk about some common LAN design principles and best practices i followed.
<details>
  <summary>1. Identifying the Needs and Goals</summary>
<div>
  <samp>
   <br>
    <p>
     Before staring the design of our LAN. we need to ask ourself some questions about our Project and find the Answers to them.
     Here are the Questions and my Answers to them as per this Project.
     <b><ul>I. What are the Main functions and applications of our LAN?</ul></b>
       The main idea of my project is Replicate my campus LAN design with appropriate Features Like. Main Web server, Email server and DNS server and NTP server and Many more Features included in that design.<br>
     <b><ul>II. How  many Users and devices will access your the Network?</ul></b>
       There are more than 6000 students and 300+ faculty and many more users are there. Network must be available to users as Wired or Wireless.<br>
     <b><ul>III. What are the expected traffic patterns and bandwidth requirements?</ul></b>
       In our project we have two traffic patterns thats is faculty traffic and students traffic. The students must not access the faculty devices. The bandwidth requirements will the intra area communications (between the routers) must be fast.<br>
     <b><ul>IV. How will we ensure security and privacy of your data?</ul></b>
       All the outside intiating connections must be stopped and incoming traffic must be checked.<br>
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
     <strong><ol>Main Campus</ol></strong>
     <ul>1. Faculty Quaters (6 Quaters)</ul>
     <ul>2. Library (2 Floors)</ul> 
     <ul>3. Lab Complex</ul>
     <ul>4. Academic Block - 1 (4 Floors)</ul> 
     <ul>5. Academic Block - 2 (4 Floors)</ul>
     <ul>6. Boys Hostel - 1 (4 Floors)</ul>
     <ul>7. Girls Hostel - 1 (4 Floors)</ul>
     <ul>8. Girls Hostel - 2 (4 Floors)</ul>
     <ul>9. Boys Hostel - 2 (4 Floors)</ul>
     <ul>10. Guest House</ul>
     <ul>11. C.S.E Department</ul>
     <ul>12. E.C.E Department</ul>
     <ul>13. M.M.E Department</ul>
     <ul>14. CIVIL Department</ul>
     <ul>15. MECH Department</ul>
     <ul>16. E.E.E Department</ul>
     <br>
     <strong><ol>Old Campus</ol></strong>
     <ul>1. PI Class Rooms</ul>
     <ul>2. MU Class Rooms</ul> 
     <ul>3. KAPPA Class Rooms</ul>
     <ul>4. LAMBDA Class Rooms</ul> 
     <ul>5. Girls Hostels RKV (Alpha/Beta)</ul>
     <ul>6. Girls Hostels ONG (Gamma/Delta)</ul>
     <ul>7. Boys Hostels RKV (Rho)</ul>
     <ul>8. Boys Hostels ONG (Teta)</ul>
     <ul>9. S.A.C Building</ul> 
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
     <img src="https://github.com/LakshmiDeepak9653/RKV-lan-resources/blob/main/RKV%20COMPLETE%20TOPOLOGY.png"></img>
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
     Network segmentation and addressing are techniques that can help us organize and manage our LAN more effectively. Network segmentation is the process of dividing our LAN into smaller subnetworks, or subnets, based on logical criteria, such as function, location, or department. As per <b>RFC 1918</b> i use 10.0.0.0/8 subnet because i need to connect alot of devices this will provide me that Host address space and i will be using the Subnet Mask of 255.255.255.0  Which means i will be using 2^16 subnets and host space will 2^8. That would be lot more enough.<br>
    <br>Here comes the Address Scheme of This Network.
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

```The main idea of my project is Replicate my campus LAN design with appropriate Features Like. Main Web server, Email server and DNS server and NTP server and Many more Features included in that design.```



## <b> Let's Connect..!</b><img src="https://github.com/LakshmiDeepak9653/RKV-lan-resources/blob/main/handshake.gif" width ="80">
<br>
<div>

[![WhatsApp](https://img.icons8.com/bubbles/100/000000/whatsapp.png)](https://wa.me/+919491184607)
[![LinkedIn](https://img.icons8.com/bubbles/100/000000/linkedin.png)](https://www.linkedin.com/in/lakshmi-deeapk-karumuri-402460207)
[![GitHub](https://img.icons8.com/bubbles/100/000000/github.png)](https://github.com/LakshmiDeepak9653)
[![Instagram](https://img.icons8.com/bubbles/100/000000/instagram-new.png)](https://www.instagram.com/deepakvevo/)
[![FaceBook](https://img.icons8.com/bubbles/100/000000/facebook.png)](https://www.facebook.com/deepak.karumuri.3)

</div>
