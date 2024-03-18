# Coding Practices

## Classes:

#### Regions: 

Regions MUST ALWAYS be used in classes, no matter how small.
The following lists the order in which the regions must appear.

1. Events
   Anything related to this class' events. Delegates, Invoke methods and even EventArgs classes.
2. Definitions
   Definitions should be arranged as follows and by alphabetical order.
   1. Private
   2. Public
   3. Property
   4. Dependency
3. Constructor
   1. The use of Ini is a must to handle complex initializations.
4. Methods
   1. UI related methods such as initializations and settings.
   2. Public
   3. Private
   4. Big Chunks (Optional)
   5. Implementation Overrides
5. Callbacks (Delegates)
   1. UI
   2. Classes used to handle Callbacks
6. Miscellaneous
7. Classes that are considered an inseparable part of its container class.
8. Utils to be used only with its container class.
9. Example describing how to use the class.

#### Variables: 

All variable naming must adhere to the following conventions.

1. private _aBcd
2. protected Abcd
3. byval aBcd
4. public Abcd
5. local aBcd
6. parameters aBcd
7. NO UNDERSCORES IN THE MIDDLE OF NAMES.

#### Properties

Include name, description and, category - name, special attributes (xmlIgnore)

#### Enums

An Enumeration is singular and not plural, each member is named following the Pascal Case convention.
For example:

> <code>
> enum ConnectionType
> {
>   Connected,
>   Disconnected
> }
> </code>

#### Copy Right - Technica Confidential

All Classes must include the following copyright.

> #Region "Copyright (C) %CreationYear% by Technica international"
> ///*************************************************************************
> //* Programmer: Your Name Here (%UserName%)
> //* Created: %CreationYear%, %CreationMonth%, %CreationDay%, %CreationTime%
> //*
> //* Technica CONFIDENTIAL
> //* _____________________
> //*
> //* [2016] - [2019] Technica International
> //*  All Rights Reserved.
> //*
> //* NOTICE:  All information contained herein Is, And remains
> //* the property of Technica International And its suppliers,
> //* if any.  The intellectual And technical concepts contained
> //* herein are proprietary to Technica International
> //* And its suppliers And may be covered by Foreign Patents,
> //* patents in process, And are protected by trade secret Or copyright law.
> //* Dissemination of this information Or reproduction of this material
> //* Is strictly forbidden unless prior written permission Is obtained
> //* from Technica International.
> //*
> //*************************************************************************/
> //#End Region

## User Interface

- WPF is the main platform - unless visuals are non existent or project consist of only 5 to 10 views use WinForms or console (good and fast for prototyping)
- The MVVM pattern must be applied in projects.
- In Custom views, the MVVM it is possible that the MVVM pattern is not practical. This is only applicable to small custom views such as a modified TextBox or Button that don't require runtime modifications through a ViewModel and don't necessarily expose a model.
- XAML code and naming must also adhere to Technica's naming conventions.
- Creating a user control/custom view is a must if it is used in more 1 views.
- Resources pictures should be PNG.
- When naming controls, the first letters should point to the type of control.
  Button: btn-  btnAdd, btnDelete.
  TextBox: txt-  txtName, txtDescription.
  TextBlock: tb- tbAge, tbContent.
  CheckBox: ch- chRememberMe, chForgetOthers
  ComboBox: cb- cbCategory, cbYear.
  ImageView: im- imUser, imLogo.

## Documentation:

1. Documentation on public delegates (private if necessary)
2. Anything other than private elements must be documented in library projects.
3. Public members must be documented in projects.
4. External libraries must be credited, if possible, make sure to check its licensing rules

## Coding Style

#### General

1. Const, Shared, IEnumerable readonly array (if possible, return)
2. == null (? character after variable) for methods only in a variable
3. Lambda expression if possible
4. Local variable should not be similar to global
5. Tuples usage - if necessary
6.  ? in the type for nullable
7. ?? on null datatype to give it value (ex Object?.Size??0)
8. ternary  (x=0) ? y = 2 : y = 3 (can be used) or If(x=0,y=2,y=3)
9. collapse file after finish editing
10. if in routine parameter name similar to a variable (put s or d at the begining for its type hungarian naming)  - avoid if possible
11. hungarian only in routine parameters - avoid if possible
12. all variables use explicit datatype
13. boolean variable should include "Is" in naming

#### Events, Delegates and Actions

1. Action delegates ?.Invoke
2. Events are preferably invoked using an Invoke method.
3. events for delegates with arguments (or event action for simple events) - (object sender, EventArgs e)
4. event handler signatures MUST adhere to handler(object sender, EventArgs e)
5. events in .NET are created using EventHandler\<T>

## Debugging and Testing

1. Performance check use stopwatch from Utils. Log data to output (not use debugging, it hinders performance)  - debugging  is for debug
2. Use Trace.WriteLine and Debuf.WriteLine for debugging, and Console.WriteLine for Console.
3. Analyze Code, with Exceptions
   3.1. not used (if necessary)
   3.2. IEnumerable (if not necessary instead of array)
4. Code metrics: 
   4.1. Maintainability Index = < 80 ( it should be divided into smaller classes) - exceptions can exist
   4.2. Cyclomatic: Functions <15 and Class Lines count/4
5. When working with core libraries a console application must be implemented to test the library
6. Code Review DevOps Subscription
7. throw new ArgumentNullException(  nameof (x))    - (for debbuguing something real bad)

## Projects Structure

1. general resources are in Resources Library
2. Folders in project means namespace
3. No external libraries in libraries (only source code) (except UI) - if a must (open a new library and wrap it in a class) - to avoid dependency if not used
4. external libraries DLLs should be in the folder of the project under (Libs)
5. maximum bared .NET framework ( .Net core if possible or 4.5 for libraries preferred lowest possible) and (4.7 and above for projects)
6. no visuals in utils
7. resource add (_ico) to icons
8. library namespace should be Tech.xxx.xxx
9. Settings(only main project) and resources (no name space) - names Settings and Resources - (Libraries should not have settings rather use class setting if needed else use main project application settings) . Utilities project shouldn't have resources
10. .NET standard 2.0 for libraries
11. framework changes on library must be discussed before (utilities must be minimum of 4) - apps focus on (4.5) for maximum support unless required - application minimum (4.5)
12. DLL Assembly usage purpose (full definition extracted from the website)
13. Reference assemblies needed to be added to libraries need to be reviewed (to avoid conflicts) - requires request
14. Exception class if needed when proofing an important class
15. Resources files are all small caps
16. CLS Compliant (Not needed)
