# Common Issues

## [Installation](https://tutorial.djangogirls.org/en/installation/)

1. When the installation and tutorial give instructions for the command line, start typing the part *after* the `$` or `C:\Users\Name\djangogirls>`.

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
	
	If none of the above work without opening the windows store, installing through the windows store should solve the problem, as long as the version is greater than 3.5.x
	
2. Under "Install Python", the tutorial states "If you already have version 3.4 or higher you should be fine."  However, when setting up the requirements.txt, the tutorial pins the Django version to a compatible version of 2.2.4.  Django 2.2.4 has a minimum Python requirement of [Python 3.5.x](https://pypi.org/project/Django/2.2.4/ "Django 2.2.4 Page on pypi.org").  I just happened to be pinned to a python version of 3.4.4 on Windows, so I happened to notice this discrepancy when doing the `pip install`.  

## [Tutorial](https://tutorial.djangogirls.org/en/)

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

1. If you get the error `NameError: name 'include' is not defined`, You have most likely forgotten to import the include method from `django.urls` in `urls.py`(from the [Django URLs](https://tutorial.djangogirls.org/en/django_urls/#your-first-django-url, "Django URLs") section).

1. If you get the error `name 'timezone' is not defined`, you have most likely missed importing timezone from `django.utils` in `views.py` (from the [Dynamic data in templates](https://tutorial.djangogirls.org/en/dynamic_data_in_templates/#queryset, "Dynamic data in templates") section).

1. If you get the error `name 'redirect' is not defined`, you have most likely missed importing redirect from `django.shortcuts` in `views.py` (from the [Django Forms](https://tutorial.djangogirls.org/en/django_forms/#saving-the-form, "Django Forms") section).

1. On the [Deploy!](https://tutorial.djangogirls.org/en/deploy#pushing-your-code-to-github) section students are pushing code to their repo. Github uses 'main' instead of 'master' now. Since the tutorial refers to the master branch keeping that naming convention will cause less confusion. A fix for this is when setting up the repo on Github, click the settings link just above the green Create repository button. In the box on the next page change main to master and click update. Close out the settings tab and click the green button on the previous page to finish creating the repo. 
