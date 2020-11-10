### JavaFX
- Intellij IDEA support integration with JavaFX Scene Builder.
- JavaFX is not built-in in JDK 11.

### Frequent Used UI
<p align="center"><img style="display: block; width: 600px; margin: 0 auto;" src=img/2020-11-10-18-38-27.png alt="no image found"></p>

### Inner Class
```java
public void start(Stage primaryStage) {
    btEnlarge.setOnAction(new EnlargeHandler());
}

class EnlargeHander implements EventHandler<ActionEvent> {
    public void handle(ActionEvent e) {
        circlePane.enlarge();
    }
}
```


### Reference
- [JavaFX comes with JDk8?](https://stackoverflow.com/questions/35974003/javafx-comes-with-jdk-8)
- [JavaFx Project in Intellij IDEA using Scene Builder](https://www.youtube.com/watch?v=T3NlWMzPyXM)
- [Configure JavaFX Scene Builder](https://www.jetbrains.com/help/idea/opening-fxml-files-in-javafx-scene-builder.html)
- [Build a Login Page](https://www.youtube.com/watch?v=T3NlWMzPyXM)