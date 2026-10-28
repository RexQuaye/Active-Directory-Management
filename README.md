
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
