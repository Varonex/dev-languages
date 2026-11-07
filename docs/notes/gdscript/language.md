# GDScript

## Introduction

GDScript is a **DSL** (Domain Specific Language) which is only used in the [Godot](https://godotengine.org) ecosystem to make games, or dedicated softwares.

It is an object-oriented language, whose goal is to override inbuilt methods to respect objects' lifecycles and interact with the engine.

## Basics

GDScript uses `snake_case` for all of its identifiers.

### Variable declaration

A variable can be declared in two distinct scopes.
It can be declared in the **global scope** if it is defined as is in the file, or **local to a scope** if it is embedded within a block.

!!! note "Globalscope and fields"
	Every variable declared in global will eventually become a class field.

The keyword `var` is used to define a variable :

```gd
var my_var
```

You can directly assign a value to it :

```gd
var my_int = 2
var my_float = 2.0 // Float.
```



### Class declaration

A `.gd` file will always define an anonymous class. That being said, everything you write in a file will be part of the implicit declared class.

!!! warning "No Polymorphism"
	Polymorphism is **not** supported!