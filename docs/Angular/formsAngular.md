# Forms

## Driven form

allow to use the ngModel directive to bind one variable (like a model).

Example :

```
@NgModule ({
imports:[
// ...
FormModule
]
})
export class AppModule { }
```

and in FormModule :

```
[(ngModel)]="person.firstName"
```

## Reactive forms

```
@NgModule({
imports: [
// ...
ReactiveFormsModule,
],
})
export class AppModule { }
```

in .ts :

```
profileForm: FormGroup = this.fb.group({
firstName: [’’, Validators.compose([Validators.required])],
lastName: [’’, Validators.compose([Validators.required])],
});

constructor(private fb: FormBuilder) {
}
```

in .html  :

```
<form [formGroup]="profileForm" (submit)="submit()">
<label>
First Name : <input [formControlName]="’firstName’" />
</label>
<label>
Last Name : <input [formControlName]="’lastName’" />
</label>

<button type="submit" [disabled]="!profileForm.valid">Submit</button>
</form>
```

### advantages

* facility to maintain
*  immuables objects
* return or cancel easy to put in place

## Links
[Reactive and Driven forms](https://www.axopen.com/blog/2020/11/formulaires-angular-reactive-form-driven-form/)
[Differents forms](https://guide-angular.wishtack.io/angular/formulaires/reactive-forms/la-boite-a-outils-des-reactive-forms)