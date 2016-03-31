# Customfinder
Custom static file finder for Django

This is extended version of FileSystemFinder static finder which allows you to exclude certain files or locations

To install it just copy this folder into your project as an app and include it in your INSTALLED_APPS

include it in STATICFILES_FINDERS remember to comment out 'django.contrib.staticfiles.finders.FileSystemFinder' as this one will replace it


    STATICFILES_FINDERS = [
        # 'django.contrib.staticfiles.finders.FileSystemFinder',
        'customfinder.finder.CustomFinder',



and add this extra BLACKLIST_FILES list which will include all files which should be excluded from collectstatic


    BLACKLIST_FILES = [
        'bower_components/font-awesome/scss',
        'bower_components/font-awesome/less',
        'bower_components/font-awesome/bower.json',
    ]
