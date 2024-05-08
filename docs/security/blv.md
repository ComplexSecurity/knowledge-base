Business logic vulnerabilities are security weaknesses or flaws in the design and implementation of an application that can be exploited to carry out actions unintended by the application's owner. Unlike traditional vulnerabilities, which are typically flaws in coding, business logic vulnerabilities are more about the ways an application's legitimate features can be manipulated.

These vulnerabilities exploit the expected or standard behavior of applications in unintended ways. They are often specific to the particular logic of an application and, therefore, vary widely from one application to another. Business logic vulnerabilities are usually harder to detect with automated tools since they involve understanding the intended functionality and logic of the application.

Identifying these vulnerabilities often requires a deep understanding of the application's business logic, making manual assessment and creative thinking crucial.

Some examples of Business Logic Vulnerabilities include:

1. **Authentication Bypass**: An application might allow a user to access protected resources without properly authenticating, perhaps through manipulation of URLs or direct access to a backend API.
2. [Insecure Direct Object References (IDOR) (KB)](): If an application exposes internal objects through URLs or parameters (like `www.example.com/account?id=123`), an attacker might manipulate these references to access data belonging to other users.
3. **Multi-Step Transaction Manipulations**: In applications involving multi-step transactions (like shopping carts in e-commerce sites), attackers could manipulate the process to change the order's outcome, such as altering prices or quantities after final confirmation but before payment.
4. **Business Rules Bypass**: If certain business rules are not enforced consistently across an application, it can lead to vulnerabilities. For example, an e-commerce site might limit one promotional item per user, but this rule could be bypassed by creating multiple accounts.
5. **Workflow Exploitations**: By understanding and manipulating the workflow of an application, attackers can exploit vulnerabilities. For instance, skipping steps in a workflow to achieve a goal that should not otherwise be allowed.
6. **Logic Flaws in Access Controls**: Poorly implemented access controls could allow a user with lower privileges to access or modify data meant for higher-privileged users.

