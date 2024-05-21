# WordPress Template

Create a new repo using this as it's [template](https://github.com/adampatterson/wordpress-template).

Assume any git commands are relative to your new repository.

Update the `.gitignore` file with your project theme

```.gitignore
-!/wp-content/themes/change-me
+!/wp-content/themes/new-theme
```

```shell
mkdir site.test
cd site.test
git checkout git@github.com:adampatterson/wordpress-template.git .
wp core download
 wp core config --dbname=site_wordpress --dbuser=root --dbpass=root --dbhost=localhost --dbprefix=wp_ 
 wp core install --url=site.test --title=Project --admin_user=adampatterson --admin_password=top-secret-password --admin_email=hello@adampatterson.ca
```

_Note the space at the start of the commands. This will prevent the command from logging in your `history`._
