<h2 class="toc">Configure Salesforce Omnichannel for Testing</h2>

In order to sync your Connect User status with your Omni-Channel agent
status, you must configure Omni-Channel Presence Syncing. This will make
your Omni-Channel presence status match your Amazon Connect Agent Status
and vice versa.

<h3 class="toc">Enable Omnichannel</h3>

First, we must enable omni-channel. Once you enable Omni-Channel, you
will have access to the other components in Salesforce that will be
required for Omni-Channel setup.

<h4 class="toc">Enable Omnichannel in Your Salesforce Org</h4>

1.  Log in into your Salesforce org and go to **Setup**

2.  In the **Quick Find** field, enter omni and choose **Omni-Channel
    Settings** from the results

<img src="../media/image230.png" />

3.  Select the checkbox for Enable Omni-Channel and choose Save

<img src="../media/image231.png" />

4.  Omni-Channel is now enabled.

<h3 class="toc">Configure Presence Statuses</h3>

Once you have enabled Omni-Channel, you will need to configure presence
statuses to reflect the different presence states that you wish your
Omni-Channel agents to enter. These do not need to match agent statuses
in Amazon Connect exactly, but it does make it easier to track what you
are doing.

<h4 class="toc">Add a Presence Status</h4>

1.  Log in into your Salesforce org and go to **Setup**

2.  In the **Quick Find** field, enter presence and choose **Presence
    Statuses** from the results

<img src="../media/image147.png" />

3.  In the Presence Statuses page, choose New

4.  Provide a status name, for example Lunch

5.  Set the Status options appropriately, for example, Busy

6.  For Online statuses, you will need to provide a channel. Please
    reference the [Omni-Channel
    documentation](https://help.salesforce.com/articleView?id=omnichannel_intro.htm&type=5)
    for details

7.  Choose Save

<img src="../media/image148.png" />

8.  Repeat as necessary for all desired statuses

<h3 class="toc">Configure Profiles to Use the New Statuses</h3>

Before agents can use the statuses that have been configured, you will
need to make sure that they have been provided rights to them. This is
done by modifying the profiles assigned to your agents.

<h4 class="toc">Modify Profiles to Use New Statuses</h4>

1.  Log in into your Salesforce org and go to **Setup**

2.  In the **Quick Find** field, enter profiles and choose **Profiles**
    from the results

<img src="../media/image149.png" />

3.  Select the profile assigned to your users

4.  Hover over the Enabled Service Presence Status link and choose Edit

<img src="../media/image150.png" />

5.  Select the available status from the left, then choose the Add
    button to add it the Enabled Service Presence Statuses field

<img src="../media/image151.png" />

6.  Select Save

7.  Repeat as necessary for other statuses or profiles.

<h3 class="toc">Add Omni-Channel to the Utility Bar</h3>

To provide agents access to the Omni-Channel tool, you will need to add
it to the Service Console.

<h4 class="toc">Add the Omni-Channel Utility Item</h4>

1.  Log in into your Salesforce org and go to **Setup**

2.  In the **Quick Find** box, type **App Manager**, then choose **App
    Manager** from the result list.

<img src="../media/image17.png" />

3.  Expand the drop-down menu associated to Service Console and select
    **Edit**.

<img src="../media/image18.png" />

4.  Once the **Lightning App Builder** opens, select **Utility Items**
    from the left Navigation

<img src="../media/image19.png" />

5.  Choose Add Utility Item, then select Omni-Channel

<img src="../media/image232.png" />

6.  Adjust the order of the utility items as desired and select Save.

7.  Return to the Service Console and refresh your browser.

8.  You should now see the Omni-Channel utility item.

<img src="../media/image233.png" />
