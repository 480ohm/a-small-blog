# A Small Blog
A small, flat-file, CMS (I suppose) written in Python.

## Outline
This is a rough outline of how I, rightly or wrongly, think the app will function. It is based on a lot of assumptions and will probably get re-written a LOT but I've got to start somewhere, right?! I have deliberately not looked at other blog platforms beause I want to make my own mistakes and learn and possibly some up with a better way of doing something (or not).

### The Not-Very-Granular Picture
* Write stuff
* Put it in a directory
* Run a command
* Things happen
* A blog post is created

### Notes
Ideally, this should be able to be run on the server. It shouldn't matter where the content is created as long as it is valid and put in the correct directory and the correct command is run.

The command is possibly something like:
  asb /path/to/blog/
  
This could work with multiple blogs/sites/whatever as it would only search the directory it's pointed at for whatever the temp post directory will be called, the directory holding published posts and the index.html page (plus whatever else is necessary but it's not going to check for directory structure everytime it's run...right?)

When the command is run, the relevant directory is scanned, posts are processed in order of time added to the directory (if possible, how else if not?), templates are applied, links added.

How are images going to be handled?

A very rough directory structure would be something like:
* posts -> where the posts are stored after being processed
* ??? -> where .md files are placed before processing
* .md_archive -> an archive of .md files before processing (just in case)
* .asbrc -> site settings: title, description, author name, etc.
* templates -> templates for the different post types

#### Templates
Templates are for the different types of posts possible. Current thoughts are:
* post
* image -> do i need this?
* link -> do i need this?
* landing -> although this might be a special type of page rather than a template? or is that the same thing? it's late and i'm cold, i'll work that out later.
Are templates more just re-stylings rather than different post types?

How am I going to handle the look? Will it be themable? Can the content be easily re-styled? Yes, I think so...

### The More Granular Picture
* Write things in Markdown and save as .md (is something else better?)
* Copy to <come up with good name> directory
* Run a command <format? allow switches? if so for what functionality?>
  * ...the command does what?
  * ...still doing things, what are they?
* A blog post is created with the file name of (roughly at this stage of thing) yyyy-mm-dd-title-of-post.html (alt is /yyyy/mm/dd/post-name.html or yyyy-mm-dd/post-name.html
* index.html is updated in some manner
  
  ### The Granular Picture
  * ...
