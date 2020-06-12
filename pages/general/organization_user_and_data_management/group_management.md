# Group Management

Click on *View App Store Groups for the organization* in the
organization portal to open the group management page:

![Groups list (administrator
view)](/general/orgs/admin/groups/admin-groups-list.png)

Note that this page does not display groups from your own organization
directory; App Store group definitions and memberships are held within
the App Store itself.

When your organization is registered with the App Store, two groups are
automatically created:

  - ***All Users*** - any user from your organization who joins the App
    Store will be added to this group.
  - ***Administrators*** - members of this group have the ability to
    create and manage users, groups, app access permissions and so on.

Intelligent Plant will contact you once your organization has registered
to identify which users should be added to the Administrators group.
Members of this group can then add or remove other members as required.

## Viewing Group Details

Click on the *Details* button to view the details for the group,
including group memberships:

![Group details (administrator
view)](/general/orgs/admin/groups/admin-group-members-2.png)

Note that non-administrator users cannot view group memberships.

## Viewing Assigned Apps

Click on *View Assigned Apps* to see the apps that members of the group
are allowed to sign in to:

![Assigned apps (administrator
view)](/general/orgs/admin/groups/admin-assigned-apps-group.png)

App access is controlled via [app safe- and block-list
management](/general/organization_user_and_data_management/app_access_management).

## Creating a New Group

From the Group Management page, click on *Create a new group* to open
the group editor:

![Group editor](/general/orgs/admin/groups/admin-create-group.png)

Enter the group details and click on *Create Group* to create the group.

**A note on externally-visible groups:** By default, organization groups
are only visible to members of your own organization. However, it is
also possible to mark a group as being externally visible. This does not
make the group visible to everyone on the App Store; it is only visible
to 3rd party organizations that have [marked your organization as
trusted](/general/organization_user_and_data_management/trust_management).

The primary reason for creating externally-visible groups is to allow
3rd parties to grant data source access to your users e.g. to assist
with app troubleshooting.

## Adding Users to Groups

From the group details page, an administrator can add users to a group
by clicking on *Add Users* on the group details page. This will open a
user browser where you can search for the users to add to the group:

![Add users to
group](/general/orgs/admin/groups/admin-add-users-to-group.png)

Select the users to add by clicking on the *Select* button next to the
user. Click *Save Changes* to add the selected users to the group:

![Updated group members](/general/orgs/admin/groups/admin-new-group.png)

## Removing Users from Groups

To remove a user from a group, click on the *Remove* button next to the
user in the group details page. Users cannot be removed from the *All
Users* group.
