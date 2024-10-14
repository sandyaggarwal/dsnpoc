---
title: Profile Viewer
slug: LcYM-profile-viewer
createdAt: Fri Oct 20 2023 09:47:30 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Jan 05 2024 12:05:24 GMT+0000 (Coordinated Universal Time)
---

- Profile viewer is a tool available on DSN front-end UI's to help you tell the story without the need to switch to other interfaces. It is available for website, mobile app and cx app, as well while using the customer website.


- ![](../../assets/a5g52yr-FsEgGW8fow0IZ_image.png)



You can find a description of each section in following articles

[Profile](<../Demo System Next/Profile.md>)

[Events](<../Demo System Next/Events.md>)

[Offers](<../Demo System Next/Offers.md>)

[Debug](<../Demo System Next/Debug.md>)

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

###

