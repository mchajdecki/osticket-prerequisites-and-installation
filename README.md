
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
<li><a href="#install">Installing features and the contents of the osTicket folder</a></li>
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
      <li>The provided link should download the folder directly - if the Google Drive message pops up then select - Download anyway button to continue.</li>
    <li>The direct download will appear in the downloads to the right on the browser.</li>
    <li>Click on the folder icon to go to the dedicated folder that the osTicket-Installation-Files downloaded into.</li>
  </ol>
  </p>
<p>
   <img src="https://github.com/mchajdecki/osticket-prerequisites/blob/3010c43b0e8bb402783a91227036371df13b79ef/images/Slide-9.jpg" alt="DownloadosTicket-Slide-9">
<br>
<hr>


<p>
 <ol type="1">
 <li>Extract the zip file to the desktop.</li>
 <li>Extracted folder osTicket-Installation-File will appear on the desktop.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites/blob/8a74f090f04feabd7c7b593f90144c13299c28d4/images/Slide_10.jpg" alt="DownloadosTicket-Slide_10">
</p>
 <br>
 <hr>


<h1 id="install"><i>Install / Enable IIS in Windows WITH CGI</i></h1>
 <p>
 <ol type="1">
 <li>Search for an open the Control Panel.</li>
 <li>Click on Programs to continue.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/a96d8f6f7fe0a74b373688a3978a534701b32ade/images/Slide_11.jpg" alt="DownloadosTicket-Slide_11">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
 <li>Click on - Turn Windows features on or off.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/96e10f37c05d6e40a22deb00e7641a022f6e4c04/images/Slide_12.jpg" alt="DownloadosTicket-Slide_12">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
   <li>A Windows Features window will appear</li>
 <li>In the Windows features we will Install / Enable IIS in Windows with CGI.</li>
 <li>Check the box and click the plus sign next to Internet Information Services to expand more options.</li>
 <li>Click the plus sign next to World Wide Web Services to expand more options.</li>
 <li>Click the plus sign next to the Application Development Features to expand more options.</li>
<li>Check the CGI box to enable it.</li>
  <li>Click Ok to continue and turn on the features.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/4e55e3027bf0b26f8990aae5d35647a05ba29cc3/images/Slide_13.jpg" alt="DownloadosTicket-Slide_13">
</p>
 <br>
 <hr>


<h1><i>Install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)</i></h1>
<p>
 <ol type="1">
 <li>From the osTicket-Installation-Files folder - double click the PHPManagerForIIS_V1.5.0 file to begin install.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/a39725ccba5a323db4b85baa8cb3c8bdf1281ce8/images/Slide_14.jpg" alt="DownloadosTicket-Slide_14">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
  <li>Click Next to continue the installation.</li>
  <li>Select I Agree - Click next to continue the installation.</li>
  <li>Click close once installation is complete.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/2fa83a0a3e9920057fac40b515d2971ebd3236aa/images/Slide_15.jpg" alt="DownloadosTicket-Slide_15">
</p>
 <br>
 <hr>

 <h1><i>Install the Rewrite Module (rewrite_amd64_en-US.msi)</i></h1>
 <p>
 <ol type="1">
 <li>From the osTicket-Installation-FIles folder - double click the rewrite_amd64_en-US.msi file to begin install.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/11bda06041c9878724a5e6a94104724fef0fb240/images/Slide_16.jpg" alt="DownloadosTicket-Slide_16">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>Check the License Agreement box and click Install to continue.</li>
 <li>Click the Finish button to complete the installation.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/80ff03eed491597b1d71174d562e21e2c7e19116/images/Slide_17.jpg" alt="DownloadosTicket-Slide_17">
</p>
 <br>
 <hr>

 <h1><i>Create the directory C:\PHP</i></h1>
 <p>
 <ol type="1">
 <li>Right click the folder in the toolbar.</li>
 <li>Navigate to File Explorer.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/082953415888f2d43735f652de9bef486ba92b01/images/Slide_18.jpg" alt="DownloadosTicket-Slide_18">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
 <li>Navigate to the Windows (C:) drive.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/3b2527699a34eccca10dad745da2271bbd09e5ee/images/Slide_19.jpg" alt="DownloadosTicket-Slide_19">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
 <li>Create a new folder in the Windows (C:) drive.</li>
   <li>Right click inside the folder - select new - click on folder to create.</li>
   <li>Name it PHP</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/934acc231d6682e78fda12853cae39edcb8c0210/images/Slide_20.jpg" alt="DownloadosTicket-Slide_20">
</p>
 <br>
 <hr>

 <h1><i>Unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder</i></h1>
 <p>
 <ol type="1">
 <li>From the osTicket-Installation-FIles right click the php-7.3.8-nts-Win32-VC15-x86.zip and select Extract All.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/b6f2ab3cdabb0e450a2836d729d010c89ba1b64c/images/Slide_21.jpg" alt="DownloadosTicket-Slide_21">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
 <li>In the select a destination and extract files - browse to find the PHP folder we created.</li>
 <li>Select the PHP folder from This PC - Windows (C:) to continue.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/f8bfa2a737c5d38dcb821ea34f8d9c586d1bf152/images/Slide_22.jpg" alt="DownloadosTicket-Slide_22">
