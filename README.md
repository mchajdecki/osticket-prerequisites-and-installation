
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h1>In This tutorial we will be creating the following resources in Microsoft Azure and proceed to Install OS Ticket Inside the Virtual Machine.</h1>

- Resource Group
- Windows Virtual Machine

<h3>For an in depth rundown on Microsoft Azure visit this <a href="https://github.com/mchajdecki/Microsoft-Azure">Microsoft Azure Full Tutorial</a>


<br>

<h2>This tutorial outlines the following</h2>
<ul>

<li><a href="#rg">Creating Resource Group</a></li>
<li><a href="#vm">Creating a Virtual Machine</a></li>
<li><a href="#login">Logging Into Virtual Machine</a></li>
<li><a href="#download">Download The osTicket Installation Files</a></li>
</ul>

<br/>


<h1 id="rg"><i>Creating a Resource Group</i></h1>
<h2>A Resource Group is a folder in the cloud that holds virtual machines, virtual networks, storage accounts and other created services.</h2>

<p>
  <ol type="1">
     <li>Navigate to Microsoft Azure main portal.</li>
    <li>Find the Resource Group option on the home page of the portal or type it in the search box.</li>
    <li>Click on the Resource Group option to continue.</li>
  </ol>
</p>
<p>
<img src="https://github.com/mchajdecki/osticket-prereqs/blob/65f7f852322784b0ae7525176b7943ac0527d8a7/images/Slide-1.jpg" alt="Creating a Resource Group - Slide_1"/>
</p>
<br>
<hr>



<p>
  <ol type="1">
    <li>Select the Subscription you are currently using.</li>
    <li>Name the Resource Group.(e.g. OSTicketRG)</li>
    <li>Select the appropriate time zone you are located in.</li>
    <li>Click Review + Create on the bottom of the page to continue.</li>
  </ol>
</p>
<p>
<img src="https://github.com/mchajdecki/osticket-prerequisites/blob/0294d5c3b8ae4ed80b46a1f3ab6059085343d855/images/Slide-2.jpg" alt="Creating a Resource Group - Slide_2"/>
</p>
<br>
<hr>


<p>
  <ol type="1">
    <li>Click create again to continue.</li>
  </ol>
</p>
<p>
<img src="https://github.com/mchajdecki/osticket-prereqs/blob/50dbb2c9858e856a10fc07f769323e13172379e0/images/Slide-3.jpg" alt="Creating a Resource Group - Slide_3"/>
</p>
<br>
<hr>


<p>
  <ol type="1">
    <li>A prompt message will display that the resource group has been successfully created.</li>
    <li>The newly created Resource Group will show up on the Microsoft Azure main portal.</li>
    <li>The Resource Group has been created.</li>  
  </ol>
</p>
<p>
<img src="https://github.com/mchajdecki/osticket-prereqs/blob/2bfa522500f3cfdb9765646739d904cfb447e5a1/images/Slide-4.jpg" alt="Creating a Resource Group - Slide_4"/>
</p>
<hr>
<br>
<br>
<br>



<h1 id="vm"><i>Creating a Virtual Machine</i></h1>
<p>
  <ol type="1">
    <li>Go to the home page on the Azure platform and locate Virtual Machines.</li>
    <li>Click on Virutal Machine option to get started.</li>
  </ol>
</p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prereqs/blob/1789638b8d0b4ac2dd40e20f6382cbfd35579a8a/images/Slide-5.jpg"  alt="CreatingaVirtualMachine _ Slide_5">
</p>
<br>
<hr>

<p>
  <ol type="1">
    <li>Click create in either place on the Virtual Machines page.</li>
    <li>Select and click on Virtual Machine from the drop down menu.</li>
      </ol>
</p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites/blob/d1200a3e84e59fb0c4bd6790d83a4a2ba06fd2ba/images/Slide-6.jpg" alt="CreatingaVirtualMachine - Slide_6">
</p>
<br>
<hr>


<p>
  <ol type="1">
    <li>Select the subscription you are using.</li>
    <li>Select the Resource Group previously created to store the VM into.</li>
    <li>Name the Virtual Machine.</li>
    <li>Select the appropriate region you are using the VM from.</li>
    <li>Here is where you will select the type of VM you want to use - etc. Windows Fro - Linux. For testing purposes select Windows 10 Pro version 22H2 - x64 Gen.</li>
    <li>Create a username and password *Remeber these credentials as you will be using them to log into the actual Virtual Machine once
created.</li>
    <li>Keep certain options at their default setting.</li>
     <li>Make sure the box for Licensing is checked before proceeding.</li>
     <li>Click Review + Create.</li>
  </ol>
</p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites/blob/a835e487a795527426e9dc4f7b6999fbea03980c/images/Slide-7.jpg" alt="CreatingaVirtualMachine - Slide_7">
</p>
<br>
<hr>



<p> 
  <ol type="1">
    <li>A message will display that the Validation has passed.</li>
    <li>Click create on the bottom of the page to continue in creating the Virtual Machine.</li>
    <li>The Virtual Machine has been successfully created.</li>
  </ol>
</p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites/blob/a835e487a795527426e9dc4f7b6999fbea03980c/images/Slide-8.jpg" alt="CreatingaVirtualMachine - Slide_8">
</p>
<br>
<hr>
  

<h1 id="login"><i>Logging Into a Virtual Machine</i></h1>

<p>
  <ol type="1">
    <li>Prior to logging into the Virtual Machine gather the log in credentials created and the public IP address associated with Virtual Machine. </li>
    <li>This information can be found in the created VM - head over to Virtual Machine and click on Connect.</li>
    <li>Copy the Public IP Address as you will need it for the Log In.</li>
  </ol>
