==========================
Mapping objects with Kinaf
==========================

In Kinaf, all the orm related files are in the orm directory in the root of the project.

An object mapped with Kinaf is called an "Entity", In order to create an Entity you'll have to create two files

First the mapping file in the /orm directory and the class file in the /namespace/entities directory.

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
      class: user
      
**/namespace/entities/comment.class.php**
::
    
    <?php
    
		namespace entities;
    
        use \kinaf\orm\model;
        
        class Comment extends model{
      
        }
        
    ?>

notice that the filename is lowercase, this is needed by the bug in the php autoloading feature.
