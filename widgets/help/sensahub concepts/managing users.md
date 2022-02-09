<!--Managing Accounts and Users-->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Managing Accounts and Users

---

## About

So you've built your application, but you don't want everyone that interacts with it to have admin priveleges. This is where Accounts and Users come in.
In Sensahub, an Account is basically the company affiliation that a User has. For example, you can create a new account called "Google", and create multiple "Users" under the Account "Google" so that all Users from "Google" are grouped together.

<br>

---

<br>

### How to get to Account and User Configuration

<div class="column-container">
<div class="column row-container" style="width:70%;">

<br>

##### To get to the Account Manager, click **Settings** in the top navigation bar

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/settings.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

<br>

##### Then click on **Manage Accounts**

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/manage_accounts.png">
</div>
</div>

<br>

##### From here, we can add/remove/edit accounts and users.

<br>

<img src="/images/help/sensahub concepts/managing users/manage_accounts_screen.png">

<br>

---

<br>

## Adding Accounts
An account is the overarching category that a group of users fall under. Commonly this is defined as the name of the company. By default, the **sensahub** account is already there along with a default user **admin**. 


<div class="column-container">
<div class="column row-container" style="width:70%;">

1. Click the **+** next to the account dropdown to add a new account.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/create_account.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

2. Enter in the details for the account, such as the address of the businesses office, and the main person to contact. 

    Note that all of the fields that have a red asterisk are required to be filled out before the account can be added.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/created_account.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

3. Press the "Create" button, and the account will be created.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/press_create.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

4. After you press "Create", it will bring you back to the Account Manager. If you click on the **Account** dropdown, you can now select "Brisbane Bus Lines".

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/change_account.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

5. Currently there are no users for this account. Let's create some!

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/empty_account.png">
</div>
</div>

<br>

---

<br>

## Adding Users

A user belongs to an account. Each individual user has their own privileges and login details.

<div class="column-container">
<div class="column row-container" style="width:70%;">

1. To create a user, click on the "Add User" icon.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/add_user.png">
</div>
</div>

<br>

<div class="column-container">
<div class="column row-container" style="width:90%;">

2. Here you add the details for the user in. 
    - **Account Name** is the account that the user will belong to.
    - **User Dashboard** allows you to set different users to see different dashboards.
    - **Username** is the username that the user would enter to log into the dashboard.
    - **Password** is the password that the user would enter to log into the dashboard.
    - **Permission** determines what parts of the Sensahub application the user can see. A developer would have all of the priveleges, but our user Jerry here doesn't need to edit the application, so he only has permission to use the Dashboard.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/user_details.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:94%;">

3. Now press "Add" to add Jerry.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/user_added.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

4. That will bring us back to the Account Manager, and if we select the "Acme Pty Ltd" account, we can now see that the user Jerry has been added.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/jerry_added.png">
</div>
</div>




5. OPTIONAL If you want to test if the account works:

<div class="column-container">
<div class="column row-container" style="width:130%;">

- Logout from the current account

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/logout.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:130%;">

- Enter in the Username and Password for Jerry's account

    
</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/jerry_login.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:100%;">

- You should see that Jerry is only able to access the Dashboard, and none of the developer screens.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing users/jerry_logged_in.png">
</div>
</div>

> If you click on a user, you can edit their privileges and their details

---