<h2 class="toc">Contact Trace Record Import</h2>

In Amazon Connect, data about contacts is captured in contact trace
records (CTR). This data can include the amount of time a contact spends
in each state: customer on hold, customer in queue, agent interaction
time. The basis for most historical and real-time metrics in Amazon
Connect is the data in the CTR. When you create metrics reports, the
values displayed for **most** (not all) metrics in the report are
calculated using the data in the CTRs.

CTRs are available within your Amazon Connect instance for 24 months
from the time when the associated contact was initiated. You can also
stream CTRs to Amazon Kinesis to retain the data longer, and perform
advanced analysis on it. Additionally, with the AWS Serverless
Application Repository for Salesforce, you can import Contact Trace
Records into your Salesforce org.

<h3 class="toc">Contact Trace Record Import</h3>

Once enabled during the AWS Serverless Application Repository for
Salesforce, CTR import is activated on a call by call basis by adding a
specific contact attribute. This attribute is used during Contact Trace
Record processing to trigger the import task.

<h4 class="toc">Enabling Contact Trace Record Import</h4>

1.  Login to your Amazon Connect instance as an Administrator

2.  From the left navigation, choose **Routing** then select **Contact
    flows**

    
<img src="../media/image201.png" />

3.  Open the contact flow that you want to use to enable call recording
    import.

4.  In you contact flow, before you transfer to queue, add a new **Set
    contact attributes** block

5.  Configure the block to set a contact attribute as follows:

    a.  **Destination key:** postcallCTRImportEnabled

    b.  **Value:** true

<img src="../media/image214.png" />

6.  **Save** the Set contact attributes block. Make sure it is
    appropriately connected to your contact flow, and **Publish** the
    flow.

7.  Wait approximately 2 minutes to give the contact flow time to
    publish.

8.  Place a call, connect to your agent, speak for a few moments, then
    end the call. Make sure the agent exits after call work

9.  The Contact Trace Record is emitted shortly after call completion
    and the import happens almost immediately.

<h4 class="toc">Adding Contact Trace Records to the Service Console</h4>

1.  Log in into your Salesforce org and go to the **Service Console**

2.  Expand the **navigation menu** by selecting the down arrow and
    choose **Edit**.

    
<img src="../media/image40.png" />

3.  On the Edit Service Console App Navigation Items page, select **Add
    More Items**

    
<img src="../media/image41.png" />

4.  Select the **+** next to **AC Contact Trace Records**

5.  Select **Add 1 Nav Item**

6.  Change the order of your Navigation Items if desired, then choose
    **Save**

    
<img src="../media/image215.png" />


7.  Once the save completes, expand the **navigation menu** by selecting
    the down arrow and choose **AC Contact Trace Records**
    
<img src="../media/image216.png" />

8.  Change the list view from Recently Viewed to **All**

<img src="../media/image217.png" />

9.  Once the view refreshes, you should see your record(s)

<img src="../media/image218.png" />

10. Select a record to view it

11. Note the ContactId value from Amazon Connect

<h3 class="toc">Display Additional Contact Trace Record Data</h3>

By default, the AC Contact Trace Record layout only contains the
ContactId. However, all of the CTR data has been imported. It is likely
that you will want to customize this view to show more data.

<h4 class="toc">Customizing the AC Contact Trace Record Layout</h4>

1.  Log in into your Salesforce org and go to **Setup**

2.  In the **Quick Find** field, enter object and choose **Object
    Manager** from the results

    
<img src="../media/image219.png" />

3.  In the Object Manager, find the **AC Contact Trace Record** object
    and select it

    
<img src="../media/image220.png" />

4.  In the left navigation, choose **Page Layouts**

5.  Select **AC Contract Trace Record Layout**

6.  Select items from the Fields section and add them to the layout as
    you wish. In the example below, I have selected Agent Username,
    Queue Name, Queue Duration, After Contact Work Duration, Agent
    Interaction Duration, and Attributes
    
    
<img src="../media/image221.png" />

7.  **Save** the layout

8.  Return to the **Service Console**

9.  **Refresh** the browser

10. Expand the **navigation menu** by selecting the down arrow and
    choose **AC Contact Trace Records**

    
<img src="../media/image216.png" />

11. Select a contact trace record

12. You should now see your modified layout

<img src="../media/image222.png" />
