# Riad Image Generate AI

A library for generating images using a custom API. This package allows developers to easily integrate image generation functionality into their applications using various technologies like React, Next.js, HTML, CSS, and JavaScript.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [Using with React](#using-with-react)
  - [Using with Next.js](#using-with-nextjs)
  - [Using in Plain HTML/CSS/JavaScript](#using-in-plain-htmlcssjavascript)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)

## Installation

To install the package, you can use npm or yarn. Here’s how:

### Using npm

```bash
npm install riad-ai-imagegen
```

### Using yarn

```bash
yarn add riad-ai-imagegen
```

## Usage

### Using with React

Here’s how to use the library in a React application:

1. **Install the package** (as shown above).
2. **Import the library** into your component.

```javascript
import React, { useState } from 'react';
import { generateImage } from 'riad-ai-imagegen';

const ImageGenerator = () => {
  const [imageData, setImageData] = useState(null);

  const handleGenerate = () => {
    generateImage("cute girls")
      .then(result => {
        setImageData(result); // Process and set the generated image data
      })
      .catch(error => {
        console.error("Error generating image:", error);
      });
  };

  return (
    <div>
      <button onClick={handleGenerate}>Generate Image</button>
      {imageData && <img src={imageData.url} alt="Generated" />} {/* Display the generated image */}
    </div>
  );
};

export default ImageGenerator;
```

### Using with Next.js

For Next.js, the process is similar to React. You can use the library in a component like this:

1. **Install the package** (as shown above).
2. **Import the library** into your Next.js component.

```javascript
import { useState } from 'react';
import { generateImage } from 'riad-ai-imagegen';

const ImageGenerator = () => {
  const [imageData, setImageData] = useState(null);

  const handleGenerate = () => {
    generateImage("cute girls")
      .then(result => {
        setImageData(result); // Process and set the generated image data
      })
      .catch(error => {
        console.error("Error generating image:", error);
      });
  };

  return (
    <div>
      <button onClick={handleGenerate}>Generate Image</button>
      {imageData && <img src={imageData.url} alt="Generated" />} {/* Display the generated image */}
    </div>
  );
};

export default ImageGenerator;
```

### Using in Plain HTML/CSS/JavaScript

If you want to use the library without a build tool, include the minified version directly in your HTML file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Generator Example</title>
</head>
<body>

<button onclick="generateImage()">Generate Image</button>
<script src="https://cdn.jsdelivr.net/npm/riad-ai-imagegen/dist/riad-image-generate.min.js"></script>
<script>
    function generateImage() {
        RiadImageGenerate.generateImage("cute girls")
            .then(result => {
                console.log("Generated image:", result); // Handle the generated image
                // Display the image or further process it
            })
            .catch(error => {
                console.error("Error generating image:", error); // Handle errors
            });
    }
</script>

</body>
</html>
```

## API Reference

### `generateImage(content)`

- **Parameters**: 
  - `content` (String): The content for which the image will be generated.
- **Returns**: A promise that resolves to the generated image data.

**Example**:
```javascript
generateImage("cute girls")
    .then(result => {
        console.log(result); // Contains the generated image data
    })
    .catch(error => {
        console.error("Error:", error);
    });
```

## Contributing

We welcome contributions! Please feel free to submit a pull request or open an issue for discussion.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```

### Key Points

- **Installation**: Clear instructions for both npm and yarn users.
- **Usage Examples**: Covers React, Next.js, and plain HTML/CSS/JavaScript, allowing developers to understand how to use the library in various environments.
- **API Reference**: Provides a concise description of the primary function, helping users understand how to implement it.
- **Contributing Section**: Encourages collaboration, which is important for open-source projects.
- **License Section**: Clearly states the licensing for the project.

### How to Update Your README.md

1. **Edit the file** directly in your GitHub repository:
   - Go to your repository: [riad-image-generate-ai](https://github.com/RiadDeveloperr/riad-image-generate-ai).
   - Navigate to the `README.md` file.
   - Click on the pencil icon to edit.
   - Paste the above content into the file.
   - Commit the changes with a meaningful message.

2. **View the updated README** on your GitHub repository page to ensure it displays correctly.
