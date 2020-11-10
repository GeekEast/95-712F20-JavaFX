### Table of Content
- How to setup JavaFX in Java 8 using Intellij?
- How to install Scene Builder and use it in JavaFX Application?
- What is Lambda Expression and when you need it?

### Event Categories
<p align="center"><img style="display: block; width: 600px; margin: 0 auto;" src=img/2020-11-10-19-23-53.png alt="no image found"></p>


### Questions
- Can one Java file include multiple classes?  
  - [stackoverflow](https://stackoverflow.com/questions/968347/can-a-java-file-have-more-than-one-class)
- What is the difference between an inner class and an outer class?
  - Normally, you define a class as an inner class if it is used **only** by its `outer` class.
- **How to change an inner class to anonymous inner class?**
  - `Inner Class`
    ```java
    public void start(State primaryStage){
        // Omitted

        btEnlarge.setOnAction(new EnlargeHandler());
    }

    class EnlargeHandler implements EventHandler<ActionEvent> {
        public void handle(ActionEvent e) {
            circlePane.enlarge();
        }
    }
    ```
  - `Anonymous Inner Class`
    ```java
    public void start(State primaryStage){
        // Omitted
        btEnlarge.setOnAction(new EventHandler<ActionEvent>(){
            public void handle(ActionEvent e) {
                circlePane.enlarge();
            }
        });
    }
    ```
  - `Lambda Expression`
    ```java
    public void start(State primaryStage){
        // Omitted
        btEnlarge.setOnAction(e -> {
            circlePane.enlarge();
        });
    }
    ```
  - Do you see the **significant** difference?
- **Summary**:
  - inner vs outer: `only once`
  - lamda vs anonymous vs inner: `Simplicity`
- Why you need `Scene Builder`?
  - Because you can remember anything but not everything.
  - Because it separate the views from controllers -> heard of MCV framework?
  - Let's talk about a bit of MCV and recomment some videos for you to review and learn.

### JavaFX
- Intellij IDEA support integration with JavaFX Scene Builder.
- JavaFX is not built-in in JDK 11.


### Frequent Used UI
<p align="center"><img style="display: block; width: 600px; margin: 0 auto;" src=img/2020-11-10-18-38-27.png alt="no image found"></p>

### Reference
- [JavaFX comes with JDk8?](https://stackoverflow.com/questions/35974003/javafx-comes-with-jdk-8)
- [JavaFx Project in Intellij IDEA using Scene Builder](https://www.youtube.com/watch?v=T3NlWMzPyXM)
- [Configure JavaFX Scene Builder](https://www.jetbrains.com/help/idea/opening-fxml-files-in-javafx-scene-builder.html)
- [Text Book Code Examples](https://media.pearsoncmg.com/ph/esm/ecs_liang_ijp_12/cw/content/ExampleByChapters.html)