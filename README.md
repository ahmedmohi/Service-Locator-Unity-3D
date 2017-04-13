# Service-Locator-Unity-3D
Implementation of service locator game design pattern in unity 3D

Usage :
    Just add the script anywhere in your project and to use.

    Whenever you need reference to another script just call

        ServiceLocator.GetService<ClassName>();


There's a couple of notes :

    If the gameobject isn't found i create new one by default , but you can just do that 
LevelManager level =  ServiceLocator.GetService<LevelManager>(false); 
or change the default value in the script

    if there is no gameobject with script required and won't create new one it throw exception , you can handle it differently if you want. 

    This script will return the first occurance of gameobject so you will mainly use it with your main scripts or manager scripts.
But what if you want to find any script or another words you will define what scripts the service locator will look for.
you can easily add a method that adds to the dictionary type and reference so you any script that you will need to find can at start at it self to the serivce locator .



