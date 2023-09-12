# CubePal Links

### *About CubePal*

CubePal is an iOS app designed for learning algorithms and solving virtual 2x2x2, 3x3x3, 4x4x4, and 5x5x5 cubes and supercubes.

You can download the FREE CubePal application on the [App Store](https://apps.apple.com/app/cubepal/id1501885433).

For additional information, please visit the app's landing page at [www.cubepal.app](https://www.cubepal.app).

### *About Universal Links*

CubePal Links is an implemetation of the Universal Links (also referred to as App Links or Deep Links) are web URLs that, when tapped on a mobile device, seamlessly open the associated app, triggering specific actions or features defined by the link's parameters. CubePal allows users to generate, export, share, modify, and use their own Universal Links as described below.

### *Why Using CubePal Links*

CubePal Links enable users to create, store, and share custom Universal Links. These links can be generated within the CubePal app or written manually and stored anywhere, including websites, other apps, or local storage. This feature simplifies the sharing of algorithms, allowing anyone to effortlessly open the algorithms and learn them using virtual cubes within the CubePal app on their mobile devices.

## Prerequisites
Before you start using CubePal Links or at least if you want to test them on a mobile device, ensure that you meet the following requirements:
- **iOS Device**: You must have an iOS device, such as an iPhone or iPad, to open CubePal Links with the app.
- **iOS Version**: Your iOS device should be running iOS 14.0 or a higher version for CubePal Links to function correctly.

## Creating CubePal Links
To create a CubePal Link that opens within the CubePal app, use the following format:

```
https://www.cubepal.app/alg?
```

Additionally, you must include URL parameters to pass information to the CubePal app. Check out the Parameters section below for more details.

## Using CubePal Links

Using CubePal Links is straightforward. Feel free to utilize CubePal Links for your personal needs or share them with others through any platform or technology of your choice.

1. **Tap the Link**: To open the CubePal app with a specific action or content, simply tap on the CubePal Link you've either created or saved. The app will automatically launch and open the respective cube and algorithm.

2. **Versatile Accessibility**: CubePal Links can be initiated from various sources, including files, emails, notes and other apps on your iOS device.

## Creating CubePal Links

You can generate CubePal Links within the CubePal app using current cube and algorithm or scramble, or you can write the CubePal Links manually using the correct format and parameters. 

**Option A: Generate CubePal Links within the app**
- Open CubePal app on your mobile device.
- Navigate to the desired cube and algorithm or scramble you want to share or save.
- Optionally, customise the cube or supercube design and color scheme as needed.
- Tap the menu button or the algorithm to open the menu and tap Share. 

**Option B: Manually Create CubePal Links**
- Write the link manually in the appropriate format described in this documentation.
- Ensure that you include the necessary parameters, as listed in the Parameters section.
- Save the link in your preferred location, such as websites, other apps, or local storage.
- Tip: Use the app to test the newly created link before sharing it.

## CubePal Link Parameters

URL parameters are used to convey information to the CubePal app. These parameters are essential for showing the desired cubes and algorithms within the app.

### General Guidelines

- Add parameters after the question mark `?` without spaces, like this:
  ```
  https://www.cubepal.app/alg?alg=R-_F_U_R
  ```
- Separate parameters using the ampersand symbol `&`, like this:
  ```
  https://www.cubepal.app/alg?cube=4x4x4&alg=R-_F_U_R&scheme=japanese
  ```
- You can omit any parameter except the algorithm sequence.
- The algorithm sequence should contain at least two turns or moves.
- While the order of the parameters can be changed, for the sake of consistency, it is recommended to use the order outlined in the table below.
- Algorithms turns should be separated by underscores `_` (recommended for readability) or by percent-encoded spaces `%20`.
- Algorithms turns are the only case sensitive values.

### Parameters

|  Parameter  | Value  |  Functionality  |
|---|---|---|
| `alg` | <pre>alg=R-_F_U2_R</pre> |  Specifies a particular algorithm (sequence of cube turns) separated by underscore `_`. <br />Inverted turns `'` are represented by dash sign `-`. |
|   |   | Example: https://www.cubepal.app/alg?alg=R-_F_U2_R <br />Opens the algorithm: `R' F U2 R` |
| ` ` |  <pre>=R_U-_F_R-</pre> | Empty parameter has the same funtionality as `alg`. <br />The parameter's name can be omitted only when the sequence is an algorithm. |
|   |   | Example: https://www.cubepal.app/alg?=R_U-_F_R- <br />Opens the algorithm: `R U' F R'` |
| `scr` |  <pre>scr=R-_F_U_R</pre> |  Specifies a particular cube scramble.|
|   |   | Example: https://www.cubepal.app/alg?scr=R-_F_U_R <br />Opens the cube in its scrambled state using the `R U' F R'` scramble. |
| `rec` |  <pre>rec=R-_F_U_R</pre>  |  Specifies a particular cube reconstruction. |
|   |   | Example: https://www.cubepal.app/alg?rec=R-_F_U_R <br />Opens the reconstructed cube using the `R U' F R'` sequence. |
| `pat` |  <pre>pat=R-_F_U_R</pre>  |  Specifies a particular cube pretty pattern. |
|   |   | Example: https://www.cubepal.app/alg?pat=R-_F_U_R <br />Opens the cube pattern using the `R U' F R'` sequence. |
| `cube` |  <pre>cube=</pre>   |  Specifies a particular cube size (dimension). <br />Both parameter and its value are optional. Default value is `3x3x3`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube= <br /> Example 2: https://www.cubepal.app/alg?=R-_F_U_R<br />Both examples open the `R U' F R'` algorithm and the `3x3x3` cube. |
|   |  <pre>cube=2x2x2</pre>  |  Specifies a 2x2x2 cube. <br />Equivalent values: `2`, `2x2`, `pocket`, `mini`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube=2x2x2 <br />Example 2: https://www.cubepal.app/alg?=R-_F_U_R&cube=mini <br />Both examples open the `R U' F R'` algorithm and the `2x2x2` cube. |
|   |  <pre>cube=3x3x3</pre>  |  Specifies a 3x3x3 cube. Parameter and value are optional for 3x3x3 cube. <br />Equivalent values: `3`, `3x3`, `rubik`, `magic`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube=3x3x3 <br />Example 2: https://www.cubepal.app/alg?=R-_F_U_R <br />Both examples open the `R U' F R'` algorithm and the `3x3x3` cube. |
|   |  <pre>cube=4x4x4</pre>  |  Specifies a 4x4x4 cube. <br />Equivalent values: `4`, `4x4`, `revenge`, `master`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube=4x4x4<br />Example 2: https://www.cubepal.app/alg?=R-_F_U_R&cube=revenge <br />Both examples open the `R U' F R'` algorithm and the `4x4x4` cube. |
|   |  <pre>cube=5x5x5</pre>  |  Specifies a 5x5x5 cube. <br />Equivalent values: `5`, `5x5`, `professors`, `professor`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube=2x2x2<br />Example 2: https://www.cubepal.app/alg?=R-_F_U_R&cube=5<br />Both examples open the `R U' F R'` algorithm and the `5x5x5` cube. |
| `super` |  <pre>super=</pre> | |
| | <pre>super=none</pre> |  Equivalent values: `classic`, `standard` |
| | <pre>super=triangles</pre> | Equivalent values: `triangle`, `triangular` |
| | <pre>super=arrowheads</pre> | Equivalent value: `arrowhead` |
| | <pre>super=arrows</pre> | Equivalent values: `arrow`, `arr`, `shepherd` |
| | <pre>super=hint</pre> | Equivalent values: `hints`, `pochmann`, `poch` |
| `mod` | <pre>mod=</pre> | | 
| | <pre>mod=small</pre> | Equivalent value: `classic` | 
| | <pre>mod=large</pre> | Equivalent value: `stickerless` | 
| | <pre>mod=carbon</pre> | Equivalent values: `fiber` | 
| `core` | <pre>core=</pre> | | 
| | <pre>core=black</pre> | Equivalent values: `b`, `dark` | 
| | <pre>core=white</pre> | Equivalent values: `w`, `light` | 
| `scheme` | <pre>scheme=</pre> | | 
| | <pre>scheme=western</pre> | Equivalent value: `boy`, `west` | 
| | <pre>scheme=japanese</pre> |  Equivalent value: `jap` | 
| | <pre>scheme=custom</pre> |  | 
