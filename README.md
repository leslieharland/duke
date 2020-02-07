# Usage

**To Run the Application**

1. Type './gradlew build'
1. In Intellij,right click on 'main/java/duke/Launcher.java' and select Run.


# What commands can I enter?

For todos | sample user command
---------------|---------------
`todo <description of task>` | todo borrow book

For events | sample user command
---------------|---------------
`event <description of task> /at <datetime>` | event project meeting /at 2020-02-12
`...` | event project meeting /at mon 6pm

For deadline | sample user command
---------------|---------------
`deadline <description of task> /by <datetime>` | event return book /by 2020-02-12
`...` | event project meeting /by mon 6pm

* Note that specifiers **/by** and **/at** are not interchangeable

  e.g. events have to use **/at**
  deadlines have to use **/by**

  
  
  
  
  
  
teps to export your project with javafx
1. Add this to your build.gradle

jar {
    exclude 'META-INF/*.SF', 'META-INF/*.DSA', 'META-INF/*.RSA', 'META-INF/*.MF'

    manifest {
        attributes 'Main-Class': 'duke.Launcher',
                'Class-Path': configurations.runtime.files.collect { "build/libs/$it.name" }.join(' ')
    }
}

Run these commands in a terminal (java -jar has to be run)
In the root project, 
1.    ./gradlew build 
2.   ./gradlew jar
3.   run java -jar duke-xxx.jar
you will receive noclassdeferr

1. Open eclipse
2. Import the project by General > projects from file system
3. Setup javafx as an external library 
Eclipse > Preferences > Build Path > Add user library external jars (using the zip attached)

4. Edit run configuration by right clicking Run As > Edit Run Configuration. Update the project and Main class to Launcher file

5. Add the user library to your project's build path. Right Click project > build path > Configure...
Add the javafx11 library u just defined to the project under classpath

Almost done
5. Right click and select export > Java > Java runnable jar
6. Select 'Package dependencies' and a location to save the jar file

Your jar file should now work on cross-platform