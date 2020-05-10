##### The Think - Bulid - Architect Mindset

>THINK

**Think** about the layout of your webpage or web app before writing code

>BUILD

**Build** your layout in HTML and CSS with a consistent structure for naming classes

>ARCHITECT

Create a logical **architecture** for your CSS with files and folders

>THINK
>😻 COMPONENT-DRIVEN DESIGN
* **Modular building blocks** that make up interface
* Held togther by the **layout** of the page
* **Re-usable** across a project, and between different projects
* **Independent**, allowing us to use them anywhere on the page

>BUILD
>😍 BEM (Block ELement Modifier)
>**BLOCK:** standalone component that is meaningful on its own.
>**ELEMENT:** part of a block that has no standalone meaning.
>**MODIFIER:** a different version of a block or an element

>ARCHITECT
>😜 THE 7-1 PATTERN
>7 different folders for partial Sass files, and
>1 main Sass file to import all other files info
>a compiled CSS stylesheet

###### THE 7 FOLDERS
>* base/
>* components/
>* layout/
>* pages/
>* themes/
>* abstracts/
>* vendors/