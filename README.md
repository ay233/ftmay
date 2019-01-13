# ftmay
A light tool to generate projects in an easy way.

# Installation
```
npm install ftmay -g
```

```

# Usage
Open your terminal and type `ftmay` or `ftmay -h` , you'll see the help infomation below:
```
  Usage: ftmay <command>


  Commands:

    add|a      Add a new template
    list|l     List all the templates
    init|i     Generate a new project
    delete|d   Delete a template

  Options:

    -h, --help     output usage information
    -V, --version  output the version number
```

> Note that if you are using `MacOS`, `sudo` was required while using commands `add` and `delete`.

# Commands
### add | a
This command would help you to add a new template to the `templates.json`, which will be used by `ftmay` to generate projects.
```
$ ftmay add

? Set the custom name of the template: my-first-template
? Owner/name of the template: jrainlau/ftmay
? Branch of the template: new
┌───────────────────┬────────────────┬────────┐
│ Template Name     │ Owner/Name     │ Branch │
├───────────────────┼────────────────┼────────┤
│ my-first-template │ jrainlau/ftmay │ new    │
└───────────────────┴────────────────┴────────┘
✔ New template has been added successfully!
```
`ftmay` use [download-git-repo](https://github.com/flipxfx/download-git-repo) to down load git repos. After answering 3 questions, you'll add a new template to `ftmay`.

### list | l
It shows you the templates list.
```
$ ftmay list

┌────────────────────┬────────────────┬────────┐
│ Template Name      │ Owner/Name     │ Branch │
├────────────────────┼────────────────┼────────┤
│ my-first-template  │ jrainlau/ftmay │ new    │
├────────────────────┼────────────────┼────────┤
│ my-second-template │ jrainlau/motto │ master │
└────────────────────┴────────────────┴────────┘
```

### init | i
After adding new templates, you could use this command to generate your own project by choosing template.
```
$ ftmay init

? Template name: my-first-template
? Project name: my-project
? Where to init the project? ../
⠹ Downloading template...

New project has been initialized successfully!
```

It's easy, right?

### delete | d
To delete a template, you could use this command:
```
$ ftmay delete

? Which template you want to delete? my-second-template
┌───────────────────┬────────────────┬────────┐
│ Template Name     │ Owner/Name     │ Branch │
├───────────────────┼────────────────┼────────┤
│ my-first-template │ jrainlau/ftmay │ new    │
└───────────────────┴────────────────┴────────┘
✔ Template has been deleted successfully
```

# Template
The most important part of ftmay is `template`. All templates' infomation were list in the `templates.json`.
A template means a project sample, which has a simple or complex file structure.

You can create your own templates repository, and push your templates in different branches. All you need to do then is to add the templates into ftmay's `templates.json`.

# License
MIT.









