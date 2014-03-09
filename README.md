# Startup Test
This project should be used as a quick run through after a system upgrade. 

At this point it is very basic, but please feel free to modify this over time to inlude anything that helps us ensure that everything is working properly.

##General

- Import the repo using Create Project
- Access the Run menu where all the following steps are configured in the .codio file
- Do a quick Project Index (static) to ensure it is working

The tests can be run manually if required. Follow these steps:

- Open a Terminal Window
- Type `parts search` and check output

##File and Folder creation

- Create a file and a folder and check that they are both successfully created


##PHP
As we have a quite a few PHP users, the project includes a simple `index.php` that can be run by pressing the 'Box URL' menu item.

I have configured a `startup.sh` file that ensures that Box Parts are all working. It start Apache2 but only if Apache2 has already been installed.

###If a fresh install of this project then ..
- Run `parts install php5`
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

##Large Projects

- Install Composer with `parts install composer`
- Install Laravel `composer create-project laravel/laravel --prefer-dist` (can take a while)
- After this, check that there is just one 'laravel' folder created and present
- Create a new folder `move`
- Drag and drop the internal contents of `laravel` (not the 'laravel' folder itself) into `moved`
- Does this all move properly? Currently, there is a long delay where nothing happens (should be fixed soon with some sort of filetree progress indicator)
- run `rm -rf move` to remove the contents. Does it get removed and is there a delay (same comments as above regarding a new progress indicator)
- test high speed editing of any file in the project. Hold keys down and ensure editing speed is good.


