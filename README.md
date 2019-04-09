# arcgis-java-maven-starter-project
Starter project for the ArcGIS Runtime SDK for Java with Maven.

The project includes the Maven wrapper, so there is no need to install Maven to run the app.

The app launches a window displaying a map.

![screenshot](screenshot.png)

### IntelliJ IDEA

1. Open IntelliJ IDEA and select _File > Open..._.
2. Choose the arcgis-java-maven-starter-project directory and click _OK_.
3. Select _File > Project Structure..._ and ensure that the Project SDK and language level are set to use Java 11.
4. Open the Maven view with _View > Tool Windows > Maven_.
5. In the Maven view, under _Plugins > arcgis-java_, double-click `arcgis-java:arcgis` to run the `arcgis` Maven goal. This will cause the ArcGIS Runtime SDK Maven plugin to download the native libraries.
6. In the Maven view, run the `compile` phase under _Lifecycle_ and then the `exec:java` goal to run the app.

### Eclipse

1. Open Eclipse and select _File > Import_.
2. In the import wizard, choose _Maven > Existing Maven Projects_, then click _Next_.
3. Select the arcgis-java-maven-starter-project as the project root directory.
4. Click _Finish_ to complete the import.
5. Right-click the project in the Project Explorer or Package Explorer and choose _Run As > Maven Build..._. In the _Edit Configuration_ dialog, create a new configuration with name `arcgis`. In the _Goals_ field, enter `arcgis-java:arcgis`. Click _Run_ to run the goal. This will cause the ArcGIS Runtime SDK Maven plugin to download the native libraries.
6. Again, create a new run configuration with name `run`. In the _Goals_ field, enter `compile exec:java`. Click _Run_ to run the goal. The app should compile and launch the JavaFX window.

### Command Line

1. `cd` into the project's root directory.
2. Run `./mvnw clean compile` on Linux/Mac or `mvnw.cmd clean compile` on Windows once to make sure the dependencies are fetched.
3. Run `./mvnw exec:java` on Linux/Mac or `mvnw.cmd exec:java` on Windows to run the app.