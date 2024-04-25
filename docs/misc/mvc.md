Model-View-Controller (MVC) is a software architectural pattern commonly used in the development of user interfaces. It divides an application into three interconnected components, each with distinct responsibilities, to separate internal representations of information from the ways that information is presented to and accepted from the user.

The Model represents the data and the business logic of the application. It is responsible for managing the data, logic, and rules of the application. In an MVC application, the model directly manages the data, logic, and rules of the application, handling the retrieval, processing, and storage of data.

The View is responsible for presenting data to the user. It displays the data that is contained in the model to the user and also sends user commands (e.g., button clicks, keyboard input) to the controller. The view is typically responsible for the layout, appearance, and user interface elements.

The Controller acts as an interface between Model and View components. It receives user input and initiates a response by making calls to model objects. The controller interprets the input it receives from the view, then processes it (possibly updating the model), and returns the output display (view).

MVC is widely used in web apps, with many [[Web Development Frameworks|web frameworks]] (like [[Django]], [[ASP.NET]] MVC) implementing the MVC pattern. It is also used in desktop apps and is integral to some development environments.

