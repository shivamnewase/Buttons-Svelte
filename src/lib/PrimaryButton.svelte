<!-- src/lib/Button.svelte -->
<script>
    export let customClass = "primary";
    export let textSize = "md"; // Add the size prop with a default value
    export let textColor = "black";
    export let onclick = null;
    export let padding = "md"; // Add the padding prop with a default value

    const getPaddingValues = (padding) => {
    const paddingSizes = {
        "p-0": "2px 4px",
        "p-2": "4px 8px",
        "p-4": "6px 12px",
        "p-6": "8px 18px",
        "p-8": "10px 20px",
        "p-10": "12px 24px",
        "p-12": "14px 28px",
        "p-14": "16px 32px",
        "p-16": "18px 36px",
        "p-18": "18px 38px",
        "p-20": "20px 40px",
        "p-24": "24px 48px",
        "p-28": "28px 56px",
        "p-32": "32px 64px",
        "p-36": "36px 72px",
        "p-auto": "auto auto",
    };
    return paddingSizes[padding] || paddingSizes.md;
  };

  const getTextSize = (textSize) => {

    if (textSize.endsWith('px')) {
            return textSize;
        }
    const textSizes = {
        "text-0" :"2px",
        "text-2" :"4px",
        "text-4" :"8px",
        "text-6" :"12px",
        "text-8" :"16px",
        "text-10" :"20px",
        "text-12" :"24px",
        "text-14" :"28px",
        "text-16" :"32px",
        "text-18" :"36px",
        "text-20" :"40px",
        "text-24" :"44px",
        "text-28" :"48px",
        "text-32" :"52px",
        "text-36" :"56px",
        "text-40" :"60px",
        "text-44" :"66px",
        "text-48" :"72px",
        "text-52" :"78px",
        "text-56" :"84px",
        "text-auto":"auto"
    };
    return textSizes[textSize] || textSizes.md;
  };

    // Function to combine default class, user-provided customClass, and button size
    const getClassNames = () => {
        const colorClass = customClass.startsWith('btn-') ? customClass: `btn-${customClass}`;
        return `button ${colorClass}`.trim();
    };
</script>

<button class={getClassNames()} style={`color: ${textColor} !important; padding: ${getPaddingValues(padding)}; font-size: ${getTextSize(textSize)};`} on:click={onclick}><slot></slot></button>

