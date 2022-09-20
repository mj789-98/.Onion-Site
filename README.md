# .Onion-Site
Self host your own .onion site on the dark web using the power of linux.

Open terminal


First update your repositories using 'sudo apt update' //If using debian based linux. Use dnf instead of apt if using fedora.

install tor using 'sudo apt install tor'

Use command "sudo nano /etc/tor/torrc"

Look for #Hidden service directory
         #Hidden service port 
         
Now remove # from both the lines

first line of code will store the .onion address
second line will expose the site to the dark web

Now write the following command in the terminal one by one -

sudo service tor stop

sudo service tor start

sudo service tor status

sudo cat /var/lib/tor/hidden_service/hostname

After executing the following commands you will have the address of the site. Copy the address and store it in wordpad or any doc file.


Now run the following commands one by one -

sudo apt install nginx

sudo service nginx start                                // This will install nginx and will show active running status.

sudo service nginx status

sudo nano /etc/nginx/nginx.conf

After executing following commands you will see config editor will open

In the editor uncomment or remove # from -

1) server_tokens off; 2) server_name_in_redirect off;

Under 1) server_tokens off - Write following command - port_in_redirect off;


Now restart the nginx server - sudo service nginx restart



Now go to following folder - cd /var/www

use 'ls' command to see the files

You will find a html file

Now cd to html using 'cd html'

usse 'ls' again to see the contents of html 

You will see  "index.nginx-debian.html" and "index.html" files there or any one of them.

You have to delete both the files using - "sudo rm index.nginx-debian.html" and "sudo rm index.html"

Now create a new html files using - "sudo nano index.html"  // nano is the text editor we are using.

Write the html code according to how you want your site to be looked, Or use a boiler plate.

You can save the file using Ctrl+x and then press 'y' and enter.


Now restart the enginx server using - sudo service nginx restart

Now use the text you copied to the notepad earlier in the process. Reload the page if you are already on the site.




                                           !!!!! CONGRATS !!!!!! You not just created a website on the daark web but also self-hosted it on your own pc.
                                           Now you are exposed to the dark web.