</p>
 <br>
 <hr>

<p>
 <ol type="1">
 <li>After the PHP folder is selected as the destination for the files to be extracted to.</li>
 <li>Click extract to finish.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/93aac352ced023a2a8963ff0efed4000e79b2740/images/Slide_23.jpg" alt="DownloadosTicket-Slide_23">
</p>
 <br>
 <hr>

 <h1><i>Install the VC_redist.x86.exe.</i></h1>
<p>
 <ol type="1">
 <li>From the osTicket-Installation-Files folder - double click the VC_redist.x86.exe. file to begin install.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/fff7394d4847ac8c4df5d1fb16d7ce7018c3b713/images/Slide_24.jpg" alt="DownloadosTicket-Slide_24">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
 <li>Check the box to agree to license and conditions and click on Install.</li>
   <li>Click on close when installation is done.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/8e07e428abe39f594e33c1d03592124546ba9640/images/Slide_25.jpg" alt="DownloadosTicket-Slide_25">
</p>
 <br>
 <hr>

 <h1><i>Install the MySQL 5.5.62 (mysql-5.5.62-win32.msi).</i></h1>
<p>
 <ol type="1">
 <li>From the osTicket-Installation-Files folder - double click the mysql-5.5.62-win32.msi.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/b61706646238a82f69f025825819de67e9bdc6c1/images/Slide_26.jpg" alt="DownloadosTicket-Slide_26">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>Go throught the install by selecting the highlighted options.</li>
 <li>At the end of the installation check the (Launch the MySQL Instance Configuration Wizard) box for the configuration options to open.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/0d6ff956cfcc8d1a5322385c1d98ca50d15a281f/images/Slide_27.jpg" alt="DownloadosTicket-Slide_27">
</p>
 <br>
 <hr>


 <h1><i>Configuring the MySQL Server 5.5 server instance.</i></i></h1>
<p>
 <ol type="1">
 <li>Go throught the configuration by following the highlighted options.</li>
 <li>In the security options type in root and confirm for the password.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/cab060985702ecd268c38e4b12d93c9d4affc96f/images/Slide_28.jpg" alt="DownloadosTicket-Slide_28">
</p>
 <br>
 <hr>

 
 <h1><i>Configuration in the Internet Information Services (IIS).</i></i></h1>
<p>
 <ol type="1">
 <li>Search for IIS (Internet Information Services) Manager and run it as administrator.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/f5d82f457a78eda40d961380d45f36c0fdc79be9/images/Slide_29.jpg" alt="DownloadosTicket-Slide_29">
</p>
 <br>
 <hr>

   <p>
 <ol type="1">
 <li>Go to osTicket.</li>
 <li>Double click on PHP manager.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/10bfafe0acdf198349995b6be6f34a8523eb02fd/images/Slide_30.jpg" alt="DownloadosTicket-Slide_30">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>Click on Register new PHP version.</li>
 <li>A window to provide a path to the php executable file will pop up.</li>
 <li>Click on the 3 dots to provide path.</li>
   <li>Go to Windows(C:) and navigate to the PHP folde and open it.</li>
   <li>Select the php-cgi and open it.</li>
   <li>Click Ok to finalize the path selection.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/988b446cd023e82197f012a80fb0838f5829e4ce/images/Slide_31.jpg" alt="DownloadosTicket-Slide_31">
</p>
 <br>
 <hr>

 
  <p>
 <ol type="1">
 <li>In the Internet Information Services (IIS) Manager go to the osTicket.</li>
<li>In the Actions menu select STOP to stop the server.</li>
   <li>Then click to START the server back up in the actions menu.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/ff8fb8e3250c4460b7276b7717794467922926d3/images/Slide_32.jpg" alt="DownloadosTicket-Slide_32">
</p>
 <br>
 <hr>

  <h1><i>Install osTicket v1.15.8.</i></i></h1>
<p>
 <ol type="1">
 <li>From the osTicket-Installation-Files right click the osTicket-v1.15.8 and select Extract All into the destination provided.</li>
   <li>Click Extract to continue.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/bcbe1c5d7374e779d06282ec1356ea166a23c0e1/images/Slide_33.jpg" alt="DownloadosTicket-Slide_33">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>The newly extracted folder is in the osTicket-Installation Files Folder.</li>
   <li>Double click to open the new folder and keep it open for the next part.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/fc092dda11f2e0a1cc86342a5ac03117ed3938d2/images/Slide_34.jpg" alt="DownloadosTicket-Slide_34">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>Keep the osTicket-v1.15.8 folder open.</li>
   <li>Right click the folder in the toolbar and then click on File Explorer to continue.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/afb01e8148a88c56a8b82b6c5c6fb4e567bb2dfe/images/Slide_35.jpg" alt="DownloadosTicket-Slide_35">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>Go to This PC --> Windows(C:) --> inetpud.</li>
 <li>In the inetpud folder go to wwwroot folder.</li>
   <li>Copy and paste the upload folder to the wwwroot folder.</li>
   <li>right click on the pasted folder and click on Rename.</li>
   <li>Rename the folder to osTicket</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/82fc27c2cfb56f9892e63d25822ff6a7554b68d4/images/Slide_36.jpg" alt="DownloadosTicket-Slide_36">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>Navigate back to ISS (Internet Information Services).</li>
 <li>In the actions menu under Manage Server - Stop and Start the server or restart it to continue.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/82b4012e94b86a5447cf7c1c359cb9bac9a2c984/images/Slide_37.jpg" alt="DownloadosTicket-Slide_37">
