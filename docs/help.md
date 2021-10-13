# Informations

## 23/09

**In IPVS** 

[*] creation of agents module

```
ng g m modules/agents --routing 
```

[*] creation of agents component
src https://stackoverflow.com/questions/40649799/create-component-add-it-to-a-specific-module-with-angular-cli 
```
ng g c agents --module agentsComp
```

[*] creation of agents-list component (in agents/component)

```
ng g c agents-list
```

## Organisation

* Create the module

* Create the differents components (made the model if necessary)

* Create the service

* Add the route in router

* Create the tab in the header component

### Add the route

app-routing.modules.ts in the application

### Add the tab

```
shared > components > header 
```
## Erros

### Module not find

restart with
```
ng serve 
```
src : https://stackoverflow.com/questions/39932969/angular2-lazy-loading-module-error-cannot-find-module