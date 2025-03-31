# Pixel-Smile

## About

Pixel Smile is a program that creates pixel art and outputs a smiley face to the console. It starts as a half implemented program, with the focus on understanding functions and leveraging TypeScript’s type system to fix bugs and guide our implementation of the missing functions.

## Features and breakdown of the code

- The variables `imageWidth`, `imageHeight`, and `imageData` are used to store the image data.
- The `createImageData()` function returns a boolean array of `false` values equal to the length of the image (calculated by multiplying the `imageWidth` and `imageHeight`). The resulting array is stored in the `imageData` variable.
- The shape and lines of the image are stored and created by changing the index values in the `imageData` array to `true` at the positions where a line or dot is required.
- The correct index positions in the array to update are calculated and located using functions: `drawDot()`, `drawHorizontalLine()`, `drawVerticalLine()`, and `drawRectangle()` which take in `x` and `y` positions and `length`/`height` as arguments.
- The `drawDot()` function uses the formula, `y \* imageWidth + x` to locate the index of the pixel in the `imageData` array and assigns the `true` value to that index.
- The `isPointInImage()` function checks that the specified point is within the bounds of the image.
- The `outputImage()` function iterates through the `imageData` array with a `for` loop. It uses a different character to represent each of the `true` and `false` values and prints the image to the console. The default parameters in this function allow for the user to customise the characters used for the pixels.

## Technologies used

- TypeScript
