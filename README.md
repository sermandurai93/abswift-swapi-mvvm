
# SWAPI MVVM

Example of architecture MVVM-FC (flow controllers) in iOS project based on Star Wars API. Flow controllers are alternative for coordinators.

## Universal structure of folders

* [Library/](Library/) - custom libraries and local extensions which can be reused in whole app. This code cannot use sources from other folders in this project. So it must contain very generic functionality which can be reused in any other project.
    * [ApiSession/](Library/ApiSession/) - library which delivers easy in use interface to make network requests with custom retry count, timeouts and settings for thread and decoding of response.  
* [SwapiMVVM/](SwapiMVVM/) - source code of our application with MVVM modules and business logic.
    * [Modules/](SwapiMVVM/Modules/) - MVVM modules. Most of modules consist of view model, view controller, flow controller and factory. There can be also custom views or data structures.
    * [Resources/](SwapiMVVM/Resources/) - assets and localized strings.
    * [Services/](SwapiMVVM/Services/) - services which can be used in view models.
        * [SwapiService/](SwapiMVVM/Services/SwapiService/) - implemented specification of SWAPI using `ApiSession` class. It delivers request methods and decoded responses.
