# Setting-up-a-world-in-Gazebo
All the details (and unique quirks) that I found out during my Summer Internship

## Prerequisites: ##


## Adding a custom model to Gazebo: ##
### Option 1 ###
__Follow these steps first. Only go to option 2 if you can't save the Gazebo world__
1. Load up gazebo (in verbose mode you can find any errors that come up)

    `gazebo --verbose`
    
2. Go to Edit -> Model Editor (Ctrl + M)
3. Go to Custom Shapes and click add
4. Then browse for the model you want to add 

      _This will be a collada (.dae) file_
  
      __Make sure the collada file is in a folder with all the textures required__

5. Place your model in the world and save the model
6. To change the model from grey to the textures you added:
    1. Go to your file manager and go to the folder __model_editor_models__
    2. Find the folder corresponding to the model name you just saved
    3. Open the __model.sdf__
    4. Delete this seciton of code:
    
     ```
        <material>
          <lighting>1</lighting>
          <script>
            <uri>file://media/materials/scripts/gazebo.material</uri>
            <name>Gazebo/Grey</name>
          </script>
          <shader type='pixel'/>
        </material>
    ```
7. Delete the model from your world
8. Insert the model (from the insert tab)
9. Repeat these steps until you have created your desired world 
10. To save the world, go to File -> Save World As (Ctrl + shift + s)

### Option 2 ###
__If you encounter an issue where you can't save your gazebo world, follow these steps__
1. Load up Gazebo using sudo

        `sudo gazebo`
        
2. Follow steps 2 - 5 in __Option 1__
3. To change the model from grey to the textures you added:
    1. Open a new terminal and type:

    `sudo nautilus`
    
    2. Find the folder corresponding to the model name you just saved
    3. Open the __model.sdf__
    4. Delete this seciton of code:
    
     ```
        <material>
          <lighting>1</lighting>
          <script>
            <uri>file://media/materials/scripts/gazebo.material</uri>
            <name>Gazebo/Grey</name>
          </script>
          <shader type='pixel'/>
        </material>
    ```
4. Delete the model from your world
5. Insert the model (from the insert tab)
6. Repeat these steps until you have created your desired world 
7. To save the world, go to File -> Save World As (Ctrl + shift + s)
   
   
## How to launch the world ##


    
 
    
