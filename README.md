[![Netlify Status](https://api.netlify.com/api/v1/badges/d8639fec-8a32-438c-9f68-aeb9db8e16be/deploy-status)](https://app.netlify.com/sites/youthful-bhaskara-adf2d8/deploys)

# LPL Resource library build using [Vitepress](https://vitepress.vuejs.org/)
---
## Setup
Download the repo and run `yarn install` .

Requirements: `node v16` (preffered) or `node v14`. To check node version run `node -v` command.



## Development
To open local dev server use `yarn run site:dev` command.

## Adding text resources
You can edit any file directly from the `edit on github link` at the bottom of the resource.

To edit `home page` or `resources` just edit the corresponding `.md` files.

```
. 
ââ đ site
â  ââ đ .vitepress
â  â  
â  ââ đ resources <--- âšī¸ Organize your files here 
â  â  ââ đ guides <--- âšī¸ Folders structure generates paths eg: resources/guides/your-file-name 
â  â  ââ đ ...  
â  â
â  ââ index.md <--- âšī¸ The Home Page
â 
ââ package.json
ââ README.md
.

```

## Adding the resources to the **sidebar** and top **navigation** menu
You can links to internal or external items in the `config-sidebar.js` file or `config-nav.js`.

Always include the full file path for any resources that are nested in folders eg:
 ```js
 {
    text: "Learning Guides",
    link: "/resources/guides/wallet/wallet-setup",
}
 ```

The config files are located in `.vitpress` directory:

```
. 
ââ đ site
â  ââ đ .vitepress
â  â  ââ đ theme
â  â  ââ config.js 
â  â  ââ config-sidebar.js <--- âšī¸ Site sidebar links
â  â  ââ config-nav.js <--- âšī¸ Top Navigation links
.

```

> **Warning**
> Any modification, **new file**,  **file name** or **folder structure change** must be **manually added** to the `config-sidebar.js` file or `config-nav.js`.
> If you forget to update the files it **will result in 404 pages**.


## Adding images and files
### Public and Private files
Images and files can be added in **two ways**
- in public directory
    - always published when the site is build.
- in other directories (private)
    - only published if there are direct links from one of the articles. 
### Organizing files
If you have a lot of image or file resources for a guide **consider making a dedicated folder for your article** and name the article file as `index.md`.

### Pasting images directly into Markdown
To [Paste Image VS Code](https://marketplace.visualstudio.com/items?itemName=mushan.vscode-paste-image) 
When you edit a file and paste an image into markdown it will automatically be saved in root folder of the file.




## Other configurations
Vitepress is modular and most features can be modified or disables in the `config.js` file.
Consult  [Vitepress docs](https://vitepress.vuejs.org/) for more information.

```
. 
ââ đ site
â  ââ đ .vitepress
â  â  ââ đ theme
â  â  â  ââcustom.css <--- âšī¸ Custom css goes here
â  â  ââ config.js <--- âšī¸ Social icons, footer, site title, description, any head links
.

```




