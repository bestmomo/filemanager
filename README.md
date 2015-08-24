## Filemanager ##

This package is to add [simogeo/Filemanager](https://github.com/simogeo/Filemanager) to Laravel 5.1 installation.

### Installation ###

Add Filemanager to your composer.json file to require Filemanager :
```
    require : {
        "laravel/framework": "5.1.*",
        "bestmomo/filemanager": "1.*"
    }
```

Update Composer :
```
    composer update
```

The next required step is to add the service provider to config/app.php :
```
    Bestmomo\Filemanager\ScafoldServiceProvider::class,
```

### Publish ###

The last required step is to publish assets in your application with :
```
    php artisan vendor:publish
```

### User model ###

For Filemanager php connector you must create at least this function in user model :

```
public function accessMediasAll()
{
    // return true for access to all medias
}
```

If you want some users access only to one folder add this function :

```
public function accessMediasFolder()
{
    // return true for access to one folder
}
```
For this function to work each user must have a "user" name in users table. A folder with this name will be created in filemanager/userfiles folder.

### Integration ###

You can now integrate Filemanager with any editor like CKEditor.




