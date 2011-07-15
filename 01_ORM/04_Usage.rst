=====
Usage
=====

The ORM is really designed to be simple to use, the following example should show you most of what you need to know.

::

	$user = new User(5); // loads user 5

	$post = new Post();
	$post->content = "My new post";
	$post->author = $user;
	if( !$post->save() ){
		// $post does not validate constraints
	}
	
	echo $post->content;
	
	$user->delete(); // will delete also all the posts if cascade is set to true
