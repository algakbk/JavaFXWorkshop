JavaFXWorkshop
==============

1. What is JavaFX and why should you care?
---------------
- successor of Swing
- Swing is dead! (Zombie-mode because for the time being it will be in the SDK)
- much more features like CSS-styling, rendering using graphic chip, binding, ...

2. Let's code!
--------------

Setup your tools:
- Eclipse IDE
- JDK >1.7u9 (with jfxrt.jar)
- SceneBuilder 1.1 (2.0 is still buggy) (http://www.oracle.com/technetwork/java/javafx/downloads/index.html)

**Part 1: SceneBuilder and fxml-files**
- fxml-file = user interface declaration
- Controller = Java class that controls one fxml-file
- don't forget to set the controller in the SceneBuilder on your top component!
- fields and methods in your controller are bound to the fxml with "@FXML"

**Part 2: Properties and binding**
- Properties are a language extension - expect them to come around in the backend, too.
- extension of bean definition: 

    setMyFoo(...) {...}
    
    getMyFoo() {...}
    
    myFooProperty() {...}
    
- There is unidirectional and bidirectional binding: 

    myProperty.bind(...);
    
    myProperty.bindBidirectional(...);
    
- you can do math with properties, for example: sum.bind(amountOfApples.add(amountOfChips).add(amountOfPotatoes));
- you can listen on properties and get notified if there's a change

**Part 3: Charts - the pie chart**
- data behind chart = ObservableList. You can listen on that, too!
- because of that, you just have to change the data and the chart will be updated

**Part 4: Styling with CSS**
- either directly for one component in SceneBuilder or in the code or in a CSS (you want to have the latter!)
- behold: not all CSS tags are available in JavaFX and you have to add a "-fx" before them: 

    -fx-background-color:red
    
- just in JavaFX - CSS: dropshadow

That is what we build together:

![alt tag](awesomeFXShoppingList.png)

More tools:
- Scenic View  (http://fxexperience.com/scenic-view/)
- e(fx)clipse (http://www.eclipse.org/efxclipse/index.html)


3. Swing Interop
----------------
- JavaFX in Swing easy. Swing in JavaFX not before JDK 8 (however possible)
- replace Swing components with FX components step by step
- maybe invert life cycle by setting a controller factory in FXML loader
- because of time constraints and focus of this workshop: Let's talk about that later and specific for your project.

4. current state of JavaFX (Java 1.7)
-------------------------------------
- Ensemble (http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
- some basic components missing like date chooser
- some rough edges in the API
- huge hype with a lot of potential

5. future prospects
--------------------
- again a big leap forward in Java 1.8
- http://fxexperience.com/controlsfx/
- first two minutes of http://www.youtube.com/watch?v=a3dAteWr40k&feature=youtu.be

6. references
-------------

- Oracle http://docs.oracle.com/javafx/