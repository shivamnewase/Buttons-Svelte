![Buttons-Svelte](/static/buttons-svelte.png)

<!-- ![Buttons-Svelte](./static/button-svelte01-48.svg) -->


# Buttons-Svelte

Buttons-Svelte is a library for Svelte, providing reusable button components.

## Introduction

Buttons-Svelte is a powerful and flexible library for creating beautiful and interactive buttons in Svelte applications. It offers a wide range of customization options, allowing you to create buttons with various colors, sizes, padding, and margins.

## Features

- Easy-to-use button components for Svelte applications.
- Customize button color, text color, padding, and margins.
- Choose from a variety of predefined button colors or use custom colors.
- Adjust the font size and font family to match your design.
- Lightweight and optimized for performance.

## Installation

You can install the `buttons-svelte` library using npm:

```bash
npm install buttons-svelte
```


## Usage
To use the button components in your Svelte project, import them from the library:


```bash
<script>
  import { Button } from "buttons-svelte";
</script>

<Button>Click Me</Button>
<Button btnColor="btn-red-500">Button</Button>
<Button btnColor="btn-green-600">Button</Button>
<Button btnColor="btn-blue-500">Button</Button>
<Button btnColor="#ff00ff">Button</Button>
```

## Available Props
##### The Button component accepts the following props:


| Props    | Type    |  Default Type | Description |
| -------- | ------- | ------------- | ----------- |
| btnColor |  string |       " "     | Custom CSS property to apply buttoncolor. |
| onClick  | function|      null     | Event handler function for button click. |
| onMouseOver| function|      null     | Event handler function for mouse pointer is over the button |
| onMouseOut| function|      null     | Event handler function for mouse pointer leaves the button |
| textColor| string  |       " "     | Custom CSS property for text color. |
|  textSize | string |       " "     | Custom CSS property for text size. |
| padding   | string |       " "     | Custom CSS property for padding. |         
| margin   |  string |       " "     | Custom CSS property for margin. |
| border   |  string |        " "    | Custom CSS property for border. |
| borderRounded| string |     " "    | Custom CSS property for rounded border.|
	
## Examples
##### Basic Usage 
  
```bash
<script>
  import { Button } from "buttons-svelte";
</script>

<Button>Click Me</Button>
```	

## Handling Click Events
```bash
<script>
  import { Button } from "buttons-svelte";

  const handleClick = () => {
    console.log("Button clicked!");
  };
</script>

<Button onclick={handleClick}>Click Me</Button>
```

## Customizing Buttons
```bash
<script>
  import { Button } from "buttons-svelte";
</script>

<Button btnColor="btn-red-500" padding="p-6" textColor="green" textSize="text-2">Click Me</Button>
<Button btnColor="btn-blue-500" padding="p-8" textColor="white" textSize="text-4">Submit</Button>
<Button btnColor="#ff00ff" padding="p-10" textColor="black"textSize="text-6">Cancel</Button>

```

## CSS Units

`  px ` `  rem ` `  em ` ` % ` 
Use any for styling purpose

## Contributing

Contributions
Yes please! See the contributing guidelines for details.
[contributing guidelines](https://github.com/shivamnewase/Buttons-Svelte).



### License

By contributing to the buttons-svelte library, you agree that your contributions will be licensed under the [MIT License]

Thank you for contributing to buttons-svelte! Your help is greatly appreciated!

