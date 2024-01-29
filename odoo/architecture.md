# Architecture Overview

## Multitier application

Odoo follows a multitier architecture, meaning that the presentation, the business logic and the data storage are separated. More specifically, it uses a three-tier architecture.

- The presentation tier is a combination of HTML5, JavaScript and CSS. 
- The logic tier is exclusively written in Python
- The data tier only supports PostgreSQL as an RDBMS.

## Odoo modules
Both server and client extensions are packaged as modules which are optionally loaded in a database. A module is a collection of functions and data that target a single purpose.
Everything in Odoo starts and ends with modules.
Modules may also be referred to as addons and the directories where the Odoo server finds them form the addons_path.

## Composition of a module

An Odoo module can contain a number of elements:

- Business objects :
 A business object (e.g. an invoice) is declared as a Python class. The fields defined in these classes are automatically mapped to database columns thanks to the ORM layer.

- Object views :
Define UI display

- Data files :
    - XML or CSV files declaring the model data:

    - views or reports,

    - configuration data (modules parametrization, security rules),

    - demonstration data

- Web controllers : 
Handle requests from web browsers

- Static web data: 
Images, CSS or JavaScript files used by the web interface or website

None of these elements are mandatory. Some modules may only add data files (e.g. country-specific accounting configuration), while others may only add business objects. 

## Module structure

Each module is a directory within a module directory. Module directories are specified by using the --addons-path option.

An Odoo module is declared by its manifest.

When an Odoo module includes business objects (i.e. Python files), they are organized as a Python package with a __init__.py file. This file contains import instructions for various Python files in the module.