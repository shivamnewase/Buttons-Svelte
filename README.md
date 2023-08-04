# buttons-svelte

Buttons-Svelte is a library for Svelte, providing reusable button components.

## Installation

You can install the `buttons-svelte` library using npm:

```bash
npm install buttons-svelte
```

## Usage

To use the button components in your Svelte project, import them from the library:
### customClass
 
 - custom class use for apply button color

```bash
<script>
  import { Button } from "buttons-svelte";
</script>

<Button>Click Me</Button>
<Button customClass="btn-red-50"  >Button</Button>
<Button customClass="btn-red-50"  >Button</Button>
<Button customClass="btn-red-100" >Button</Button>
<Button customClass="btn-red-200" >Button</Button>
<Button customClass="btn-red-300" >Button</Button>
<Button customClass="btn-red-400" >Button</Button>
<Button customClass="btn-red-500" >Button</Button>
<Button customClass="btn-red-600" >Button</Button>
<Button customClass="btn-red-700" >Button</Button>
<Button customClass="btn-red-800" >Button</Button>
<Button customClass="btn-red-900" >Button</Button>
<Button customClass="btn-red-900" >Button</Button>
<Button customClass="btn-red-900" >Button</Button>

```
### Size
```bash
<script>
  import { Button } from "buttons-svelte";
</script>

<Button textSize="text-2">Button</Button>
<Button textSize="text-4">Button</Button>
<Button textSize="text-6">Button</Button>
<Button textSize="text-8">Button</Button>
<Button textSize="text-10">Button</Button>
<Button textSize="text-12">Button</Button>
 .....
<Button textSize="text-36">Button</Button>

```
or
```bash
<script>
  import { Button } from "buttons-svelte";
</script>

<Button textSize="200px">Button</Button>
```
## Available Props

The `Button` component accepts the following props:

-   `customClass` (string, default: ""): The custom CSS class to apply to the button for additional styling.
-   `onclick` (function, default: null): The event handler function to be called when the button is clicked.

## Examples
### Basic Usage
```bash
<script>
  import { Button } from "buttons-svelte";
</script>

<Button>Click Me</Button>
```


### Handling Click Events

```bash
<script>
  import { Button } from "buttons-svelte";

  const handleClick = () => {
    console.log("Button clicked!");
  };
</script>

<Button onclick={handleClick}>Click Me</Button>

```
## Example
```bash
<script>
  import { Button } from "buttons-svelte";

  const handleClick = () => {
    console.log("Button clicked!");
  };
</script>

<Button onclick={handleClick} customClass="btn-red-500" textSize="text-2">Click Me</Button>
```

## Contributing

Contributions to the `buttons-svelte` library are welcome! If you find a bug, have a feature request, or want to contribute code, please open an issue or submit a pull request on the [GitHub repository](https://github.com/shivamnewase/Buttons-Svelte).

## License

This project is licensed under the MIT License. See the [LICENSE](https://chat.openai.com/c/LICENSE) file for details.


This `README.md` file includes the introduction, installation instructions, usage guidelines, available props for the `Button` component, usage examples, contribution guidelines, and licensing information for the "buttons-svelte" library, all written in Markdown format. You can copy and paste this content into your actual `README.md` file for your library and customize it as needed.
