
# Go modules sample project

## Instructions

### Init new module
```
go mod init <MODULE_PATH>/<MODULE_NAME>
```

### List dependencies
* View final versions that will be used in a build for all direct and indirect dependencies
	```
	go list -m all
	```
* View available minor and patch upgrades for all direct and indirect dependencies
	```
	go list -u -m all
	```
* View specific dependencies
	```
	go list -m <DEPENDENCY_PATH>/<PARTIAL_DEPENDENCY_NAME>
	```

### Show documentation
```
go doc <DEPENDENCY>
	e.g.
	go doc rsc.io/quote/v3
```

### Update all 
Update all direct and indirect dependencies to latest minor or patch upgrades
```
go get -u
```

### Upgrade single dependency
```
go get <DEPENDENCY>
	e.g.
	go get golang.org/x/text
```

### Include single dependency specific version
```
go get <DEPENDENCY>@<VERSION>
	e.g.
	go get rsc.io/sampler@v1.3.1
```

### Tidy dependencies
Prune any no-longer-needed dependencies from go.mod and add any dependencies needed for other combinations of OS, architecture, and build tags
```
go mod tidy
```

### `OPTIONAL` Go vendor
Create a vendor directory
```
go mod vendor
```

---

## Links
* https://blog.golang.org/using-go-modules
* https://github.com/golang/go/wiki/Modules
