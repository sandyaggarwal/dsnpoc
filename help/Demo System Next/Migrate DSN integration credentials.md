---
title: Migrate DSN integration credentials
slug: gzW3-migra
createdAt: Tue Aug 29 2023 10:06:05 GMT+0000 (Coordinated Universal Time)
updatedAt: Mon Nov 27 2023 18:40:06 GMT+0000 (Coordinated Universal Time)
---

Demo System Next gains access to your IMS Organization via Adobe I/O integration. Recently, Adobe decided to deprecate previously used authentication mechanism based Service Account (JWT) and public/private key pairs. It is now possible and recommended to migrate to OAuth credentials. The added benefit is that OAuth credentials no longer enforce yearly key/secret rotation.

### Pre-requisites

- You need to have developer permissions and access to Demo System Next project in Adobe I/O.
- You need to get in touch with DSN team, to update credentials in our database.

### How to migrate

- 1\. Open [Adobe I/O developer console](https://developer.adobe.com/console/projects) for your org and find DSN integration project. Usually called simply `Demo System Next`
- ![](../../assets/TA8zsfFMXWtoBKP7lOVer_image.png)



- 2\. Find `Credentials` section and click `Service Account (JWT)` card.
- ![](../../assets/HPz4AVuB_MHiUqj7NfjvM_image.png)

* 3\. You will see a detailed deprecation message along with migration steps. Click on `Add new credential` button and confirm in the pop-up.
* ![](../../assets/eKMurtavvR0ZaPOZOuXy5_image.png)

- 4\. Once completed, you will see a new credential appear on the left, as well as a success toast on the bottom. Switch to new credential tab by clicking any of those two.
- ![](../../assets/o2fpgZc8Tr52pkH31BUgu_image.png)

* 5\. Scroll down to the `SCOPES` section. Copy the listed scopes with the highlighted button.


* ![](../../assets/_NAt5ok5OnBHaYG2jS83D_image.png)

- 6\. Update integration details within DSN:
  a) If you are marked as an org admin within DSN, visit <https://dsn.adobe.com/tools/org-admin> Send copied scopes along with your Org ID or Client ID to Demo System Next team, eg. by using contact form on <https://dsn.adobe.com/help>

  *Note to DSN team: paste scopes into *`adobeio_integrations.scopes`* field in databse and remove *`adobeio_integrations.accessToken`* Optionally, remove privateKey, but keep it in case we need to roll back.*

  7\. Wait for confirmation, that credentials have been updated in DSN.

  8\. Test if the integration continues to work (eg. check sandbox status on <https://dsn.adobe.com/environments>.


- ![](../../assets/DLXEZpoC6kw-bwwXiPEd0_image.png)

* 9\. Once you confirm that the new credentails are working, complete migration by removing old credentials. Click `Review and delete` button in Adobe I/O credentials, then in pop-up check if new credentails have already been used and confirm old credentail removal.
* ![](../../assets/UNucgFnneX8G6khd1NDUY_image.png)

  ![](../../assets/8Twv5f3B-aqH0TAgUblCG_image.png)

  ![](../../assets/gAX9Om-kxkyh6keeOMmBt_image.png)

