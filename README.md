Virtual-Host
============

Configuracion de virtual Host

1. sudo cp /etc/apache2/sites-available/default /etc/apache2/sites-available/local.proyecto1.com
2. sudo gedit /etc/apache2/sites-available/local.proyecto1.com
3. sudo gedit /etc/hosts
4. sudo a2ensite local.proyecto1.com
5. sudo /etc/init.d/apache2 restart

<VirtualHost *:80>
  ServerName local.alice.com
  DirectoryIndex app.php
  DocumentRoot /home/joebuntu/NetBeansProjects/alice/web
  <Directory /home/joebuntu/NetBeansProjects/alice/web>
      Options Indexes FollowSymLinks MultiViews
      AllowOverride All
      allow from all
  </Directory>
</VirtualHost>
