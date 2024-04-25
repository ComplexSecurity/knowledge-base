Django is a free and open-source web development framework written in Python. It is a high-level framework, with a pragmatic design that encourages fast and clean development. Django has a large collection of modules and features, allowing developers to focus on what really matters.

Django provides the ability to build websites quickly and to scale it with less effort.

In general, a project developed with Django is broken down into small applications composed of a [[Django]] package that, in return, resolves specific domains of the application.

Each of these small applications is based on the **MVT - or Model-View-Template** - pattern, the three aspects of a web application worked on by Django:

- **Model:** the model is the structure that represents the data in this application. In other words, it has a direct connection to a database. This is the abstraction layer used to manipulate, include, or exclude data. Whenever a model is created, Django provides an API (also called ORM) for this manipulation;
- **View**: the view is a Python function designed to receive a request and send a response back. This is where the data is extracted, generating a response;
- **Template:** this is the layer where the application template is produced through artifacts understood by the web browser. This is the part that concerns everything that the end user is able to view on their device.

![[mvt.png]]
