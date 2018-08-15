Extending and Customizing the website
=====================================
The IPBES website is based on DKAN, a `Drupal
Distribution <https://drupal.org/documentation/build/distributions>`_. Additional modules have been added to extend functionality. Modules are added from contributed modules available from the Drupal Community `contrib  modules <https://www.drupal.org/project/project_module>`_ from the Drupal community. 

DKAN consists of of a distribution profile which manages the initial installation, 3rd party libraries and drupal modules, and DKAN specific modules. Below is a simplified version of where the DKAN code sits within the code::

   profiles/
       dkan/
         libraries/ (3rd party libraries)
         modules/
            dkan/ (dkan modules)
            contrib/ (3rd party module dependencies)
         themes/ (dkan themes)

The modules and themes should not be updated or changed within the DKAN folder. All customisations, updates and patches need to be done within sites/all/.. directory::

   sites/
      all/
         libraries/ (your libraries)
         modules/ (your modules)
            contrib/ (modules from Drupal)
            custom/ (custom modules)
         themes/ (your themes)

Modules
-------
Themes
------
Themes are responsible for the appearance of the site. The theme used is based on Radix which comes packaged with DKAN. Customisations have been done and a new theme (ipbes_new) has been built. The theme uses Gulp_ to compile Sass and check for errors in CSS. Gulp needs Node. This approach minifies the code to make it load fast while simplifying maintenance.

Installation of theme
~~~~~~~~~~~~~~~~~~~~~~

1) Make sure you have Node and npm installed.
You can read a guide on how to install node here: https://docs.npmjs.com/getting-started/installing-node
If you prefer to use Yarn_ instead of npm, install Yarn by following the guide here: https://yarnpkg.com/docs/install.

2) Install bower::

    npm install -g bower

3) Clone the git repository for the webstyles to be next to your project folder::

    git clone https://github.com/ipbes/webstyles.git
    
4) Go to the root of `ipbes_new` theme and run the following commands::

    npm run setup

    To install using Yarn, run::

    yarn install && bower install

5) Configure the destination folder. This is only the source code for the theme and the generated assets need to be
copied to the panthoen repository in the `sites/all/themes` folder::

    export DIST=<pantheon_repo>/sites/all/themes

6) Run gulp to copy the minified styles to the project directory::

    gulp dist
    
    
.. _Gulp: http://gulpjs.com
.. _Yarn: https://yarnpkg.com
