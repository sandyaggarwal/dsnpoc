---
title: Projects
slug: 608a-project-types
createdAt: Thu Aug 31 2023 10:57:33 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Jan 24 2024 14:39:30 GMT+0000 (Coordinated Universal Time)
---

Projects are configuration for DSN UI assets - websites, apps, Profile Viewer sidebar, etc. Each project has a type which determines the available configuration options.&#x20;
Project is identified by an ID, and in some cases by a user-friendly alias.&#x20;

## Aliases

Aliases are user-friendly labels that replace the not-so-user-friendly project IDs visible in links and your browser's address bar. By setting an alias for your project, you'll provide a smoother and more coherent experience for both you and your project's visitors.

Setting an alias is easy. Here's how to do it:

1. **Edit Your Project:**

   &#x20;Open your project, and navigate to the 'Access' tab.
2. **Alias Section:**

   &#x20;In the 'Access' tab, you'll find an 'Alias' section.
3. **Create Your Alias:**

   &#x20;Type in your desired alias for your project.
4. **Confirmation:**

   &#x20;Click the confirmation button, and if successful, you'll see an updated link to your project. Don't worry, the old links using the project ID will still work.

**Why Aliases Matter**

1. **Improved User Experience:** Aliases create a friendlier and more intuitive browsing experience for your project visitors. No more confusing project IDs in the address bar!
2. **Enhanced Demo Coherence:** Your project will have a consistent and professional appearance, which is crucial, especially when you're demonstrating your work to clients or stakeholders.
3. **Avoid Duplicate Aliases:** New aliases cannot match any existing alias or project ID. This ensures that every project gets its unique label.
4. **Sharing is Easy:** Sharing your project is a breeze with an alias. Simply send the link with the alias, and your recipients will instantly know what to expect.

**Consider the Community**

While setting up your alias, please consider the community of users. If you're no longer using an alias, remove it to free it up. Others will surely thank you!&#x20;

![](../../assets/ScClT78dx8iVki4zWenbg_dsn-testadobecomprojectsopawica-cxiushare.png)

## Sharing

Project can be shared with others in three main ways:

1. **Within DSN UI:** Project owner can assign user roles in Project's **Access** tab. All projects where you have a role of Editor or Observer will be visible in the shared project list. This works for all project types.
2. **With a link (web only):** You can simply copy a project URL visible in your Address Bar. This will still require user to authenticate, and will not allow non-editors to modify the project. For mobile projects, you can share the ID or alias.
3. **Access Link (web only):** You can generate a pre-authenticated link to your project. Anyone opening this link will be able to view it without having to sign in to DSN. Anonymous users will not be able to edit the project. Shared link can be generated in your Project's **Share** tab.

![](../../assets/oR5APpObN0KsmJ4wiXrkA_dsn-testadobecomprojectsopawica-cxiushare-1.png)

## Project metadata

The **Web**, **Customer Experience** and **Customer Hub** projects' settings allow you to set custom metadata. Enabling this metadata will allow you to add your own website's title, description and image that will be displayed in a snippet e.g. when sharing a link to your project on Slack, Teams or any other similar places that allow links previews.

:::hint{type="warning"}
Keep in mind that enabled metadata will be exposed and available without authentication to allow the link previews to work!
:::



- ![](../../assets/JnvRRoAesG7RdlUdhXpKY_withoutproxy.jpg "Link preview with metadata DISABLED")
- ![](../../assets/GGmXdIWXqiAgUSGbRRGFv_withproxy.jpg "Link preview with metadata ENABLED")

In order to set metadata, visit the Project's **Share** tab. At any time you can edit your metadata, change the title, description and images, or enable/disable metadata for the project, without losing the data you entered in the past - it would just become hidden if you disable metadata.

![](../../assets/qFavraHIOIVreyjcIfdNE_dsn-testadobecomprojectsopawica-cxiushare-2.png)

![](../../assets/auJ2PlOWD790Il3pyDvsz_dsn-testadobecomprojectsopawica-cxiushare-4.png "the Edit Metadata settings dialog")

### Universal project link prefix

For the **Web**, **Customer Experience** and **Customer Hub** projects you can now use a new URL address route schema for easier process of project sharing without having to remember its type. For this you can use the **p** prefix of the project ID/alias. e.g.

- **dsn.adobe.com/p/luma3** will redirect you to **dsn.adobe.com/web/luma3**
- **dsn.adobe.com/p/luma3-cx-app** will redirect you to **dsn.adobe.com/cx2/luma3-cx-app**

****
