# Changes-the-directory-root-for-the-main-domain-to-public_html-subfolder
Changes the directory root for the main domain to public_html/subfolder



Changes the directory root for the main domain to public_html/subfolder

RewriteEngine on
RewriteCond %{HTTP_HOST} ^(www.)?example.com$
RewriteCond %{REQUEST_URI} !^/subfolder/
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ /subfolder/$1
RewriteCond %{HTTP_HOST} ^(www.)?example.com$
RewriteRule ^(/)?$ subfolder/index.php [L]

NOTE: The .htaccess file should be located in the directory root of the domain you wish to configure certain rules for.
