# DropDownList with dynamic itemTemplate for Angular

## To set the itemTemplate programmatically for dropdownlist component 

To load an itemTemplate in the dropdownlist component dynamically, we need to use createComponent to load the template as new component and assign its itemTemplate instance to dropdownlist's itemTemplate property. Please refer the below code snippet,

```
    ngAfterViewInit() {        
        let componentFactory = this.componentResolver.resolveComponentFactory(Newcomponent);
        const ref = this.viewContainerRef.createComponent(componentFactory);
        this.ddl.itemTemplate = ref.instance.itemTemplate;
    }
```

## Installing and Running Application

### Installing

To install all dependent packages, use the below command

```
npm install
```

### Run the application

To compile and run the source files, use the below command

```
npm start
```
