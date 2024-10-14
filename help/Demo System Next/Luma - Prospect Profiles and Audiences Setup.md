---
title: Luma - Prospect Profiles and Audiences Setup
slug: iXzy-pro
createdAt: Wed Apr 24 2024 06:05:20 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Jun 05 2024 11:34:47 GMT+0000 (Coordinated Universal Time)
---

Prospect profiles are used to represent people who have not yet engaged with your company but you want to reach out to. With prospect profiles, you can supplement your customer profiles with attributes from trusted third-party partners.

## Behind the Scenes :&#x20;

![](../../assets/Z3hsP9ciW0FLTXDF7ruU__image.png)

## Setup for Luma :

### Identities

In preparation for receiving prospect profiles from your data partner, you must extend your data management framework in Real-Time CDP to accommodate this new profile type.

We have created a **Demo System Partner ID**.

![](../../assets/Pcr9-c-JBHrixs1-71Gu6_partnerid.png)

### Schema

In order to demonstrate use cases with Prospect profiles and audiences we need to have in place Schemas with **XDM Individual Prospect Profile **class.

So we have created two schemas **Demo System - Partner Data Prospecting Schema (Global v2.0)**, **Demo System - Partner Data Enrichment Schema (Global v2.0)**

![](../../assets/bF-f-fUzs-GuNHKBOKvVx_partnerschema1.png)

![](../../assets/D9GZ7gVsQQ3IXv_OyygQY_partnerschema2.png)

### Data Governance Label

Adding third-party data governance labels to all of the fields that make up the schema.This is important in order to ensure responsible use of third-party data and minimize the risk of data leakage.&#x20;

We will add **Third Party , Third party Prospecting, Third party Enrichment** label to all fields in schemas.

![](../../assets/IOI1bW4kfJD61tEsikqOV_partnerlabel1.png)

![](../../assets/S2otBfdCsiHXK_XCspIAW_partnerlabel2.png)

### Datasets

Now we are ready to ingest our prosect data into AEP as we have created two datasets where you can drop your CSVs or JSON files with prospect data and demostrate the use cases against those data, utilise them create a prospect audience, futher activate them to destinations.

**Demo System - Partner Data Prospecting Dataset**, **Demo System - Partner Data Enrichment Dataset (Global v2.0)**

![](../../assets/Mqc6J3usPg8b2WXO668ku_prospectdataset1.png)

![](../../assets/XevHD0_0UxjDGxUvkLB_R_prospectdataset2.png)

## Demo environments

- **AEP Sandbox**: [Public project - Luma](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/platform/home)

