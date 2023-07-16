### Design Principles vs Design Patterns :
Design Principles sont des directives générales pour guider la conception logicielle, tandis que les design patterns sont des solutions spécifiques et réutilisables pour des problèmes de conception courants. Les principes de conception fournissent une base solide pour concevoir des systèmes de haute qualité, tandis que les design patterns offrent des approches concrètes pour appliquer ces principes dans des situations spécifiques.
Ce sont des solutions aux problèmes du monde réel qui surgissent à maintes reprises, sont des solutions aux problèmes généraux rencontrés par les développeurs de logiciels lors du développement de logiciels. Ces solutions ont été obtenues par essais et erreurs par de nombreux développeurs de logiciels sur une période assez longue. donc au lieu de réinventer la roue, nous suivons les modèles de conception qui ont fait leurs preuves, testés par d'autres et sûrs à suivre.

**Examples:**
- Encapsulate what varies.
- Program to interfaces, not to implementations.
- Depend upon abstractions. Do not depend upon concrete classes. 

**Examples:**
- Singleton Pattern ( One class can only have one instance at a time ).
- Adapter Pattern ( Match interface of different classes ).

---------------------------------------------------------------------- Design Principles ------------------------------------------------

### SOLID : 
##### Principe de responsabilité unique (SRP - Single Responsibility Principle) :
Une classe ne devrait avoir qu'une seule raison de changer. Cela signifie qu'une classe ne doit être responsable que d'une seule tâche ou d'un seul aspect du système. Par exemple, une classe "Utilisateur" ne devrait être responsable que de la gestion des données de l'utilisateur, et non de l'envoi d'e-mails ou de la génération de rapports.

##### Principe d'ouverture/fermeture (OCP - Open/Closed Principle) : 
Les entités logicielles (classes, modules, etc.) doivent être ouvertes à l'extension mais fermées à la modification. Cela signifie qu'il faut pouvoir ajouter de nouvelles fonctionnalités en étendant le code existant plutôt qu'en le modifiant directement. Par exemple, au lieu de modifier une classe "Calculatrice" existante pour ajouter une nouvelle opération, on peut créer une nouvelle classe dérivée de "Calculatrice" pour cette opération spécifique.
En gros : use inheritance to modify(override) methods and avoid modifying base class.

##### Principe de substitution de Liskov (LSP - Liskov Substitution Principle) : 
Les objets d'une classe dérivée doivent pouvoir être utilisés en remplacement des objets de la classe de base sans altérer le fonctionnement du programme. Cela garantit une utilisation cohérente des classes dérivées et facilite la polymorphie. Par exemple, si une classe "Animal" a une méthode "manger()", toutes les classes dérivées comme "Chien" ou "Chat" doivent pouvoir être utilisées sans problème dans un contexte où "Animal" est attendu.

##### Principe de ségrégation des interfaces (ISP - Interface Segregation Principle) : 
Les clients ne doivent pas être forcés de dépendre d'interfaces dont ils n'ont pas besoin. Les interfaces doivent être spécifiques aux besoins des clients qui les utilisent. Cela évite les dépendances inutiles et garantit un couplage faible. Par exemple, au lieu d'avoir une seule interface "IModule" avec de nombreuses méthodes, on peut définir des interfaces spécifiques à chaque aspect du module, telles que "IModuleA" et "IModuleB".

**--- Interface Pollution : ---**
- Large interface(that's bad).
- Classes have empty methods implementation.
- Method implementations return null/default/dummy values.
- Use a lot of unsupportedOperationException.

##### Principe d'inversion de dépendance (DIP - Dependency Inversion Principle) : 
Les modules de haut niveau ne doivent pas dépendre de détails d'implémentation, mais plutôt d'abstractions. Cela signifie que les dépendances entre les classes doivent être basées sur des interfaces ou des classes abstraites plutôt que sur des classes concrètes. Par exemple, une classe "ServiceClient" ne doit pas dépendre directement d'une classe "HttpClient", mais plutôt d'une interface "IHttpClient" qui peut être implémentée par différentes classes.

> “High-level modules should not depend on low-level modules, both should depend on abstractions.”
“Abstractions should not depend on details. Details should depend upon abstractions.”

A high-level module is a module (class) that uses other modules (classes) to perform a task. 
A low-level module contains a detailed implementation of some specific task that can be used by other modules.  
