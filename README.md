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
