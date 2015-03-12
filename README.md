# GDM-split-msgs-tutorial
Split 1 message into multiple messages graphically by using the Graphical Data Mapping editor

This tutorial demonstrates how to use a message map (also known as a graphical data map) to graphically process an XML message that contains one or more records, in the form of a list of child XML elements. It also demonstrates how to split the input message into individual messages by creating a new message from each child element. 

This Graphical Data Mapping capability in IBM Integration Bus is implemented within an application. In this application, a message flow defines the steps required to implement the message transformation and the message split logic of the solution.

An application is a container for all the resources that are required to create the solution. An application can contain IBM Integration Bus resources, such as message flows, message models, libraries, and JAR files.

The application takes as input one file with one or more records. Each record contains a list of items that a customer has bought in a store.

The message models that represent the input message and the output message are defined by XML schemas and contained in a shared library. The library is then referenced by the application.

A FileInput node is used to model the input step in the message flow. When the input node detects that a file with one or more records is available, it parses the content of the file, and sends the internal message representation to the next step in the flow. In this tutorial, an internal message is created for each sales item record in the input file.

A Mapping node is used to model a graphical data transformation step in the message flow. The mapping node has an associated message map, also known as a graphical data map.

The message map is the resource you use to define and implement the data transformation and message split requirements.

A FileOutput node is used to place any output messages in the file system.
