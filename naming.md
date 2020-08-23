## General (applied to all)
1. Avoid single letter names. Be descriptive with your naming.
    ```
    // bad
    function q() {
      // ...
    }

    // good
    function query() {
      // ...
    }
    ```

## Folders
1. Use **lower-case** when naming folders and use hypehn(-) as separator.
    ```
    // bad 
    laguageTranslation
    LaguageTranslation
    Laguage-Translation
    
    // good
    laguage-translation (using - as separator)
    ```
1. Use **ProperCase** (PascalCase) when naming folder for a component.
    ```
    // bad 
    Sidenav
    side-nav
    sideNav
    
    // good
    SideNav
    ```    

## Files
1. File naming pattern should be `<file-name>.<extension>`, extensions could be (js/jsx/ts/tsx).

    > Use hyphen (-) as separator in `<file-name>` part
    ```
    // bad
    sidebarMenu.ts // file name should not be in camelCase
    SIDE_MENU.ts // UpperCase name not allowed
    
    // good
    sidebar-menu.constant.ts  
    api.ts 
    ```
> NOTE: In most of the cases index.(js/jsx/ts/tsx) will be the main file in a folder.

> NOTE: If we are using CSS/SCSS modules then we will name our style files as `<file-name>.module.<extension>`, extension could be css/scss.


## Components
1. Use **ProperCase** (PascalCase) when naming component (class or function). Use the filename as the component name.
    ```
    // bad
    const inspectorHeader = ()=>{}    
    const inspector-header = ()=>{}    

    class productThumbnail extends React.Component
    class product-thumbnail extends React.Component

    
    // good
    const InspectorHeader = ()=>{}
    class ProductThumbnail extends React.Component    
    ```
1. Root components of a directory should use index.jsx as the filename and use the directory name as the component name:
    ```  
    // bad
    import Footer from './Footer/Footer';
    import Footer from './Footer/index';
    
    // good
    import Footer from './Footer';
    ```
1. Use PascalCase for React components and camelCase for their instances.
    ```
    // bad
    import reservationCard from './ReservationCard';
    const ReservationItem = <ReservationCard />;
    
    // good
    import ReservationCard from './ReservationCard';
    const reservationItem = <ReservationCard />;
    ```

## Variables
1. Use **camelCase** when naming variables for objects, functions, and instances.
    ```
    // bad
    let OBJEcttsssss = {};
    let this_is_my_object = {};
    let c = function() {}

    // good
    let thisIsMyObject = {};
    let thisIsMyFunction = function() {}
    ```

1. Use **let** instead of var for declaring variables.
    ```
      // bad 
      var myName = 'Varun Sukheja';
      
      // good
      let myName = 'Varun Sukheja';
    ```
    
1. Private variables and functions should be prefixed with underscore ( _ ).
    ```
    // bad
    private toast:ToastService  // _ not prefixed
    private loaderService:LoaderService    // service as suffix not to be used
    
    // good
    private _toast:ToastService
    ```
    > `Private` keyword is applicable only in TS. For JS only in ES2019 and above you can prefix # to make a variable private.
1.  Use suffix as **List** for variables of data type - Array, eg customReviewList
1.  Use suffix as **Set** for variables of data type - Set, eg customReviewSet
1.  Use suffix as **Map** for variables of data type - Map, eg customReviewMap

## Constants
1. User **UPPER_CASE** when naming constants and use underscore(_) as separator.
    ```
    // bad
    export const THING_TO_BE_CHANGED = 'should obviously not be uppercased';

    // bad
    export let REASSIGNABLE_VARIABLE = 'do not use let with uppercase variables';

    // ------------------------------------

    // bad
    export const apiKey = 'SOMEKEY';
        
    // good
    export const API_KEY = 'SOMEKEY';
    
    // ------------------------------------
    
    // bad - no need to uppercases objec key, only uppercase object name
    export const MAPPING = {
      KEY: 'value'
    };
    
    // good
    export const MAPPING = {
      key: 'value'
    };    
    ```

## Enums
1. Use ProperCase (PascalCase) when naming enums and all the keys should be UPPER_CASE.
    ```
    // bad
    enum myDirection {
        up,
        right,
        down,
        left
    }
    
    // good
    enum MyDirections {
        UP,
        RIGHT,
        DOWN,
        LEFT
    }
    ```
    
## Functions
1. 1. Use **camelCase** when naming functions.
    ```
    // bad
    function c() {}

    // good
    function thisIsMyFunction() {}
    ```
    
1.  Functions for handling events should be named as `on<FunctionName><EventName>`.
    ```
    // bad
    function click() {}
    function onClick() {}
    function onCancel() {}
    function whenClickedCancel() {}    
    function clickingCancel() {}    

    // good
    function onCancelClick() {}
    ```
    
## Classes
1. Use ProperCase (PascalCase) when naming classes.
    ```
    // bad
    class user {
      constructor(options) {
        this.name = options.name;
      }
    }

    const bad = new user({
      name: 'nope',
    });
    
    // good
    class User {
      constructor(options) {
        this.name = options.name;
      }
    }

    const good = new User({
      name: 'yup',
    });
   ``` 
1. Use UPPER_CASE naming for **readonly** class properties.
  > NOTE: readonly keyword is available only in TS and not in JS.

## Interfaces
1. Use ProperCase (PascalCase) when naming interfaces and use Props as suffix for typecheking component Props, eg CustomerReviewProps.
    ```
    // bad
    interface person { // not used ProperCase 
      name: string;
      age:  number;
    }  
    
    // good
    interface PersonI {
      name: string;
      age:  number;
    }  
    ```

## Types
1. Use ProperCase (PascalCase) when naming types.
    ```
    // bad
    type stringOrNumber = string | number; // instead of camelCase use ProperCase.
    
    // good
    type StringOrNumber = string | number;
    type FilterType = 'chips' | 'checkbox' | 'radio' | 'calendar' | 'toggle';
    