</p>
 <br>
 <hr>

 
  <h1><i>Launch osTicket browser.</i></i></h1>
<p>
 <ol type="1">
 <li>Navigate to (IIS) Internet Information Services Manager.</li>
   <li>Go to Sites --> Default Web Site --> osTicket.</li>
   <li>Then click on Browse *:80 (http).</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/c976abc7767e9ffac83722d3fc10751cd2d65396/images/Slide_38.jpg" alt="DownloadosTicket-Slide_38">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>After clicking on Browse *:80 (http) the osTicket browser window will show.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/7467b64ffc663bf55dfdb286d8a7c060640b62c9/images/Slide_39.jpg" alt="DownloadosTicket-Slide_39">
</p>
 <br>
 <hr>

   <h1><i>Enabling extensions.</i></i></h1>
<p>
 <ol type="1">
   <li>Open (IIS) Information Services Manager and double click on PHP Manager to open it.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/acdec98625637045ea61808d2c11e4fa38646e2e/images/Slide_40.jpg" alt="DownloadosTicket-Slide_40">
</p>
 <br>
 <hr>

   <p>
 <ol type="1">
 <li>Click on Enable or disable an extension.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/2918617c33ca57de367b3312a6108da35638259b/images/Slide_41.jpg" alt="DownloadosTicket-Slide_41">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>To enable extensions the button "enable" will show in the Actions menu when they are disabled.</li>
   <li>Select the (php_imap.dll) - (php_intl.dll) - (php_opcache.dll) and enable to continue.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/901ab06a80dfd9d27445c624dc67468076cea26d/images/Slide_42.jpg" alt="DownloadosTicket-Slide_42">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
 <li>Refresh the osTicket browser.</li>
   <li>The osTicket browser before refreshing still shows the extensions as disabled.</li>
   <li>The osTicket browser after refreshing shows the extensions now enabled.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/41856277de0088d91cf42d9c8517156b3db4b75b/images/Slide_43.jpg" alt="DownloadosTicket-Slide_43">
</p>
 <br>
 <hr>

   <h1><i>Allowing Permissions.</i></i></h1>
<p>
 <ol type="1">
   <li>Right click the folder in the toolbar and go to File Explorer.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/b09cd27adbea22d620663df6c46e2252ab697ac2/images/Slide_44.jpg" alt="DownloadosTicket-Slide_44">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>Navigate to the file ost-sampleconfig.php</li>
   <li>Go to --> This PC --> Windows (C:) --> inetpud --> wwwroot --> osTicket --> include.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/654fa406b1141cd52b9f138f193371fd6c2d3913/images/Slide_45.jpg" alt="DownloadosTicket-Slide_45">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
 <li>Rename the file ost-sampleconfig.php to os-config.php</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/c2f72628f16b6808170a8d6cbbe651112c073027/images/Slide_46.jpg" alt="DownloadosTicket-Slide_46">
</p>
 <br>
 <hr>

<p>
 <ol type="1">
 <li>Right click on the ost-config.php file and click on Properties to continue.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/da47f81a45ea9c00a148a3107520b1d22fd472a4/images/Slide_47.jpg" alt="DownloadosTicket-Slide_47">
</p>
 <br>
 <hr>

 <p>
 <ol type="1">
 <li>In the Properties menu first click on Security then click on Advanced for more options.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/10eb3afc0e35f08da2884913bc007e0ae440535d/images/Slide_48.jpg" alt="DownloadosTicket-Slide_48">
</p>
 <br>
 <hr>

  <p>
 <ol type="1">
 <li>In the advanced menu click on Disable Inheritance and then click Remove all inherited permissions from this object.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/6f1327d02e6bfa3114ce23e909e994d8879f7a72/images/Slide_49.jpg" alt="DownloadosTicket-Slide_49">
</p>
 <br>
 <hr>

   <p>
 <ol type="1">
 <li>Click on Add - to add new permissions.</li>
 </ol>
 </p>
<p>
  <img src="https://github.com/mchajdecki/osticket-prerequisites-and-installation/blob/a8a4e7d5fd7810c691444191259d0e0232b68deb/images/Slide_50.jpg" alt="DownloadosTicket-Slide_50">
</p>
 <br>
 <hr>



