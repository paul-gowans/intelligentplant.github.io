# App Safe- and Block-List Management

The App Store uses the concept of safe- and block-lists to control the
apps that an organization's users are allowed to sign in to.

**Important:** By default, safe-listing is disabled for newly-registered
organizations, meaning that its users can sign in to any app that is not
block-listed. **Intelligent Plant recommends enabling the safe list for
full control over app access.**

To view the app access overview page, click on the *Configure the safe-
and block-listed apps for \<Your Organization Name\>* link in the
organization portal actions. The overview page displays a summary of the
safe- and block-list status:

![Safe list status
(disabled)](/general/orgs/admin/app-access/safe-list/app-safe-list-disabled.png)

To enable the safe list, click on *Enable Safe List*:

![Safe list status
(enabled)](/general/orgs/admin/app-access/safe-list/app-safe-list-enabled.png)

When the safe list is enabled, it can be disabled by clicking on
*Disable Safe List*.

## Managing the Safe List

When the safe list is enabled, click on *Manage Safe-Listed Apps* on the
app access overview to open the safe list management page:

![Safe-listed
apps](/general/orgs/admin/app-access/safe-list/app-safe-list-1.png)

### Adding Apps to the Safe List

To add apps to the safe list, click on the *Add Apps to Safe List*
button. This will open the app browser, allowing you to page through the
available apps and select the ones you want to add to the safe-list:

![App
browser](/general/orgs/admin/app-access/safe-list/app-safe-list-2.png)

Click on the *Save Changes* button to apply the changes:

![Updated safe-listed
apps](/general/orgs/admin/app-access/safe-list/app-safe-list-3.png)

### Removing Apps from the Safe List

Click on the *Remove* button next to a safe-listed app to remove it from
the safe list.

### Managing Access Permissions

You can restrict access to any app to specific organization groups and
users. To manage permissions for a safe-listed app, click on *Authorized
Users and Groups* next to the list entry:

![Safe-listed app
permissions](/general/orgs/admin/app-access/safe-list/app-safe-list-4.png)

By default, when an app is added to the safe list, the *All Users* group
is granted access permissions to the app. Existing permissions can be
removed by clicking on the *Remove* button next to the entry.

Grant permission to a group by clicking on the *Add Groups* button.
Similarly, permissions for individual users can be granted by clicking
on the *Add Users* button. These actions will display the group browser
and user browser respectively, where you can select the items to grant
app permissions to:

![Group
browser](/general/orgs/admin/app-access/safe-list/app-safe-list-5.png)
![User
browser](/general/orgs/admin/app-access/safe-list/app-safe-list-6.png)

In both cases, click on *Save Changes* to apply the changes:

![Updated safe-listed app
permissions](/general/orgs/admin/app-access/safe-list/app-safe-list-7.png)

If you view the assigned apps for affected
[users](/general/organization_user_and_data_management/user_management#viewing_assigned_apps)
or
[groups](/general/organization_user_and_data_management/group_management#viewing_assigned_apps),
you will see that their assigned app list has been updated, e.g.

![Updated assigned apps list for
user](/general/orgs/admin/app-access/safe-list/app-safe-list-8.png)

## Managing the Block List

From the app access overview page, click on *Manage Block-Listed Apps*
to open the block list management page:

![Block-listed
apps](/general/orgs/admin/app-access/block-list/app-block-list-1.png)

### Adding Apps to the Block List

Adding an app to the block list will immediately prevent all users in
the organization from using the app, even if it has been safe-listed.

To block-list an app, click on *Add Apps to Block List*. This will open
the app browser, allowing you to page through the available apps and
select the ones you want to add to the block-list:

![Selecting apps to add to the block
list](/general/orgs/admin/app-access/block-list/app-block-list-2.png)

Click *Save Changes* to update the block list:

![Updated block
list](/general/orgs/admin/app-access/block-list/app-block-list-3.png)

### Removing Apps from the Safe List

Click on the *Remove* button next to a block-listed app to remove it
from the block list.
