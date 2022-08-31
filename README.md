# Setting-up-a-world-in-Gazebo
All the details (and unique quirks) that I found out during my Summer Internship



## Adding a custom model to Gazebo (option 1): ##
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
    2. Open the __model.sdf__
    3. Delete this seciton of code:
    
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


