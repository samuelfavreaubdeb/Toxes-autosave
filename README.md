# Toxes autosave

![Repo Logo](/src/img/toxes-autosave.png)

# What is this?

This is a TOX that can be imported inside your TouchDesigner project to ensure that all of your external toxes are exported when your project is saved.

## What problem does this solve?

When working on bigger and bigger TouchDesigner projects, it can be useful to utilise external toxes to make the project more modular. The main problem when using external toxes is that you need to contently remember to re-export your toxes, otherwise, all of your hard work will be lost. This TOX will automatically open a dialog every time the project is saved to allow you to easily export the toxes you've been working on. This way, you won't need to crawl around your project to find all of the toxes that have been modified.

# Parameters - Toxes Autosave

- ### `Active` 
    - When set to On, the external toxes will be automatically exported on save.
- ### `Alert on save` 
    - When set to On, a dialog will show up on save to allow you to select the external toxes to export.

# Operator Inputs

- ### `Input 0` 
    - (optional) A Table containing the name and relative path of all the toxes you want to keep track of. All external toxes will be checked by default.

# Features

- ### `Export Toxes dialog`
    - When the "Alert on save" parameter is activated, the "Export Toxes dialog" will appear when the project is saved. You will then be able to select the individual toxes you wish to export, or export them all. For a tox to be visible on the list, it's "Enable External .tox" parameter needs to be set to "On" and it needs to have a relative path in it's "Export .tox path" parameter.

![Export Toxes Dialog](/src/img/export-toxes.png)

- The "Show" button will allow automatically set the home view on the selected Tox.

![Show Tox](/src/img/show-operator.png)

- If you double click on the export path of a tox, you will be able to modify it. The changes made to the dialog will be mirrored on the actual Tox.

![Edit Tox Path](/src/img/edit-export-path.png)



- ### `Conflict dialog`
    - When two or more toxes with identical export paths are selected, the "Conflict dialog" will appear. With it, you will be able to export only the desired toxes, or edit the export paths in order to export them all without loosing progress.

![Edit Tox Path](/src/img/conflict.png)

- ### `Reload dialog` 
    - If you wish to reload all of your external toxes, you can press "Ctrl + r" on your keyboard and the "Reload dialog" will appear. You will then be able to select the individual toxes you wish to reload, or reload them all.

![Edit Tox Path](/src/img/reload.png)

## Requirments

TD builds > 2023.12370

## Installation.

Download the latest version from the [Release Page](https://github.com/picturesbyrobots/td-completes-me/releases). Then, place the TOX file at the root of your project. It should automatically detect your external toxes.

## Tested On

PC.

## Release Notes

### 0.1.0

Initial release.

**Enjoy!**
