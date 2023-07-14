<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

Part 1 (Create Virtual Machine in Azure)

-Create a Resource Group

-Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs
  aWhen creating the VM, allow it to create a new Virtual Network (Vnet)

Name: Vm-osticket

Username: labuser (for example/whatever you chose)

Password: osTicketPassword1! (for example/whatever you chose)

  
![Annotation 2023-07-12 214439](https://github.com/isobarh/osticket-prereqs/assets/139295370/9e9145db-946d-44e2-8f5b-64e3fc962da9)
![Annotation 2023-07-12 214539](https://github.com/isobarh/osticket-prereqs/assets/139295370/21fdc0a7-db76-4aa1-9696-67b06dcae9ef)


<h2>Installation Steps</h2>
<p>
  -Install / Enable IIS in Windows WITH CGI and Common HTTP Features

  World Wide Web Services -> Application Development Features ->
  [X] CGI
  [X] Common HTTP Features

-AND IIS Management Console

  Internet Information Services -> Web Management Tools -> IIS Management Console
	[X] IIS Management Console
 </p>
<br />

![Annotation 2023-07-12 215814](https://github.com/isobarh/osticket-prereqs/assets/139295370/d4a96a64-d0f1-47c0-9f66-cbad64a5112b)

![Annotation 2023-07-12 215850](https://github.com/isobarh/osticket-prereqs/assets/139295370/1cda395d-4eb2-4391-ad9b-14d071aaa04d)

![Annotation 2023-07-12 220318](https://github.com/isobarh/osticket-prereqs/assets/139295370/27db6fce-06a5-4aa7-9f4b-f82db09f4b15)

![Annotation 2023-07-12 220354](https://github.com/isobarh/osticket-prereqs/assets/139295370/c2765ed3-0076-4851-bbb6-f600d08ac053)

![Annotation 2023-07-12 220517](https://github.com/isobarh/osticket-prereqs/assets/139295370/e41aa659-5a34-4f9f-a3f5-449f17cb14fd)

![Annotation 2023-07-12 221021](https://github.com/isobarh/osticket-prereqs/assets/139295370/597be610-8e24-4ecf-9a48-d4edb0efd0f8)


-download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)


![Annotation 2023-07-12 221539](https://github.com/isobarh/osticket-prereqs/assets/139295370/5c039bba-ed2a-4f3e-8693-b5cf03ea56d8)


-download and install the Rewrite Module (rewrite_amd64_en-US.msi)


![Annotation 2023-07-12 221704](https://github.com/isobarh/osticket-prereqs/assets/139295370/882d403b-e8e6-41cc-945a-3bbd225e9f99)


-Create the directory C:\PHP

![Annotation 2023-07-12 221944](https://github.com/isobarh/osticket-prereqs/assets/139295370/a8fc594e-c9d0-4c6d-a211-81d155cfc9b8)

-From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP

![Annotation 2023-07-12 222115](https://github.com/isobarh/osticket-prereqs/assets/139295370/7423c733-fd92-45a7-82e6-d42e37622414)

![Annotation 2023-07-12 222257](https://github.com/isobarh/osticket-prereqs/assets/139295370/e7ef52a3-6e29-4339-820f-afca86b92582)

-From the Installation Files, download and install VC_redist.x86.exe.

![Annotation 2023-07-12 222429](https://github.com/isobarh/osticket-prereqs/assets/139295370/7cd1e34d-e648-4785-8608-da05a3ed9813)

![Annotation 2023-07-12 222520](https://github.com/isobarh/osticket-prereqs/assets/139295370/54070083-08c6-42c4-95bb-7f2b208b6af0)

-From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

Typical Setup -> 

Launch Configuration Wizard (after install) -> 

Standard Configuration ->

Password1

![Annotation 2023-07-12 222604](https://github.com/isobarh/osticket-prereqs/assets/139295370/d0d4f3b0-b378-487b-95ad-ecc1d52167ad)

![Annotation 2023-07-12 222641](https://github.com/isobarh/osticket-prereqs/assets/139295370/ca5f3e85-cd91-4518-b6b3-6e4cffcf319e)

![Annotation 2023-07-12 222716](https://github.com/isobarh/osticket-prereqs/assets/139295370/855c82ba-56e5-4187-9b5c-36116d81fbc2)

![Annotation 2023-07-12 222751](https://github.com/isobarh/osticket-prereqs/assets/139295370/0e31b7a0-c112-4f06-9da3-fdc23843fcb8)

![Annotation 2023-07-12 222853](https://github.com/isobarh/osticket-prereqs/assets/139295370/4f0baa92-21ff-4a79-a7b7-eaf70d3481f4)

![Annotation 2023-07-12 223017](https://github.com/isobarh/osticket-prereqs/assets/139295370/4c5a414c-2398-42f4-87c5-f83bc3961223)

![Annotation 2023-07-12 223042](https://github.com/isobarh/osticket-prereqs/assets/139295370/4b6cc1f8-ad30-49a0-a4ff-48e79c8fb5bf)

-Open IIS as an Admin

-Register PHP from within IIS

-Reload IIS (Open IIS, Stop and Start the server)


![Annotation 2023-07-12 223157](https://github.com/isobarh/osticket-prereqs/assets/139295370/73c0aa08-84ce-4095-8c25-7af2db2f1ced)

![Annotation 2023-07-12 223512](https://github.com/isobarh/osticket-prereqs/assets/139295370/d2c3760e-18f9-41d5-9a66-f3711f8350a6)

![Annotation 2023-07-12 223625](https://github.com/isobarh/osticket-prereqs/assets/139295370/a81915bf-1403-41c9-87e3-45f5c8c50115)

-Install osTicket v1.15.8

-Download osTicket from the Installation Files Folder

-Extract and copy “upload” folder to c:\inetpub\wwwroot

-Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

-Reload IIS (Open IIS, Stop and Start the server)

-Go to sites -> Default -> osTicket

-On the right, click “Browse *:80”

-Note that some extensions are not enabled

-Go back to IIS, sites -> Default -> osTicket

-Double-click PHP Manager

-Click “Enable or disable an extension”

-Enable: php_imap.dll

-Enable: php_intl.dll

-Enable: php_opcache.dll

-Refresh the osTicket site in your browse, observe the changes


![Annotation 2023-07-12 224210](https://github.com/isobarh/osticket-prereqs/assets/139295370/113dc03f-aca9-4f34-8772-b079d0409752)

![Annotation 2023-07-12 224231](https://github.com/isobarh/osticket-prereqs/assets/139295370/f46b3590-bd23-4df9-a7c6-4a2319885fef)

![Annotation 2023-07-12 224250](https://github.com/isobarh/osticket-prereqs/assets/139295370/05a08163-21c7-44a7-9e33-bb1c8d8327f9)

![Annotation 2023-07-12 224313](https://github.com/isobarh/osticket-prereqs/assets/139295370/9f9bb22b-0edb-4a32-b52c-d08abd8af783)

![Annotation 2023-07-12 224519](https://github.com/isobarh/osticket-prereqs/assets/139295370/f10cf505-d175-47af-a3a5-54eda5c95c69)

![Annotation 2023-07-12 224558](https://github.com/isobarh/osticket-prereqs/assets/139295370/e93fb340-d041-4816-b00f-2c482e8016ef)

![Annotation 2023-07-12 224646](https://github.com/isobarh/osticket-prereqs/assets/139295370/d7009fdc-e9ad-42e1-b28b-ffb85c5d25c7)

![Annotation 2023-07-12 224709](https://github.com/isobarh/osticket-prereqs/assets/139295370/06114ab5-0ced-466b-b3c5-02c0b7462e0d)

![Annotation 2023-07-12 224927](https://github.com/isobarh/osticket-prereqs/assets/139295370/8b544d47-bc50-4ba8-8206-625781e31126)

![Annotation 2023-07-12 225110](https://github.com/isobarh/osticket-prereqs/assets/139295370/2a38e810-322f-4651-83ca-d823bb0b46ff)

![Annotation 2023-07-12 225237](https://github.com/isobarh/osticket-prereqs/assets/139295370/8c64565b-a23a-4102-bf70-d8965a0fc0b6)

![Annotation 2023-07-12 225355](https://github.com/isobarh/osticket-prereqs/assets/139295370/76bab04a-ae31-4971-a55d-c2cfc14af70c)

![Annotation 2023-07-12 225757](https://github.com/isobarh/osticket-prereqs/assets/139295370/85b7572e-d418-404d-a986-4b32e8a4c6f3)

![Annotation 2023-07-12 225818](https://github.com/isobarh/osticket-prereqs/assets/139295370/1421525f-a007-431a-a3e9-ac4fd7d77ffb)

-Rename: ost-config.php

-From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

-To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

![Screenshot 2023-07-12 230935](https://github.com/isobarh/osticket-prereqs/assets/139295370/05040f06-5929-4659-b55e-6196d8215082)

![Screenshot 2023-07-12 231040](https://github.com/isobarh/osticket-prereqs/assets/139295370/9cd808e3-60ce-449c-b24c-4eee040171fc)

-Assign Permissions: ost-config.php

-Disable inheritance -> Remove All

-New Permissions -> Everyone -> All

![Screenshot 2023-07-12 231731](https://github.com/isobarh/osticket-prereqs/assets/139295370/3889bb40-24e5-457b-a107-b506997226df)

![Screenshot 2023-07-12 231959](https://github.com/isobarh/osticket-prereqs/assets/139295370/867d7ab6-106e-4f76-99c0-7c23b5c9231b)

![Screenshot 2023-07-12 232105](https://github.com/isobarh/osticket-prereqs/assets/139295370/425e59e9-6774-4701-9267-1c102805da9f)

-Continue Setting up osTicket in the browser (click Continue)

-Name Helpdesk

-Default email (receives email from customers)

![Screenshot 2023-07-12 232707](https://github.com/isobarh/osticket-prereqs/assets/139295370/1394c30c-8980-4355-995c-5551bc67ea63)

-From the Installation Files, download and install HeidiSQL.

-Open Heidi SQL

-Create a new session, root/Password1

-Connect to the session

-Create a database called “osTicket”


![Screenshot 2023-07-12 233006](https://github.com/isobarh/osticket-prereqs/assets/139295370/bc802069-723c-49b4-9ea2-1ae735e7d580)

![Screenshot 2023-07-12 233206](https://github.com/isobarh/osticket-prereqs/assets/139295370/073d0075-2c75-42de-ab93-0aad34a6e104)

![Screenshot 2023-07-12 233429](https://github.com/isobarh/osticket-prereqs/assets/139295370/a6fb71c6-bf2d-4679-94aa-9dddfaeec38d)

![Screenshot 2023-07-12 235059](https://github.com/isobarh/osticket-prereqs/assets/139295370/2c960ab2-b3bc-4568-baa0-27dd8d23c187)

![Screenshot 2023-07-14 140759](https://github.com/isobarh/osticket-prereqs/assets/139295370/54c0683a-5362-4518-9745-f98ab1e7c744)

-Continue Setting up osticket in the browser

-MySQL Database: osTicket

-MySQL Username: root

-MySQL Password: Password1

-Click “Install Now!”

![Screenshot 2023-07-12 234119](https://github.com/isobarh/osticket-prereqs/assets/139295370/13b2ccd7-b185-4c33-a4e0-c635a35d0a74)

-Congratulations, hopefully it is installed with no errors!

-Browse to your help desk login page: http://localhost/osTicket/scp/login.php

-End Users osTicket URL:http://localhost/osTicket/ 

-Clean up

-Delete: C:\inetpub\wwwroot\osTicket\setup

-Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

-Notes:

-Browse to your help desk login page: http://localhost/osTicket/scp/login.php

-End Users osTicket URL: http://localhost/osTicket/ 

![Screenshot 2023-07-12 234216](https://github.com/isobarh/osticket-prereqs/assets/139295370/21b387d9-985b-4bf2-bb03-d4f7032aa8c7)

![Screenshot 2023-07-14 141158](https://github.com/isobarh/osticket-prereqs/assets/139295370/5be29da0-d75b-4649-9cd4-46abd9648fc9)

![Screenshot 2023-07-14 141653](https://github.com/isobarh/osticket-prereqs/assets/139295370/2107490b-33f9-4d85-a5d0-8eeed07447a2)


