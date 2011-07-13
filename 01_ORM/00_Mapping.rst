==========================
Mapping objects with Kinaf
==========================

In Kinaf, all the orm related files are in the orm directory in the root of the project.

An object mapped with Kinaf is called an "Entity", In order to create an Entity you'll have to create two files

First the mapping file in the /orm directory and the class file in the /namespace/entity directory.

Here is an example for an entity called "Comment"

**/orm/comment.yaml**

::
  
  fields:
    content:
      type: text
      constraints:
        required: true
    post:
      type: entity
    author:
      type: entity
      classname: user
      
**/namespace/entity/comment.class.php**
::
    
    <?php
        use \kinaf\orm\model;
        
        class Comment extends model{
      
        }
        
    ?>

notice that the class name is lowercase, this is needed by the bug in the php autoloading feature.

===========
Fields type
===========

===========
Constraints
===========

=====
Usage
=====

=======
Hacking
=======

