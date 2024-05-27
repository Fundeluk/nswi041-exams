## Test Conditions: Use Case - Update subject info
<table>
    <thead>
        <th>ID</th>
        <th>Name</th>
        <th>Description</th>
    </thead>
    <tr>
        <td>T_COND_01</td>
        <td>Closing the site while updating does not save changes</td>
        <td>Test that the updated info is not saved if the site is closed during the updating process</td>
    </tr>
    <tr>
        <td>T_COND_02</td>
        <td>Check for collisions</td>
        <td>Test that no collisions with other subjects appear after updating</td>
    </tr>
    <tr>
        <td>T_COND_03</td>
        <td>Updated information persists</td>
        <td>Test whether the information gets saved in the database after updating the info</td>
    </tr>
    <tr>
        <td>T_COND_04</td>
        <td>Update notification</td>
        <td>Test whether all relevant people are notified about the change</td>
    </tr>
    <tr>
        <td>T_COND_05</td>
        <td>Validation</td>
        <td>Test whether the updated info is valid before saving it</td>
    </tr>
</table>

## Test case 1 
<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_01</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Updated information persists</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The subject already exists. The user doing the updating has required access rights.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The updated information is saved in the database and is shown to all users that view the subject info.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account rights, updated information about subject.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_COND_02, T_COND_03, T_COND_04, T_COND_05</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Access the subject information page on the website.</td>
        <td>The page is accessible.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Start the editation process</td>
        <td>The service is working</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Fill out the new information</td>
        <td>The new information is being shown in place of the old one</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Click a confirmation button.</td>
        <td>If the new info is valid and no collisions with other subjects were found, the data is saved and from this point on shown to all other users. All of the relevant users are notified about the change.</td>
    </tr>
</table>

## Test case 2
<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_02</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">New information does not persist if not validated and confirmed</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The subject already exists. The user doing the updating has required access rights.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The information about the subject does not change</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account rights, updated information about subject.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_COND_01, T_COND_05</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Access the subject information page on the website.</td>
        <td>The page is accessible.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Start the editation process</td>
        <td>The service is working</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Fill out the new information</td>
        <td>The new information is being shown in place of the old one</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>The site is closed or the information is not valid and the confirm button is clicked</td>
        <td>The new info is not saved anywhere and the old info is still shown to everyone.</td>
    </tr>
</table>
