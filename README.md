# CUBA Petclinic

<p align="center">
  <img src="https://github.com/cuba-platform/cuba-petclinic/blob/master/img/petclinic_logo_with_slogan.svg"/>
</p>


CUBA Petclinic is a CUBA platform example application dealing with the domain of a petclinic. It is based on the commonly known [Spring Petclinic](https://github.com/spring-projects/spring-petclinic) example.

The CUBA Petclinic application deals with the domain of a Pet clinic and the associated business workflows to manage a pet clinic.


## Customizations

![Customizations](img/screenshots/customizations.gif)

### Column Selection always visible

```scss
.v-table .v-table-column-selector:not(.v-disabled) {
color: var(--primary-color-shade-2);
border-color: var(--primary-color-shade-2);
background: transparent;
opacity: 1;
filter: none;
}
```

### Popup Width for Lookup Field

```java
package com.haulmont.sample.petclinic.web.pet.pet;

public class PetBrowse extends StandardLookup<Pet> {
    
    @Inject
    protected LookupField<PetType> typeFilterField;


    @Subscribe
    public void onBeforeShow(BeforeShowEvent event) {
        typeFilterField.setPopupWidth("400px");
    }
}
```
more information: https://doc.cuba-platform.com/manual-latest/gui_LookupField.html#gui_LookupField_PopupWidth

