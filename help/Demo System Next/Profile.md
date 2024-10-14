---
title: Profile
slug: sic7-profile
createdAt: Fri Oct 20 2023 13:24:14 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Oct 20 2023 13:48:17 GMT+0000 (Coordinated Universal Time)
---

Profile section in Profile Viewer is responsible for displaying information about the current user. It also has registration and sign in utilities

### Identities and Profile Details

Top section shows the identities informations as well as profile details, which are available in AEP for the current user. If you would like to change the fields being displayed there, you can do that by modifying your connected builder project.&#x20;

### Modifying displayed profile fields in profile viewer

- Open profile viewer and click the gear icon at the top

  or

  Open your project and switch to profile viewer tab
- ![](../../assets/GguuX7ITbnLIKs-BFqokx_image.png)

* In your project, review fields available in **Profile Viewer **tab section. They match the fields that are currently displayed in Profile Viewer on customer website.
* ![](../../assets/G0MiFBsZ-AaqDod4RTvti_image.png)

- You can add/remove/modify field names to match your story. In Under Armour example we will add an extra profile field: Shoe size.&#x20;
  To do that, click&#x20;

  **Add property **in the **Profile **section.

  **Label**: *Shoe size*

  **Path**:*$tenantId.individualCharacteristic.retail.shoeSize*

  Path can be copied from AEP UI. You can either use your exact tenant or $tenantId variable - it will be replaced automatically with your proper tenant name

  &#x20;In case of arrays use \[] brackets

  When your changes are done, refresh the web page with profile viewer to see that the new fields are visible there
- ![](../../assets/Oum3vqgqnoyHaEioFTcqg_image.png)

### You can update the values displayed in profile viewer also using dynamic values.

To access dynamic value in text (eg. Text component's content) use `${selector}` syntax, where selector matches

- **\<Path> **property for component that has Path set and no Form ID
  eg. `${enrollment.selectedPlan}`
  - *Tip: You can also use the path selector in the Profile Viewer options to refer to some information in Experience Events titles! For example:  *`${timestamp}`* will refer to *`entity.timestamp`* value of the particular event*
- **\<Name> **property for component that have Name set but no Path or Form ID,
  eg. `${email}`
- **formData.\<Form ID>.\<Path> **for component that has Form ID and Path set,
  eg. `${formData.registration.name.firstName}`
- **formData.\<Form ID>.\<Name> **for component that has Form ID and Name set but no Path,
  eg. `${formData.registration.email}`
- **\<Attribute selector> **for AEP Profile Schema attributes,&#x20;
  eg. `${person.name.firstName}`

The selectors can be used as inputs for the dynamic values formatting functions, e.g. `${formatDate:YOUR_SELECTOR}` will attempt to format the value behind your selector as a date. See [FAQ](docId:0mrMrRce-kwKEB5mIHPSr) for more information on the formatting functions.

##

## Segments

![](../../assets/3hGSFKaQFLeAa7yIqQhYq_image.png)

This section displays segments that are matching the current profile. It should display the same segments you defined and are resolved for the profile in AEP UI.&#x20;

In order to narrow the amount of displayed segments, use the filter available in the project.&#x20;

![](../../assets/lHyudxXyJHrr5zREcM8Qh_image.png)

## Utilities

![](../../assets/fcKKutbComxe4cDSwD-kH_image.png)

Registration and sign in utilities will allow you, instead of connecting registration/sign in form on external website, to use a generic dialog which will send data directly to AEP.