</p>
<p>
  <img src="https://github.com/mchajdecki/Microsoft-Azure/blob/95a413af6ef9b1e1154c1f15583ceb2f53785d92/images/Slide_27.jpg" alt="LoggingIntoAVirtualMachine - Slide_27">
</p>
<br>
<hr>


<h3>The Virtual Machine that is accessed in this tutorial is from a Mac Computer to a Windows Virtual Machine</h3>


<p>
  <ol type="1">
    <li>In the App Store on a Mac device search for the Windows App software.</li>
    <li>Proceed to download the software at it is necessary in order to log into the created Virtual Machine.</li>
    <li>Open the Windows App software.</li>
  </ol>
</p>
<p>
<img src="https://github.com/mchajdecki/Microsoft-Azure/blob/95a413af6ef9b1e1154c1f15583ceb2f53785d92/images/Slide_28.jpg" alt="LoggingIntoAVirtualMachine - Slide_28">
</p>
<br>
<hr>


<p>
  <ol type="1">
    <li>Click on the + sign in the right hand corner of the Windows App and observe a drop dowm menu appear.</li>
    <li>From the drop down menu click on Add PC to continue the log in process.</li>
  </ol>
</p>
<p>
  <img src="https://github.com/mchajdecki/Microsoft-Azure/blob/95a413af6ef9b1e1154c1f15583ceb2f53785d92/images/Slide_29.jpg" alt="LoggingIntoAVirtualMachine - Slide_29">
</p>
<br>
<hr>


<p>
  <ol type="1">
    <li>Add PC box will display.</li>
    <li>Copy and Paste The Public IP address that was created in the Virtual Machine.</li>
    <li>The add option will be available to click after typing in the IP address.</li>
    <li>Click add option to continue.</li>
  </ol>
</p>
<p>
  <img src="https://github.com/mchajdecki/Microsoft-Azure/blob/a9a63e5d632c2c84c56179cfeae2338a93bbe86b/images/Slide_30.jpg" alt="LoggingIntoAVirtualMachine - Slide_30">
</p>
<br>
<hr>


<p>
  <ol type="1">
    <li>After copying and pasting the Public IP the PC Box will display.</li>
    <li>Double click the saved PC box to continue.</li>
  </ol>
  </p>
<p>
  <img src="https://github.com/mchajdecki/Microsoft-Azure/blob/d134a7038cc557ec3e7700c8a626de602995620b/images/Slide_31.jpg" alt="LoggingIntoAVirtualMachine - Slide_31">
</p>
  <br>
  <hr>



  <p>
  <ol type="1">
    <li>Once the PC box is double clicked a pop up window will display.</li>
    <li>Here enter your usernam and password that was set up during the creation of the Virtual Machine.</li>
    <li>Enter the credentials and click continue.</li>
  </ol>
  </p>
<p>
  <img src="https://github.com/mchajdecki/Microsoft-Azure/blob/840983e9f13b0689b63328c7804e995fd2bd1276/images/Slide_32.jpg" alt="LoggingIntoAVirtualMachine - Slide_32">
</p>

  <br>
  <hr>




<p>
  <ol type="1">
    <li>A Welcome screen to the Windows Virtual Machine will display if all the steps were followed correctly.</li>
    <li>This is a Welcome display screen for a Windows VM that is used for this tutorial.</li>
  </ol>
  </p>
<p>
  <img src="https://github.com/mchajdecki/Microsoft-Azure/blob/75b52de34c4448a156a15b9b63ce50f0ea95360f/images/Slide_33.jpg" alt="LoggingIntoAVirtualMachine - Slide_33">
</p>
  <br>
  <hr>


<p>
 <ol type="1">
 <li>A privacy settings screen will display next.</li>
 <li>Check all the prompts to No.</li>
 <li>Click Accept to continue.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/Microsoft-Azure/blob/b6787d44059598c2eade4fd3e1eacc516a37adfa/images/Slide_34.jpg" alt="LoggingIntoAVirtualMachine - Slide_34">
</p>
 <br>
 <hr>


<p>
 <ol type="1">
 <li>A Windows Virtual Machine home page displays.</li>
   <li>That is how you log into a Windows Virtual Machine from a Mac computer.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/Microsoft-Azure/blob/0944ae8630442293e1598a0ee2d0ae9d4d6edf73/images/Slide_35.jpg" alt="LoggingIntoAVirtualMachine - Slide_35">
</p>
 <br>
 <br>
 <br>
 <hr>

 <h1 id="download"><i>Download The osTicket Installation Files</i></h1>
<h3>The next portion of the installation will all take place inside the virtual machine.</h3>
<p>
  <ol type="1">
    <li>In the virtual machine click the following link to download the osticket installation files <a href="https://github.com/mchajdecki/osticket-prerequisites/releases/latest/download/osTicket-Installation-Files.zip" class="btn">
   osTicket-Installation-Files-Download Here </a>
      <li>The provided link should download the folder directly - if the Google Drive message pops up select - Download anyway button to continue.</li>
    <li>The direct download will appear in the downloads to the right on the browser.</li>
    <li>Click on the folder icon to go to the dedicated folder that the osTicket-Installation-Files downloaded into.</li>
<p>
   <img src="https://github.com/mchajdecki/osticket-prerequisites/blob/3010c43b0e8bb402783a91227036371df13b79ef/images/Slide-9.jpg" alt="DownloadosTicket-Slide-9">
<br>
<hr>


<p>
 <ol type="1">
 <li>Extract the zip file to the desktop..</li>
 <li>Extracted folder osTicket-Installation-Fill will appear on the desktop</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites/blob/8a74f090f04feabd7c7b593f90144c13299c28d4/images/Slide_10.jpg" alt="DownloadosTicket-Slide_10">
</p>
 <br>
 <hr>