<style>
    .button {
        color: #ffffff;
        padding: 10px 20px;
        border: none;
        border-radius: 4px;
        cursor: pointer;
    }

    .btn-red-50{
        background-color: #ffd9d9 ;
     }
    
     .btn-red-100{
        background-color:  #ffcccc ;
     }
     .btn-red-200{
        background-color:  #ffbfbf;
     }
     .btn-red-300{
        background-color:  #ff9999 ;
     }
     .btn-red-400{
        background-color: #ff4d4d  ;
     }
     .btn-red-500{
        background-color:  #FF0000  ;
     }
     .btn-red-600{
        background-color: #e60000 ;
     }
     .btn-red-700{
        background-color: #bf0000  ;
     }
     .btn-red-800{
        background-color: #990000 ;
     }
     .btn-red-900{
        background-color: #7d0000;
     }
  .btn-blue-50{
    background-color: #d9d9ff;
  }
  .btn-blue-100{
    background-color: #ccccff ;
  }
  .btn-blue-200{
    background-color:#bfbfff ;
  }
  .btn-blue-300{
    background-color:#9999ff  ;
  }
  .btn-blue-400{
    background-color: #4d4dff ;
  }
  .btn-blue-500{
    background-color: #0000FF ;
  }
  .btn-blue-600{
    background-color: #0000e6;
  }
  .btn-blue-700{
    background-color:#0000bf  ;
  }
  .btn-blue-800{
    background-color:#000099  ;
  }
  .btn-blue-900 {
    background-color: #00007d ;
  }
  .btn-green-50{
    background-color: #d9ffd9;
  }
  .btn-green-100{
    background-color:#ccffcc ;
  }
  .btn-green-200{
    background-color: #bfffbf;
  }
  .btn-green-300{
    background-color: #99ff99;
  }
  .btn-green-400{
    background-color: #4dff4d;
  }
  .btn-green-500{
    background-color: #00FF00;
  }
  .btn-green-600{
    background-color:#00e600 ;
  }
  .btn-green-700{
    background-color:#00bf00 ;
  }
  .btn-green-800{
    background-color:#009900 ;
  }
  .btn-green-900{
    background-color:#007d00 ;
  }
  .btn-yellow-50{
    background-color: #ffffd9;
  }
  .btn-yellow-100{
    background-color: #ffffcc;
  }
  .btn-yellow-200{
    background-color: #ffffbf;
  }
  .btn-yellow-300{
    background-color: #ffff99 ;
  }
  .btn-yellow-400{
    background-color: #ffff4d;
  }
  .btn-yellow-500{
    background-color: #FFFF00;
  }
  .btn-yellow-600{
    background-color: #e6e600;
  }
  .btn-yellow-700{
    background-color:#bfbf00;
  }
  .btn-yellow-800{
    background-color: #999900 ;
  }
  .btn-yellow-900{
    background-color:#7d7d00;
  }
  .btn-orange-50{
    background-color: #fff2d9;
  }
  .btn-orange-100{
    background-color:#ffedcc;
  }
  .btn-orange-200{
    background-color:#ffe9bf;
  }
  .btn-orange-300{
    background-color: #ffdb99;
  }
  .btn-orange-400{
    background-color:  #ffc04d ;
  }
  .btn-orange-500{
    background-color: #FFA500;
  }
  .btn-orange-600{
    background-color: #e69500;
  }
  .btn-orange-700{
    background-color:  #bf7c00 ;
  }
  .btn-orange-800{
    background-color: #996300 ;
  }
  .btn-orange-900{
    background-color: #7d5100 ;
  }
  .btn-purple-50{
    background-color: #ecd9ec;
  }
  .btn-purple-100{
    background-color: #e6cce6;
  }
  .btn-purple-200{
    background-color: #dfbfdf;
  }
  .btn-purple-300{
    background-color: #cc99cc ;
  }
  .btn-purple-400{
    background-color: #a64da6 ;
  }
  .btn-purple-500{
    background-color: #800080;
  }
  .btn-purple-600{
    background-color: #730073;
  }
  .btn-purple-700{
    background-color: #600060;
  }
  .btn-purple-800{
    background-color: #4d004d;
  }
  .btn-purple-900{
    background-color: #3f003f;
  }
  .btn-pink-50{
    background-color: #fff6f7 ;
  }
  .btn-pink-100{
    background-color: #fff2f5 ;
  }
  .btn-pink-200{
    background-color:#ffeff2;
  }
  .btn-pink-300{
    background-color:  #ffe6ea;
  }
  .btn-pink-400{
    background-color:#ffd3db;
  }
  .btn-pink-500{
    background-color: #FFC0CB;
  }
  .btn-pink-600{
    background-color:  #e6adb7;
  }
  .btn-pink-700{
    background-color: #bf9098;
  }
  .btn-pink-800{
    background-color:  #99737a ;
  }
  .btn-pink-900{
    background-color:  #7d5e63 ;
  }
  .btn-gray-50{ 
    background-color:#ececec;
 }
 .btn-gray-100{
       background-color:#e6e6e6; 
    }
 .btn-gray-200{
    background-color:#dfdfdf;
 }
 .btn-gray-300 {
    background-color:#cccccc;
 }
 .btn-gray-400 {
    background-color:#a6a6a6;
 } 
	.btn-gray-500 {
        background-color:#808080;
     }
	.btn-gray-600 {
        background-color:#737373;
     }
	.btn-gray-700 {
        background-color:#606060;
    } 
	.btn-gray-800 {
        background-color:#4d4d4d;
     }
	.btn-gray-900 {
        background-color:#3f3f3f;
     }
     .btn-silver-50{
        background-color:#f6f6f6;
     }
     .btn-silver-100{
        background-color: #f2f2f2;
     }
     .btn-silver-200{
        background-color: #efefef;
     }
     .btn-silver-300{
        background-color:#e6e6e6;
     }
     .btn-silver-400{
        background-color: #d3d3d3;
     }
     .btn-silver-500{
        background-color:#C0C0C0;
     }
     .btn-silver-600{
        background-color:#adadad;
     }
     .btn-silver-700{
        background-color:#909090;
     }
     .btn-silver-800{
        background-color:#737373;
     }
     .btn-silver-900{
        background-color:#5e5e5e;
     }

    .btn-brown-50{
    background-color: #f2dfdf ;
    }
    .btn-brown-100{
    background-color: #edd4d4 ;
    }
    .btn-brown-200{
    background-color: #e9caca ;
    }
    .btn-brown-300{
    background-color: #dbaaaa;
    }
    .btn-brown-400{
    background-color:  #c06a6a ;
    }
    .btn-brown-500{
    background-color: #A52A2A;
    }
    .btn-brown-600{
    background-color: #952626;
    }
    .btn-brown-700{
    background-color:  #7c2020;
    }
    .btn-brown-800{
    background-color: #631919;
    }
    .btn-brown-900{
    background-color: #511515;
    }

    /* Define different button sizes */
    .xs {
    font-size: 8px;
  }

  .sm {
    font-size: 9px;
  }

  .md {
    font-size: 11px; /* Default size */
  }

  .lg {
    font-size: 13px;
  }

  .xl {
    font-size: 15px;
  }

  .xxl {
    font-size: 17px;
  }

  .p-0 {
    font-size: 4px;
  }

</style>
