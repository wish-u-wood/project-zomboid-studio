![Banner](https://github.com/Konijima/project-zomboid-studio/blob/master/.images/pzstudio-banner.png?raw=true)

[![npm version](https://badge.fury.io/js/pzstudio.svg)](https://badge.fury.io/js/pzstudio)

This is an intuitive and efficient solution to create and maintain LUA mods for Project Zomboid with greater ease. The tool allows for effortless structuring of mods, reducing time and complexity typically associated with mod creation. Key features include the ability to 'Build' and 'Watch' for changes, enhancing workflow and enabling dynamic mod adjustments.

For seamless coding and guidance, we leverage the [asledgehammer/Candle](https://github.com/asledgehammer/Candle) library, offering intelligent code completion (IntelliSense) for LUA.

Start creating more powerful and versatile mods for Project Zomboid today!

<br>

## VSCode Extentions:
- [Lua](https://marketplace.visualstudio.com/items?itemName=sumneko.lua) - The Lua language server provides various language features for Lua to make development easier and faster. With around half a million installs on Visual Studio Code, it is the most popular extension for Lua language support. 
- [EmmyLua](https://marketplace.visualstudio.com/items?itemName=tangzx.emmylua) - Add EmmyLua to your VSCode.
- [ZedScript](https://marketplace.visualstudio.com/items?itemName=asledgehammer.zedscript-vscode) - A third-party VSCode extension for supporting ZedScript, a scripting format for creating Items, Recipes, etc.

<br>

## Requirements:
- [NodeJS LTS](https://nodejs.org/en) - Require NodeJS and NPM to use the CLI commands.

<br>

# Commands:

## Install
Install **Project Zomboid Studio** globally.
```bash
npm install -g pzstudio
```

## New Project
Create a new project.
> You can create a project anywhere on your computer, but **DO NOT** create it inside your Mods and Workshop directory. The build command will generate the actual mod into the Workshop directory or any output directory you set.
```bash
pzstudio new "<project-title>" "<mod-id>"
# ex1: pzstudio add "My Super Cool Mod"
# ex2: pzstudio add "My Super Cool Mod" "my-super-cool-mod"
```

## Help
Displays help information.
```bash
pzstudio help "<command>"
```

<br>

## **IMPORTANT**  
> The following commands must be executed from within a **PZStudio Project** directory.

<br>

## Update
Update **PZStudio**, **Candle** and the project.
```bash
pzstudio update
```

## Add Mod
Add an other mod to your project.
```bash
pzstudio add "<mod-name>" "<mod-id>"
# ex1: pzstudio add "My other mod"
# ex2: pzstudio add "My other mod" "my-other-mod"
```

## Rename Mod
Rename a mod from your project.
```bash
pzstudio rename "<mod-id>" "<new-mod-id>"
# ex: pzstudio rename "my-mod" "my-super-mod"
```

## Delete Mod
Delete a mod from your project.
```bash
pzstudio delete "<mod-id>"
# ex: pzstudio delete "my-mod"
```

## Add Language
Add a translation language.
```bash
pzstudio lang "<mod-id>" "<language-code>"
# ex: pzstudio lang "my-mod-1" "en"
```

## Copy Language
Copy a translation language to an other language.
```bash
pzstudio lang "<mod-id>" "<from-language-code>" "<to-language-code>"
# ex: pzstudio lang "my-mod-1" "en" "fr"
```

## OutDir
Set your output directory. Default: `"<user-dir>/Zomboid/Workshop/"`
```bash
pzstudio outdir "<output-dir-path>"
# ex: pzstudio outdir "C:/Users/Konijima/Zomboid/Workshop"
```

## Clean
Clean your output directory from the current built project.
```bash
pzstudio clean
```

## Build
Build your project and update your output directory with your project.
```bash
pzstudio build
```

## Watch
Watch for changes and keep your output directory synced.
```bash
pzstudio watch
```
