# Local Setup

### Training Requirements

* macOS 10.14 or higher.  Windows 10 Pro
* A text/code editor.  We recommend [Microsoft Visual Studio Code](https://code.visualstudio.com/download) which works on macOS and Windows.
* A Command Line Interface \(CLI\) tool.  On macOS use [Terminal](https://www.youtube.com/watch?v=Jm8-UFf8IMg), and on Windows use [PowerShell](https://www.youtube.com/watch?v=VFuobJbbDtU)
* Windows users may need PHP installed.  You could use [WampServer](https://www.youtube.com/watch?v=D_Fhu_6RuMw).  You also need to setup your environment variables after installing PHP.  [This video shows](https://www.youtube.com/watch?v=aheaqzw8ih8) this if using Wampserver.
* Basic familiarity with [running commands on a CLI ](https://www.hongkiat.com/blog/web-designers-essential-command-lines/)is useful
* Basic understanding of HTML and CSS is required

### Front-End tooling installation

1. Install **NVM** \([macOS](https://medium.com/@jamesauble/install-nvm-on-mac-with-brew-adb921fb92cc) or [Windows 10](https://www.youtube.com/watch?v=px9N1JOzRVU)\)
2. Install the latest LTS versions of [NodeJS with NPM](https://nodejs.org/en/).  It is recommended you install NodeJS with [NVM](https://tecadmin.net/install-nodejs-with-nvm/).

### **Drupal 8**

Use one of the options below to install Drupal 8.  Install the [latest Drupal 8 ](https://www.drupal.org/project/drupal/)release.

* [Acquia Dev Desktop](https://docs.acquia.com/dev-desktop/install/)
* You could also use [Lando](https://docs.lando.dev/basics/installation.html), [DDev](https://ddev.readthedocs.io/en/stable/#installation), [Docksal](https://docksal.io/installation), or [Vagrant](https://www.vagrantup.com/intro/getting-started/install.html)

### Drupal Modules

Regardless of which option you use to setup Drupal 8, the following modules need to be installed and enabled:

* [Components Libraries](https://www.drupal.org/project/components)
* [Paragraphs](https://www.drupal.org/project/paragraphs)
* [Entity Reference Revisions](https://www.drupal.org/project/entity_reference_revisions)
* [Devel & Kint](https://www.drupal.org/project/devel) \(both in same module\)
* [Admin toolbar and Admin toolbar Extras](https://www.drupal.org/project/admin_toolbar)
* [Twig Field Value](https://www.drupal.org/project/twig_field_value)
* [Focal Point](https://www.drupal.org/project/focal_point)
* [Crop API](https://www.drupal.org/project/crop)
* [Views Reference Field](https://www.drupal.org/project/viewsreference)
* Responsive Images \(core\)
* Media & Media Library \(both on core\)

### New Drupal 8 theme with Theme Generator

Please create a new Drupal 8 theme using [Mediacurrent's Theme Generator.](https://mariohernandez.io/blog/mediacurrent-theme-generator)

1. Create a new folder inside your /themes folder in your drupal project called `training_theme` \(`/themes/training_theme` or `/themes/custom/training_theme`\)
2. In your command line tool, navigate into the new folder \(**training\_theme**\)
3. Run `nvm install node && node -v > .nvmrc`.  In Windows you may need to run these commands separately \(i.e. `nvm install node`, then `node -v > .nvmrc`\)
4. Run `npm create yo mc-d8-theme` \(don't change this command\).  Respond to the on-screen prompts as follows:

   1. Accept the default for human readable name for your theme by pressing Return \(Training Theme\)
   2. The theme's machine name MUST be `training_theme`.  If you changed the human readable name above, be sure the machine name remains **training\_theme** \(it shoud always march your directory name\).
   3. Type a description for your theme
   4. Select **Stable** as your base theme
   5. Select **Y** to ignore the **/dist** directory in `.gitignore`
   6. Select the **Drupal tabs** and **Drupal messages** components
   7. After the theme has been created, run `npm run build`
   8. Then run `npm run watch`
   9. Open Pattern Lab using the provided URL at the end of the last command \(\`http://localhost:3000\)

   You are all set! 🙌

