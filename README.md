# Getting Started with Syncfusion Vue Accordion Component in Vue 3

**Repository Description**  
This repository contains a Vue 3 sample that demonstrates how to integrate and configure the Syncfusion **Vue Accordion** component in a Vue application.

The sample walks through installing the required Syncfusion packages, registering the Accordion component and its child directives, applying the necessary styles, and running the application to view the Accordion in action.

## Project Overview
The purpose of this project is to help developers understand how to use the Syncfusion Vue Accordion component in a Vue 3 environment. It provides a step‑by‑step setup process for rendering accordion items and structuring expandable sections within a Vue application.

## Features
- Integration of Syncfusion Vue Accordion in a Vue 3 application  
- Registration of Accordion components and child directives  
- Configuring accordion items using Vue templates  
- Applying required Syncfusion and dependency CSS styles  
- Running and testing the accordion locally  

## Prerequisites
Ensure the following requirements are met before running this project:
- Node.js (latest LTS recommended)  
- Vue 3  
- npm package manager  
- Visual Studio Code or a compatible IDE  

## Installation

### Adding Syncfusion Accordion package in the application

All the available Essential JS 2 packages are published in [`npmjs.com`](https://www.npmjs.com/~syncfusionorg) registry.

Install the `Accordion` component by using the below npm command.

```bash
npm install @syncfusion/ej2-vue-navigations --save
```

### Adding Syncfusion Vue Accordion in the application

You have completed all the necessary configurations needed for rendering the Syncfusion Vue component. Now, you are going to add the Accordion component using following steps.

  1. Import the Accordion component in the `<script>` section of the `src/App.vue` file.

     ```html
     <script>
       import { AccordionComponent, AccordionItemDirective, AccordionItemsDirective } from "@syncfusion/ej2-vue-navigations";
      </script>
     ```

  2. Register the Accordion component along with the required child directives which are used in this example. Find the list of child directives and the tag names that can be used in the Accordion component in the following table.
    
        | Directive Name   | Tag Name    |
        |------------------|-------------|
        | `AccordionComponent` | `ejs-accordion` |
        | `AccordionItemsDirective`  | `e-accordionitems`  |
        | `AccordionItemDirective`  | `e-accordionitem`  |
        
    ```js
        import { AccordionComponent, AccordionItemDirective, AccordionItemsDirective } from "@syncfusion/ej2-vue-navigations";
        //Component registeration
        export default {
            name: "App",
            components: {
            "ejs-accordion": AccordionComponent,
            "e-accordionitems": AccordionItemsDirective,
            "e-accordionitem": AccordionItemDirective,
            }
        }
    ```
 In the above code snippet, you have registered Accordion and its child directives. AccordionItem Directive is  used for defining the accordion item.

3. Add the component definition in template section.

    ```html
    <template>
        <ejs-accordion>
            <e-accordionitems>
                <e-accordionitem
                    expanded="true"
                    header="ASP.NET"
                    content="Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services."
                ></e-accordionitem>
                <e-accordionitem
                    header="ASP.NET MVC"
                    content="The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller."
                ></e-accordionitem>
                <e-accordionitem
                    header="JavaScript"
                    content="JavaScript (JS) is an interpreted computer programming language.It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed."
                ></e-accordionitem>
            </e-accordionitems>
        </ejs-accordion>
        </template>
    ```

4. Adding CSS reference for Syncfusion Vue Accordion component

    Import the needed css styles for the Accordion component along with dependency styles in the `<script>` section of the `src/App.vue` file as follows.

    ```js
     <script>
       import "../node_modules/@syncfusion/ej2-base/styles/material.css";
       import "../node_modules/@syncfusion/ej2-vue-navigations/styles/material.css";
     </script>
    ```

5. Summarizing the above steps, update the `src/App.vue` file with following code.

    ```html
    <template>
        <ejs-accordion>
            <e-accordionitems>
                <e-accordionitem
                    expanded="true"
                    header="ASP.NET"
                    content="Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services."
                ></e-accordionitem>
                <e-accordionitem
                    header="ASP.NET MVC"
                    content="The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller."
                ></e-accordionitem>
                <e-accordionitem
                    header="JavaScript"
                    content="JavaScript (JS) is an interpreted computer programming language.It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed."
                ></e-accordionitem>
            </e-accordionitems>
        </ejs-accordion>
        </template>

        <script>
            import {AccordionComponent, AccordionItemDirective, AccordionItemsDirective} from "@syncfusion/ej2-vue-navigations";

            import "../node_modules/@syncfusion/ej2-base/styles/material.css";
            import "../node_modules/@syncfusion/ej2-vue-navigations/styles/material.css";

            //Component registeration
            export default {
                name: "App",
            components: {
                "ejs-accordion": AccordionComponent,
            "e-accordionitems": AccordionItemsDirective,
            "e-accordionitem": AccordionItemDirective,
            }
        }
        </script>
    ```

### Running the application
Run the application using the following command.
```bash
npm run serve
```
Open the URL shown in the terminal (typically `http://localhost:8080`) to view the Syncfusion Vue Accordion component in the browser.

## Documentation
- General Syncfusion documentation:
https://help.syncfusion.com/
- Vue Introduction:
https://ej2.syncfusion.com/vue/documentation/introduction
- Vue Accordion Getting Started (Vue 3):
https://ej2.syncfusion.com/vue/documentation/accordion/getting-started-vue-3

## Additional Resources
- Syncfusion Vue Accordion product overview:
https://www.syncfusion.com/vue-components/vue-accordion

## Troubleshooting
- Ensure the correct Vue 3 version is used.
- Re‑run npm install if dependencies are missing.
- Verify that Syncfusion CSS files are properly included.
- Restart the development server after configuration changes.

## Support
For detailed API references, advanced configuration options, and feature explanations, refer to the Syncfusion Vue Accordion documentation links provided above.