---
description: >-
  Atomico posee una forma de validación de tipos realmente eficiente y simple,
  la validacion de tipos opera de la siguiente forma:
---

# Value cycle as prop

### **Cycle as attribute**:&#x20;

the given value is transformed to the corresponding type, be it String, Number, Boolean, Array or Object, once transformed it is sent to the [**cycle as property**](value-cycle-as-prop.md#cycle-as-a-property).

### cycle as property:&#x20;

evaluates if the value is of the declared type:

* **If it corresponds to the type:**
  1. It is saved in props.
  2. An event is emitted (if this has been configured in the prop).
  3. It is reflected as an attribute (if this has been configured in the prop).
  4. It is sent to the update queue and subsequent rendering.
* **It does not correspond to the type**: an error is created by console with the following data:
  * **target**: Instance of the webcomponent.
  * **value**: Input value.
  * **type**: expected type.



