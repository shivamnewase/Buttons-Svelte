<!-- src/lib/Button.svelte -->
<script>
    export let label;
    export let classList = "";
  
    const getClassNames = () => {
      return `button ${classList}`.trim();
    };
  </script>
  
  <button class={getClassNames()}>{label}</button>
  
  <style>
    .button {
      background-color: #007bff;
      color: #ffffff;
      padding: 10px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
  </style>
  