#5. Global Assets
We separate some assets that can be used in all layouts into standalone folder named ```global```.

The pre-complied files list belew

    global/
    ├── css/
    ├── fonts/
    │   ├── brand-icons/
    │   │   ├── brand-icons.css
    │   │   ├── brand-icons.ttf
    │   │  ...
    │   │
    │   ├── font-awesome/
    │   │   ├── font-awesome.css
    │   │   ├── font-awesome.ttf
    │   │  ...
    │  ...
    │
    ├── js/
    │   ├── components/
    │   ├── components.js (combine the files in components folder)
    │   ├── configs/
    │   ├── plugins/
    │   └── core.js
    └── vendor/
        ├── bootstrap/
        │   ├── bootstrap.js
        │   └── bootstrap.min.js
        ├── jquery/
        │   ├── jquery.js
        │   └── jquery.min.js
        ├── jquery-selective/
        │   ├── jquery-selective.css
        │   ├── jquery-selective.min.css
        │   ├── jquery-selective.js
        │   └── jquery-selective.min.js
       ...

And The source files you can see below

    global/
    └── src/
        ├── fonts/
        │   ├── brand-icons/
        │   │   └── brand-icons.less
        │  ...
        │
        ├── es/
        │   ├── components/
        │   ├── configs/
        │   ├── plugins/
        │   └── core.js
        ├── scss/
        │   ├── bootstrap/ (bootstrap source files)
        │   ├── bootstrap_extend/ (improvements styles for remark)
        │   ├── mixins/ (basic scss mixins from bootstrap)
        │   ├── mixins/ (more useful mixins we defined)
        │   ├── components/ (the components we added to remark)
        │   └── _vars.scss
        ├── skins/
        └── vendor/
            ├── jquery-selective/
            │   └── jquery-selective.scss
           ...

We use [assets-manager](https://github.com/amazingSurge/assets-manager) to copy all 3rd vendors to `global/vendor` folder. Just exec `gulp vendor` command on `global` folder or generated layout folder.