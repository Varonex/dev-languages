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

You can directly assign a value to it:

```gd
var my_int = 2 # Integer.
var my_float = 2.0 # Float.
```

It is advised to give a type to your variables:

```gd
var my_int: int = 2 # Integer.
var also_my_int: int = 2.0 # Integer.
```

Not only do types help you refine your codebase, but they also provide optimizations as Godot does not need to predict the type of the variable at runtime.

You can also use type inference whenever you declare a value with a type:

```gd
var my_int := 2 # Integer.
var not_my_int := 2.0 # Float.
```

However, this technique can be error-prone depending on your code.

### Class declaration

A `.gd` file will always define an anonymous class. That being said, everything you write in a file will be part of the implicit declared class.

!!! warning "No Polymorphism"
	Polymorphism is **not** supported!