# Common Issues

## During Installation

1. On Windows, when you check the python version after installation, you may get this error followed by the Windows Store opening:

	```
	$ python3 --version
	bash: python3: command not found
	```
	
	try this instead:
	
	```
	$ python --version
	Python 3.9.0
	```
	
	or
	

	```
	$ py --version
	Python 3.9.0
	```
	
	(Your version may be different, but as long as you see 'Python' followed by a number you are good to go.)
	
	If this is the case, any time the `python3` command is supposed to be called during the tutorial, substitute it for one of the working ones above.

## Tutorial Tips

1. After creating the `my-first-blog` repository on GitHub, I was supposed to push my git files to the repo.  I got this error:

	```
	error: src refspec master does not match any  
	error: failed to push some refs to 'https://github.com/john-jordan/my-first-blog.git'
	```

	I had not committed the changes I had been making in VScode. Git creates master branch only after commit to your local repo. If you just initialize repo, then there is no master.

1. When initializing your git repository, make sure you are in the same folder on your terminal and code editor.  I was in a different folder on my editor and when I typed git status on my terminal I didn’t see any of the .gitignore files that I had just created or previous files that should have been there.

1. Under the [Your First Django URL](https://tutorial.djangogirls.org/en/django_urls/#your-first-django-url) section, when creating the first URL, just copy the `Your code should now look like this:` box because the preceding paragraph with instructions is very confusing and I would guess most students would enter the information incorrectly. 

1. In the [Dynamic Data in Templates](https://tutorial.djangogirls.org/en/dynamic_data_in_templates/) section, I missed the part were they added the variable `posts` to the query set in the function.  They had a small paragraph where they mentioned it after the example but it is easy to miss.

1. After adding in my CSS files, I went to refresh the page and it didn’t show the changes.  Finally figured out I had to shut down my live server  that I had kept live then restart it in order for the changes to show up.  It doesn’t ever say shut the live server down most times, so just something to be aware of.
