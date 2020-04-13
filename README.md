# Go app skeleton

```
your-application-name
├── cmd
|   ├── your-application-name-cli
|   |    └── main.go
|   ├── your-application-name-api
|   |    └── main.go
├── internal/
|   ├── package01
|   |    ├── file01.go
|   |    └── file02.go
|   ├── package02
|   |    ├── file01.go
|   |    └── file02.go
├── pkg/
|   ├── library01
|   |    ├── file01.go
|   |    └── file02.go
|   ├── library02
|   |    ├── file01.go
|   |    └── file02.go
├── vendor/
├── LICENSE
└── README.md
```


Folder structure description:


```
/cmd
```
Every path to access to the app.
Such us, API, CLI, etc..
Each of them inside the folder ```cmd```will contain their ```main.go``` and all the rest of the files, configuration, environments, depency inyection, etc...
Important, the name of the packages inside the cmd will have reference to the binary.

```
/internal
```
Will serve all the components of their app that won't be exposed.

```
/pkg
```
Folder which will have all the package that we want to expose and they will have reutilization in the future.

```
/vendor
```
(Optional), folder which will have all the third party dependencies, in the case that you don't have migrate to Go Modules yet.
