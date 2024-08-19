# Microsoft Entra ID: User, Group, and Role-Based Access Management with External Invitations

### Steps to Manage Users, Groups, and Access Control

## Architecture Diagram
![Entra ID User, Guest user and Groups](https://github.com/user-attachments/assets/fc16115a-99c0-4898-8746-9a18b80d0ff8)


1. **Sign in to the Azure Portal**:
   - Go to [https://portal.azure.com](https://portal.azure.com) and sign in with your Azure account credentials.

2. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory" or search for it in the search bar.

3. **Create Users**:
   - Click on "Users" under the "Manage" section.
   - Click on "+ New user" at the top.
   - Fill in the required user details.
   - Click "Create" to add the user.
  
![User](https://github.com/user-attachments/assets/b438250f-1836-4547-a074-8fbbf68f03cf)

4. **Create Groups**:
   - In the Azure Active Directory section, click on "Groups".
   - Click on "+ New group" at the top.
   - Fill in the required group details.
   - Click "Create" to add the group.
  
![group](https://github.com/user-attachments/assets/aff5eb1a-0894-47ed-abc8-b002e76f47e1)

5. **Manage Access Control for Users and Groups**:
   - After creating users and groups, navigate to the Azure resource you want to grant access to.
   - Click on "Access control (IAM)" in the left-hand menu.
   - Click on "+ Add role assignment".
   - Select the role you want to assign (e.g., Owner, Contributor, Reader).
   - Choose the user or group you want to grant the role to.
   - Click "Save" to assign the role.
   - Repeat this step for both users and groups as needed.
  
![Other user access](https://github.com/user-attachments/assets/9aab6b5e-f79a-4c1f-ac21-2e43fd4e4594)
![VM User access](https://github.com/user-attachments/assets/3f5be656-c1f1-4c12-96aa-2d5135443e8d)


7. **Invite External Users**:
   - In the Azure Active Directory section, click on "External identities".
   - Click on "+ Add guest user" at the top.
   - Fill in the email address of the external user you want to invite.
   - Customize the invitation message and set any additional options.
   - Click "Invite" to send the invitation.

8. **Login with User Account**:
   - Open a web browser and go to [https://portal.azure.com](https://portal.azure.com).
   - Enter the username and password of the user account you created earlier.
   - Click "Sign in" to log in to the Azure Portal.
  
![Login as senior user](https://github.com/user-attachments/assets/b22a1003-e129-4352-a304-14087c9b8c45)

![Login as other user](https://github.com/user-attachments/assets/0ac6ce97-62b0-43ce-b5d7-6343c3a1c86a)
