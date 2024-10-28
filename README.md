# International Phone Input Mask - Vanilla JavaScript

This repository provides a simple and lightweight input masking solution for international phone numbers using only vanilla JavaScript. The script automatically applies a mask to phone number inputs, dynamically adapting to the appropriate format based on the user's input.

## Features

- Supports international phone numbers.
- Automatically detects the closest matching mask based on the input.
- Lightweight and easy to integrate.
- Vanilla JavaScript - no external dependencies.
- Included a list of 205 countries with 294 regex patterns. 

## Usage

### 1. Include the Script

Add the script to your HTML file:

```html
<script src="path/to/your/local/folder/vanilla-mask-input.js"></script>
```
or
```html
<script src="https://cdn.delcantao.dev/js/vanilla-mask-input-min.js"></script>
```


### 2. Initialize the Mask

Use the ``vanillaMaskInput`` function to apply the mask to your input fields.

```html
<input type="text" id="phone-input" placeholder="Enter phone number"/>
<script>
    vanillaMaskInput('#phone-input');
</script>
```

### 3. Mask List Example

The script works with a predefined list of masks, where each mask has a regex pattern and a country-specific format. Below is a sample structure for the maskList:

```html
<input type="text" class="phone-input" placeholder="Enter phone number">
<script>
    const maskList = [
        {
            country_mask: "+1 (###) ###-####",
            regex: "^\\+1\\d{0,3}\\d{0,3}\\d{0,4}$"
        },
        {
            country_mask: "+55 (##) #####-####",
            regex: "^\\+55\\d{0,2}\\d{0,5}\\d{0,4}$"
        }
    ];

    vanillaMaskInput('.phone-input');
</script>
```

When the user starts typing, the input field will automatically apply the appropriate mask based on the country code.

### How It Works
1. ```findClosestMask(input)```: Searches the mask list to find the closest matching mask based on the user's input.
2. ```setMask()```: Applies the mask dynamically to the input field.
3. ```vanillaMaskInput(selector)```: Initializes the masking for all inputs matching the specified selector.

### Contributing
Feel free to fork this repository and make improvements! Contributions are welcome.

### License
This project is licensed under the MIT License.







