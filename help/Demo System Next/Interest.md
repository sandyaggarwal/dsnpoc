---
title: Interest
slug: 7fAJ-interest
createdAt: Fri Dec 01 2023 04:08:43 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Feb 20 2024 10:43:25 GMT+0000 (Coordinated Universal Time)
---

This page details the flow for presenting a standard demonstration of RT-CDP B2B/P (CDP) + Adobe Marketo Engage (AME) using the Bodea Public Project. Part 2 shows the development of Interest.

:::hint{type="info"}
**Bodea **public projects are connected to **Adobe Demo System Shared **org, **public-bodea **sandbox. All Adobe Employees can have read-only access to it.
:::

### **Business Objective (Recap)**

B2B Marketers are seeing a rise in the number of systems and data points that support their engagement marketing. Within the highly competitive digital marketplace, they need unique messaging strategies that give their sales people the greatest chance at closing opportunities. To support this objective, digital marketers want to leverage knowledge from previously untapped sources to track, resolve, and unify profile details at the person and account level in order to drive differentiated buying cycles with customers.

The following flow shows how Mark and others within the ABC Corporation Buying Group are monitored for progress as they go through the BodeaSecure Trial Experience. Events captured by RT-CDP are used to develop Audiences, whose members are then shared with Adobe Marketo Engage as static list members (updated in real-time for steaming audiences) to enhance the engagement marketing experience configured by Christina (Bodea Marketing Team).

### **Persona Intro (Recap):**

ABC Corporation has seen a rise in machines that are not compliant with the latest Antivirus updates within their organization. To assist with closing the compliance gaps Director of Security Shawna has asked her team to investigate a new solution for distributing and monitoring Antivirus installations across the organization.

Sr. Security Manager Mark, along with Security Analyst Rashid, from Shawna's team have been tasked with researching potential solutions. Together, the three team members make up the Buyer Group that is evaluating improved Antivirus solutions. The following scenario will show how RT-CDP helps track and connect activity within the Buyer Group to align engagement marketing through Marketo Engage. The enhancements will alert the Bodea sales team to key activities within the deal cycle and accelerate the sale to a close through greater access to previously untapped detail.

To begin, Mark and Rashid leave the latest team meeting and with the researching of potential solutions top of mind.

### **Interest Scenario**

### **Starting point**

<https://dsn.adobe.com/workspaces/bodea> or directly <https://dsn.adobe.com/web/bodea/home>

:::hint{type="info"}
Before next part of the journey reset your profile or open new incognito session with Bodea website.
:::

### **STEP 2 - INTEREST DEVELOPMENT & INTERACTION TRACKING**

Having viewed the recent Bodea Professional services webinar Mark and Rashid discuss the content that they viewed and agree that a Trial Evaluation of the BodeaSecure solution would help their team determine if the product is worth considering as a fit for ABC Corporation.

### **INSTRUCTIONS**

1\) Mark asks Rashid to setup a Trial Account for BodeaSecure to begin the evaluation.`Go to `<https://dsn.adobe.com/web/bodea/home>. `Make sure you are an anonymous visitor.`

![](../../assets/A3OGW29I4EjK_1HfSAEDI_image.png)

2\) Rashid browses the Marketplace on the website and navigates to BodeaSecure to learn more.

`Click on the "Marketplace" in the top navigation. Under "Recommended Software" click on the BodeaSecure.`

![](../../assets/JrCjDvkKzNN74lBTLShhV_image.png)

3\) Rashid reads more about the BodeaSecure Trial and signs up.

`Fill the form for Trial Registration. Click "Submit"`

![](../../assets/6hngCnoDvF6MgueNUqPe4_image.png)

4\) A few moments later Rashid receives an email with the link to start his BodeaSecure trial. He clicks on the link in the email.&#x20;

`Open your mailbox and read the message. Click the button "Start your trial".`

![](../../assets/yYGR49e3BfU_PIEWSyY3v_image.png)

5\) A new screen with Trial opens and Rashid is ready to start exploring.

`Look at the Profile Viewer - the audience profile is merged with an account. The audience was also assigned to: Bodea - Register for Trial`

![](../../assets/EEUaL0J4e68CsN22SL8W0_image.png)

6\) Rashid clicks on Step 1 and explores BodeaSecure Antivirus options.&#x20;

`Click on the BodeaSecure (Start now) link. A new page will open up and new audience will be resolved: Bodea - Trial Step 1 - Started.`

![](../../assets/2bOmuKm9fv7rORLwZOwPw_image.png)

7\) When done, Rashid confirms the step completion.&#x20;

`Click on the "I have completed Trial 1 button" Notice that another audience will be resolved "Bodea - Trial Step 1 - Completed" and the audience "Bodea - Trial Step 1 - Started" will be in Exited state`

![](../../assets/2jquwMIkZxgAxD2SvYxj5_image.png)

8\) For the demo, users can choose to access and complete as many of the Trial Steps as fits the conversation. The intention is to show marketers that it is possible to track progress with greater granularity, then share the detailed Audiences and Status to Marketo Engage to improve the accuracy, scoring, and assignment of audiences.

`Follow the same steps with other 3 steps. Appropriate audiences will be resolved. Open the profile in AEP, you will see all events there as well as Account to which this profile is assigned to. The data of the company are from SalesForce.`

![](../../assets/8mg29avvQT4mPsL4U12Is_image.png)

![](../../assets/k_hms6keL-5Fm7NE6FscB_image.png)

![](../../assets/oX5tFjKw_6ttaaR7Rbo8O_image.png)

![](../../assets/k8gv1b_Oy1E1ML59NSq3f_image.png)

9\) All of Rashid's interactions are tracked back to the unified profile found in RT-CDP, including resolution of identities across systems. For example, maybe Rashid used a personal email address to attend the original webinar and a work address to setup the Trial Account.

`Navigate to RT-CDP to show the tracking of Audiences, including the detail from Rashid's Trial interactions using the unified profile developed within the demo.`

![](../../assets/qn5Q67c2gEOMrzpLCF0zk_image.png)

10\) *Within the Audiences tab of RT-CDP, click on one of the Trial Tracking Segments to show the Detail. Overview the Audience Summary and how it is mapped to the Trial Progress Events.*

![](../../assets/Pfqt2h5hMAfXH7OcYdvPM_image.png)

*11) Based on Access & Permissions, click into the Edit Audience element to show the detailed ability to developed Audience Criteria. As needed, use your own instance to show the depth of audience configurations.*

![](../../assets/BTgpv0d6BeUKFr6Q6dTHf_image.png)

12\) In the Activated Destinations tile, click into the Bodea Destinations to see how Audiences are being shared with Marketo Engage through the pre-built connector.

![](../../assets/gpguNVhORtgGNlv42MfP4_image.png)

13\) Navigate back to the Audiences and click into a sample profile to show how RT-CDP is resolving identity within the Linked Identities tile.

![](../../assets/K-MaVrGBBvTUHp1U4x_8I_image.png)

14\) For a more in-depth and visual look at identity resolution, click View Identity Graph. Make sure that the "View Graph" selection is turned on.

![](../../assets/9jgHXdiOkQeGw_EaViA9i_image.png)

With Indicators of Interest showing that Rashid is taking the evaluation of BodeaSecure seriously, it is time to notify the sales team that ABC Corporation is a viable opportunity. The next section shows how Marketo Engage consumes the improved Segmentation detail from CDP to orchestrate enhanced Engagement Marketing.
