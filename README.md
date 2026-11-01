
<a name="top"></a>
<h1>Active Directory Management</h1>

### 📋 Tickets Covered in This Repository

- 🏢 [**Ticket #82** — Managing Active Directory](#ticket-82)
- 🔑 [**Ticket #83** — Access Active Directory Services](#ticket-83)
- 📁 [**Ticket #84** — Create a New Organizational Unit](#ticket-84)
- 👤 [**Ticket #85** — Create a New User](#ticket-85)
- 👥 [**Ticket #86** — Create a New User Group](#ticket-86)
- 📝 [**Ticket #87** — Research and Create Documentation](#ticket-87)



<br />
<br />

---

<br />
<br />

<a name="ticket-82"></a>
<h1>Ticket #82 — Managing Active Directory</h1>

<h2>Languages and Utilities Used</h2>
- <b>Remote Desktop Connection (RDP)</b>
- <b>Active Directory Users and Computers</b>

<h2>Environments Used</h2>
- <b>Windows Server (Active Directory domain controller, sandbox.prod)</b>
- <b>Windows client (Remote Desktop)</b>
<br />
<h2>Project walk-through:</h2>

**Task:** Access the Windows Active Directory server to manage and administer user accounts.

**Objective:** Enhance system administration skills through identity management using Active Directory, following the "Windows Server User Management using Active Directory" wiki guide.

**Steps from the wiki guide:**
1. Connect to the Active Directory server via RDP.
2. Open Active Directory Users and Computers and navigate to sandbox.prod &gt; YellowTail.
3. Add a new user: right-click the target OU &gt; New &gt; User, fill in the details, set a password and finish.
4. Create a new group: right-click the OU &gt; New &gt; Group, enter a name and description, and click OK.
5. Reset a user's password: right-click the user &gt; Reset Password, enter the new password and click OK.

<br />
<br />
<br />
<p align="center">
<b>Opening Remote Desktop Connection and entering the Active Directory server's address:</b>
<br/><img width="464" height="267" alt="image" src="https://github.com/user-attachments/assets/f109ed27-19d0-4910-9ffb-10f6d8c8542f" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Entering the credentials for the connection (password hidden):</b>
<br/>
<img width="460" height="409" alt="image" src="https://github.com/user-attachments/assets/467d2994-2f34-4e52-980f-d5d4c8a2d83e" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Accepting the certificate warning for the domain controller DC01.sandbox.prod (certificate not from a trusted certifying authority):</b>
<br/><img width="397" height="413" alt="image" src="https://github.com/user-attachments/assets/918c4f71-b72c-4efc-ab76-8bfdd9f68d00" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Active Directory Users and Computers — Creating the organizational unit Rquaye-VITI under sandbox.prod/YellowTail/VITI (other users' OUs redacted):</b>
<br/>
<img width="1039" height="628" alt="image" src="https://github.com/user-attachments/assets/52f6c1cf-e7ae-44c4-833d-9eccd5e8d461" />

</p>

<br />
<br />
<br />
<p align="center">
<b>The new Rquaye-VITI organizational unit is created and selected (other users' OUs redacted):</b>
<br/><img width="1030" height="566" alt="image" src="https://github.com/user-attachments/assets/f07de08e-2934-41b4-9200-9fddc2d88095" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Right-clicking Rquaye-VITI &gt; New &gt; Group:</b>
<br/><img width="1036" height="857" alt="image" src="https://github.com/user-attachments/assets/aa4e66d2-d2cc-45cc-a87b-c23cc339a47d" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Creating the security group rquaye-apprentices (Global scope, Security type):</b>
<br/>
<img width="1048" height="628" alt="image" src="https://github.com/user-attachments/assets/c46db4e8-1636-4585-9acc-2ece357ec235" />


</p>

<br />
<br />
<br />
<p align="center">
<b>The rquaye-apprentices group now appears in the Rquaye-VITI OU:</b>
<br/>
<img width="1038" height="567" alt="image" src="https://github.com/user-attachments/assets/3ddcee68-4adc-4112-a65d-e9558f0215b2" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Right-clicking Rquaye-VITI &gt; New &gt; User:</b>
<br/><img width="1037" height="855" alt="image" src="https://github.com/user-attachments/assets/4826e3c4-4248-4dcf-9303-a09725f60fc6" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Entering the new user's name and logon name (Jim Test, jtest):</b>
<br/>
<img width="1044" height="610" alt="image" src="https://github.com/user-attachments/assets/54dd5ad1-bfce-4001-9438-ff7726a06dd4" />

</p>

<br />
<br />
<br />
<p align="center">
<b>Setting the initial password with &quot;User must change password at next logon&quot; selected (password hidden):</b>
<br/>
<img width="941" height="630" alt="image" src="https://github.com/user-attachments/assets/4e6c199b-2e9b-4f73-b19b-bea8d66a9e6f" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Reviewing the new user before finishing:</b>
<br/>
<img width="1047" height="652" alt="image" src="https://github.com/user-attachments/assets/ce239c7f-4ed4-47c6-aa94-686912e99460" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Confirming Jim Test is listed on the Members tab of rquaye-apprentices:</b>
<br/><img width="1032" height="774" alt="image" src="https://github.com/user-attachments/assets/0ef440b1-51fa-412d-b642-b7f61bd6dbb1" />


</p>

<br />
<br />
<br />

<b><u>Solution:</u></b> I connected to the Active Directory server (DC01.sandbox.prod) with Remote Desktop and accepted the certificate warning, since the server's certificate is not from a trusted certifying authority. In Active Directory Users and Computers I opened sandbox.prod &gt; YellowTail &gt; VITI and created my own working organizational unit, Rquaye-VITI, following the naming convention used by the other OUs in that tree. Inside it I created the security group rquaye-apprentices (Global scope) and a new user, Jim Test (jtest@sandbox.prod), with an initial password and "User must change password at next logon" selected. The group's Members tab showed Jim Test as a member. I then reset the account's password as a separate action, as step 5 of the wiki guide requires. The Members list also showed a second entry that appears to be the group itself, which I noted as a follow-up cleanup item instead of removing it right away.

<br />
<br />

<p align="right"><a href="#top">⬆ Back to top</a></p>

---


<br />
<br />

<a name="ticket-83"></a>
<h1>Ticket #83 — Access Active Directory Services</h1>

<h2>Languages and Utilities Used</h2>
- <b>Remote Desktop Connection (RDP)</b>
- <b>Active Directory Users and Computers</b>

<h2>Environments Used</h2>
- <b>Windows Server (Active Directory domain controller, sandbox.prod)</b>
- <b>Windows client (Remote Desktop)</b>
<br />
<h2>Project walk-through:</h2>

**Objective:** Enhance system administration skills through identity management using Active Directory.

**Instructions:**
1. Use the Remote Desktop Client (Windows or Mac) to connect to Active Directory services running on Windows Server.
2. Check the wiki page for step-by-step guidance.

<br />
<br />
<br />
<p align="center">
<b>Creating a new user, Eric Quaye (logon name equaye), in the Rquaye-VITI OU (other users' OUs redacted):</b>
<br/>
<img width="683" height="406" alt="image" src="https://github.com/user-attachments/assets/d4866dad-a4c3-467b-bd67-90f61491a23c" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Reviewing the new user before finishing; the password must be changed at next logon (other users' OUs redacted):</b>
<br/>
<img width="655" height="392" alt="image" src="https://github.com/user-attachments/assets/dfe338ce-bb2a-4d0a-ac12-9a02a9436cc6" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Right-clicking Rquaye-VITI &gt; New &gt; Group (other users' OUs redacted):</b>
<br/>
<img width="637" height="378" alt="image" src="https://github.com/user-attachments/assets/a75871a1-35db-4247-98eb-ad207fdd9b14" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Creating the security group rquaye-catalog (Global scope, Security type) (other users' OUs redacted):</b>
<br/>
<img width="530" height="520" alt="image" src="https://github.com/user-attachments/assets/91bd1a65-f25a-4e47-9f9f-83c19e21fed1" />


</p>

<br />
<br />
<br />
<p align="center">
<b>The Rquaye-VITI OU now holds the groups rquaye-apprentices and rquaye-catalog and the users Jim Test and Eric Quaye (other users' OUs redacted):</b>
<br/>
<img width="851" height="541" alt="image" src="https://github.com/user-attachments/assets/1fcfd757-2c87-4971-aa65-39c91c0cc300" />


</p>

<br />
<br />
<br />

<b><u>Solution:</u></b> I connected to the Active Directory server (DC01.sandbox.prod) with Remote Desktop, the same way as in <a href="#ticket-82">Ticket #82</a>, and opened Active Directory Users and Computers. Following the identity-management wiki guide, I went to my working OU, Rquaye-VITI, and created a new user, Eric Quaye, with an initial password. I then created the security group rquaye-catalog (Global scope) in the same OU and added Eric Quaye to it as a member, confirming he appeared in the group's Members list. Finally, I reset his password as a separate action to complete the last requirement from the guide. The OU now contains both groups and both test users.

<br />
<br />

<p align="right"><a href="#top">⬆ Back to top</a></p>

---


<br />
<br />

<a name="ticket-84"></a>
<h1>Ticket #84 — Create a New Organizational Unit</h1>

<h2>Languages and Utilities Used</h2>
- <b>Remote Desktop Connection (RDP)</b>
- <b>Active Directory Users and Computers</b>

<h2>Environments Used</h2>
- <b>Windows Server (Active Directory domain controller, sandbox.prod)</b>
- <b>Windows client (Remote Desktop)</b>
<br />
<h2>Project walk-through:</h2>

**Objective:** Enhance system administration skills through identity management using Active Directory.

**Instructions:**
1. To add a new Organizational Unit (OU) under the domain, use Active Directory Users and Computers.
2. The OU should be created under the already-created OU "VITI", named {freeipa_username}-VITI.
3. Check the separate step-by-step guidance.

**Note on redactions:** In the Active Directory screenshots, other users' OU names in the tree are redacted.

<br />
<br />
<br />
<p align="center">
<b>Right-clicking the VITI OU &gt; New &gt; Organizational Unit (other users' OUs redacted):</b>
<br/>
<img width="735" height="383" alt="image" src="https://github.com/user-attachments/assets/c84c4e54-e674-4c7f-b880-e79a305194ac" />


</p>

<br />
<br />
<br />
<p align="center">
<b>The Rquaye-VITI OU already exists under VITI and contains the groups and users created in Tickets #82 and #83 (other users' OUs redacted):</b>
<br/><img width="727" height="453" alt="image" src="https://github.com/user-attachments/assets/798bcc2c-1fa4-4f14-b6e9-957718d906f8" />


</p>

<br />
<br />
<br />

<b><u>Solution:</u></b> I connected to the Active Directory server with Remote Desktop, as in <a href="#ticket-82">Ticket #82</a>, and opened Active Directory Users and Computers. I navigated to sandbox.prod &gt; YellowTail &gt; VITI and right-clicked VITI to create a new organizational unit named Rquaye-VITI, the name this ticket requires ({freeipa_username}-VITI). Active Directory returned a "name already exists" error, which confirmed that Rquaye-VITI was already in place directly under VITI. I had created it while working on <a href="#ticket-82">Ticket #82</a>, using the same naming convention. The OU already holds the groups and users from Tickets #82 and #83, so the ticket's requirement is met.

<br />
<br />

<p align="right"><a href="#top">⬆ Back to top</a></p>

---


<br />
<br />

<a name="ticket-85"></a>
<h1>Ticket #85 — Create a New User</h1>

<h2>Languages and Utilities Used</h2>
- <b>Remote Desktop Connection (RDP)</b>
- <b>Active Directory Users and Computers</b>

<h2>Environments Used</h2>
- <b>Windows Server (Active Directory domain controller, sandbox.prod)</b>
- <b>Windows client (Remote Desktop)</b>
<br />
<h2>Project walk-through:</h2>

**Objective:** Enhance system administration skills through identity management using Active Directory.

**Instructions:**
1. Create a new user within the same Organizational Unit (OU) created in the previous task.
2. Any user name may be used.
3. Set the "Password never expires" option and set the password specified in the ticket.

**Note on redactions:** In the Active Directory screenshots, other users' OU names in the tree are redacted.

<br />
<br />
<br />
<p align="center">
<b>Creating a new user, Rob Santana (logon name rsantana), in the Rquaye-VITI OU:</b>
<br/>
<sub><i>Redaction: other users' OU names in the tree are redacted.</i></sub>
<br/>
<img width="616" height="517" alt="image" src="https://github.com/user-attachments/assets/672f8069-a596-4be1-a902-1b5f495bb051" />


</p>

<br />
<br />
<br />
<p align="center">
<b>Reviewing the new user's summary before finishing:</b>
<br/>
<sub><i>Redaction: other users' OU names in the tree are redacted.</i></sub>
<br/>
<img width="632" height="494" alt="image" src="https://github.com/user-attachments/assets/955d4a77-f175-4849-a0bb-44fc631bfd0a" />


</p>

<br />
<br />
<br />
<p align="center">
<b>The new user Rob Santana now appears in the Rquaye-VITI OU:</b>
<br/>
<sub><i>Redaction: other users' OU names in the tree are redacted.</i></sub>
<br/>
<img width="911" height="537" alt="image" src="https://github.com/user-attachments/assets/681ff4f7-c736-4c17-a215-9b487f828eae" />


</p>

<br />
<br />
<br />

<b><u>Solution:</u></b> I connected to the Active Directory server with Remote Desktop, as in <a href="#ticket-82">Ticket #82</a>, and opened Active Directory Users and Computers. I navigated to my working OU, Rquaye-VITI (created in <a href="#ticket-82">Ticket #82</a> and confirmed in <a href="#ticket-84">Ticket #84</a>), right-clicked it and chose New &gt; User. I created the user Rob Santana with the logon name rsantana@sandbox.prod and set the account password to the value given in the ticket (not shown here). Rob Santana now appears in the Rquaye-VITI OU alongside the groups and users created in the earlier tickets.

<br />
<br />

<p align="right"><a href="#top">⬆ Back to top</a></p>

---





