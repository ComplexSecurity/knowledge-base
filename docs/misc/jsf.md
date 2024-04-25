JavaServer Faces (JSF) is a [[Java]] specification for building component-based user interfaces for web applications. It is part of the [[Java Enterprise Edition (Java EE)]] platform. Developed by Oracle Corporation, JSF provides a framework for simplifying the development of user interfaces in Java web applications.

JSF is a component-based MVC ([[Model-View-Controller (MVC)|Model-View-Controller]]) framework. It provides a set of reusable UI components that can be easily dragged and dropped in a web application. JSF supports event-driven programming. Components in a JSF page can generate events (like clicks or value changes) that are handled by server-side Java code.

JSF integrates seamlessly with other Java EE technologies, such as [[Enterprise JavaBeans (EJBs)|Enterprise JavaBeans (EJB)]] for business logic and [[Java Persistence API (JPA)]] for database operations. In JSF, managed beans are used to define Java classes that contain business logic. These beans are managed by the JSF container in terms of their creation, lifecycle, and destruction.

Facelets is a powerful templating engine used in JSF. It is the default view declaration language for defining JSF views using [[XHTML]]. JSF’s architecture allows for easy customization of existing components and creation of new components.

JSF supports [[Ajax]], enabling the creation of dynamic and rich internet applications with partial page updates. JSF provides built-in validation and data conversion features, simplifying the process of validating user input and converting it to application-specific data types.

JSF includes a navigation model to control the sequence of screen navigation in a web application. It supports internationalization for building applications in multiple languages and also provides support for accessibility standards. JSF integrates with the Expression Language (EL), allowing the page to communicate with the managed beans.