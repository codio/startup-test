# Startup Test
This project should be used as a quick run through after a system upgrade. 

At this point it is very basic, but please feel free to modify this over time to inlude anything that helps us ensure that everything is working properly.

##General

- Import the repo using Create Project
- Open a Terminal Window
- Type `parts search` and check output

##PHP
As we have a quite a few PHP users, the project includes a simple `index.php` that can be run by pressing the 'Box URL' menu item.

I have configured a `startup.sh` file that ensures that Box Parts are all working. It start Apache2 but only if Apache2 has already been installed.

###If a fresh install of this project then ..
- Run `parts install apache2` 
- Run `parts start apache2`

###If fresh or a re-run
- Press 'Box URL' and make sure we don't see a 502 Gateway Error
- If there are issues, is it the `startup.sh` failing to execute or it is a broader problem with Box Parts.

##Node

- From the terminal, enter `npm install` and make sure it runs

##Claptrap

- Check the file tree and make sure it all looks ok
- Enter `mv node_modules test_modules` to check mv reflects properly in the file tree
- Enter `rm -rf test_modules` to check proper removal from the file tree

##Any other good ideas?

