Creating a project
------------------

Downloading Kinaf
=================

Starting a project with Kinaf is pretty simple. 

first of all create a directory and download Kinaf into a directory, you can name it whatever you want but by convention you can name it Kinaf.

::

    mkdir myProject
    cd myProject
    git clone git://github.com/djpate/Kinaf.git
    php Kinaf/bin/kinaf init

You should now have this structure :

::

	├── configuration
	├── Kinaf
	│   ├── bin
	│   │   ├── base_file
	│   │   └── scripts
	│   │       └── templates
	│   │           └── Class
	│   ├── classes
	│   │   └── kinaf
	│   │       └── orm
	│   └── libs
	│       ├── Twig
	│       │   ├── Error
	│       │   ├── Extension
	│       │   ├── Filter
	│       │   ├── Function
	│       │   ├── Loader
	│       │   ├── Node
	│       │   │   └── Expression
	│       │   │       ├── Binary
	│       │   │       └── Unary
	│       │   ├── NodeVisitor
	│       │   ├── Sandbox
	│       │   ├── Test
	│       │   └── TokenParser
	│       └── yaml
	├── layout
	│   └── default
	├── namespace
	├── orm
	├── public
	├── routing
	└── views


