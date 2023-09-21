# CubePal Links

### *About CubePal*

CubePal is an iOS app designed for learning algorithms and solving virtual 2x2x2, 3x3x3, 4x4x4, and 5x5x5 cubes and supercubes.

You can download the FREE CubePal app on the [App Store](https://apps.apple.com/app/cubepal/id1501885433).

For additional information, please visit the app's landing page at [www.cubepal.app](https://www.cubepal.app).

### *About Universal Links*

CubePal Links is an implemetation of the Universal Links (also referred to as App Links or Deep Links) are web URLs that, when tapped on a mobile device, seamlessly open the associated app, triggering specific actions or features defined by the link's parameters. CubePal allows users to generate, export, share, modify, and use their own Universal Links as described below.

### *Why Using CubePal Links*

CubePal Links enable users to create, store, and share custom cubes and algorithms. These links can be generated within the CubePal app or written manually and stored anywhere, including websites, other apps, or local storage. This feature simplifies the sharing of algorithms, allowing anyone to effortlessly open and learn them using virtual cubes within the CubePal app on their mobile devices.

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

Using CubePal Links is straightforward. Feel free to use CubePal Links for your personal needs or share them with others through any platform or technology of your choice.

1. **Tap the Link**: To open the CubePal app with a specific cube or algorithm, simply tap on the CubePal Link you've either created or saved on your mobile device. The app will automatically launch and open the respective cube and algorithm.

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
- Tip: Use the CubePal app to test manually created links before sharing them.

## CubePal Link Parameters

URL parameters are used to convey information to the CubePal app. These parameters are essential for showing the desired cubes and algorithms within the app.

### General Guidelines

- Add parameters after the question mark `?` without spaces:
  ```
  https://www.cubepal.app/alg?alg=R-_F_U_R
  ```
- Separate parameters using the ampersand symbol `&`:
  ```
  https://www.cubepal.app/alg?cube=4x4x4&alg=R-_F_U_R&scheme=japanese
  ```
- You can omit any parameter except the algorithm sequence.
- The algorithm sequence should contain at least two turns or moves.
- While the order of the parameters can be changed, for the sake of consistency, it is recommended to use the order outlined in the table below.
- Algorithms turns should be separated by underscores `_` (recommended for readability) or by percent-encoded spaces `%20`.
- Algorithm turns and algorithm name are the only parameters with case sensitive values.

### Parameters

|  Parameter  | Value  |  Functionality  |
|---|---|---|
| `alg` | <pre>alg=R-_F_U2_R</pre> |  Specifies a particular algorithm[^1] (sequence of cube turns) separated by underscore `_`. <br />Inverted turns `'` are represented by dash sign `-`. |
|   |   | Example: https://www.cubepal.app/alg?alg=R-_F_U2_R <br />Opens the algorithm: `R' F U2 R` |
| ` ` |  <pre>=R_U-_F_R-</pre> | Empty parameter has the same funtionality as `alg`. <br />The parameter's name can be omitted only when the sequence is an algorithm. |
|   |   | Example: https://www.cubepal.app/alg?=R_U-_F_R- <br />Opens the algorithm: `R U' F R'` |
| `scr` |  <pre>scr=R-_F_U_R</pre> |  Specifies a particular cube scramble.[^2]|
|   |   | Example: https://www.cubepal.app/alg?scr=R-_F_U_R <br />Opens the cube in its scrambled state using the `R U' F R'` scramble. |
| `rec` |  <pre>rec=R-_F_U_R</pre>  |  Specifies a particular cube reconstruction[^3]. |
|   |   | Example: https://www.cubepal.app/alg?rec=R-_F_U_R <br />Opens the reconstructed cube using the `R U' F R'` sequence. |
| `pat` |  <pre>pat=E_S-_E-_S</pre>  |  Specifies a particular cube pretty pattern[^4]. |
|   |   | Example: https://www.cubepal.app/alg?pat=E_S-_E-_S <br />Opens the cube pattern using the `E S' E' S` sequence. |
| `cube` |  <pre>cube=</pre>   |  Specifies a particular cube size (dimension). <br />Both parameter and its value are optional. Default cube size: `3x3x3`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube= <br /> Example 2: https://www.cubepal.app/alg?=R-_F_U_R<br />Both examples open the `R U' F R'` algorithm with a `3x3x3` cube. |
|   |  <pre>cube=2x2x2</pre>  |  Specifies a 2x2x2 cube. <br />Equivalent values: `2`, `2x2`, `pocket`, `mini`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube=2x2x2 <br />Example 2: https://www.cubepal.app/alg?=R-_F_U_R&cube=mini <br />Both examples open the `R U' F R'` algorithm with a `2x2x2` cube. |
|   |  <pre>cube=3x3x3</pre>  |  Specifies a 3x3x3 cube. Parameter and value are optional for 3x3x3 cube. <br />Equivalent values: `3`, `3x3`, `rubik`, `magic`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube=3x3x3 <br />Example 2: https://www.cubepal.app/alg?=R-_F_U_R <br />Both examples open the `R U' F R'` algorithm with a `3x3x3` cube. |
|   |  <pre>cube=4x4x4</pre>  |  Specifies a 4x4x4 cube. <br />Equivalent values: `4`, `4x4`, `revenge`, `master`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube=4x4x4<br />Example 2: https://www.cubepal.app/alg?=R-_F_U_R&cube=revenge <br />Both examples open the `R U' F R'` algorithm with a `4x4x4` cube. |
|   |  <pre>cube=5x5x5</pre>  |  Specifies a 5x5x5 cube. <br />Equivalent values: `5`, `5x5`, `professors`, `professor`. |
|   |   | Example 1: https://www.cubepal.app/alg?=R-_F_U_R&cube=2x2x2<br />Example 2: https://www.cubepal.app/alg?=R-_F_U_R&cube=5<br />Both examples open the `R U' F R'` algorithm with a `5x5x5` cube. |
| `name` |  <pre>name=T_Perm</pre> | Specifies the name of the algorithm. <br />Algorithm name words should be separated by underscore `_` |
| | | Example 1: https://www.cubepal.app/alg?pat=M2_E2_S2&name=Checkerboard <br />Opens the cube with the checkerboard pattern using the `M2 E2 S2` sequence<br />Example 2: https://www.cubepal.app/alg?=R_U_R-_U-_R-_F_R2_U-_R-_U-_R_U_R-_F-&name=T_Perm <br /> Opens the T Perm algorithm `R U R' U' R' F R2 U' R' U' R U R' F'` |
| `super` |  <pre>super=</pre> | Specifies the type of supercube[^5]. <br />Default supercube: `arrows` - a supercube with arrow stickers. <br />Note: If `super` parameter is omited, a default cube (not supercube) is shown. |
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&super= <br />Opens a default supercube with arrow stickers. |
| | <pre>super=none</pre> | Specifies a classic cube - not a supercube. <br />Equivalent values: `classic`, `standard`, `regular` |
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&super=none<br />Opens the algorithm and a classic cube. |
| | <pre>super=arrows</pre> | Specifies a supercube with arrow stickers. <br />Equivalent values: `arrow`, `arr`, `shepherd` |
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&super=arrows<br />Opens the algorithm and a supercube with arrow stickers. |
| | <pre>super=arrowheads</pre> | Specifies a supercube with arrowhead stickers. <br/>Equivalent value: `arrowhead` |
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&super=arrowheads<br />Opens the algorithm and a supercube with arrowhead stickers. |
| | <pre>super=triangles</pre> | Specifies a supercube with triangle stickers. <br/>Equivalent values: `triangle`, `triangular` |
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&super=triangles<br />Opens the algorithm and a supercube with triangle stickers. |
| | <pre>super=hint</pre> | Specifies a supercube with hint stickers. <br/>Equivalent values: `hints`, `pochmann`, `poch` |
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&super=hint<br />Opens the algorithm and a supercube with hint stickers. |
| `mod` | <pre>mod=</pre> | Specifies the cube stickers mod. <br />Default mod: `small`. | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&mod=<br />Parameter is ignored and opens a cube with default small rounded stickers. |
| | <pre>mod=small</pre> | Specifies a mod with small classic stickers. <br/>Equivalent value: `classic`, `standard`, `regular` | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&mod=small<br />Opens the algorithm and a cube with small rounded stickers. |
| | <pre>mod=large</pre> | Specifies a mod with large borderless stickers. <br/>Equivalent value: `stickerless`, `borderless` | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&mod=large<br />Opens the algorithm and a cube with large borderless stickers. |
| | <pre>mod=carbon</pre> | Specifies a mod with carbon stickers. | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&mod=carbon<br />Opens the algorithm and a cube with carbon rounded stickers. |
| `core` | <pre>core=</pre> | Specifies the cube core or body color or material. <br />Default core: `black`. |
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&core=<br />Paramater with empty value is ignored, and opens a cube with a default black core. |
| | <pre>core=black</pre> | Specifies a black or dark core. <br />Equivalent values: `b`, `dark` | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&core=black<br />Opens the algorithm and a cube with black core. |
| | <pre>core=white</pre> | Specifies a white or light core. <br />Equivalent values: `w`, `light` | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&core=white<br />Opens the algorithm and a cube with white core. |
| `scheme` | <pre>scheme=</pre> | Specifies the color scheme of the cube. <br />Default scheme: `western`. | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&scheme=<br />Paramater with empty value is ignored, and opens a cube with a western color scheme. |
| | <pre>scheme=western</pre> | Specifies the western or BOY color scheme (Blue-Green, Orange-Red, Yellow-White color pairs for opposite cube faces). <br />Equivalent value: `boy`, `west` | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&scheme=western<br />Opens the algorithm and a cube with a western color scheme. |
| | <pre>scheme=japanese</pre> | Specifies the Japanese color scheme (Yellow-Green, Orange-Red, Blue-White color pairs for opposite cube faces). <br />Equivalent value: `jap`, `jpn` | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&scheme=japanese<br />Opens the algorithm and a cube with a japanese color scheme. |
| | <pre>scheme=custom</pre> | Specifies the custom color scheme as defined by the user. | 
|   |   | Example: https://www.cubepal.app/alg?=R-_F_U_R&scheme=custom<br />Opens the algorithm and a cube with a custom color scheme. |

## CubePal App Versions

CubePal's functionality and parameters vary depending on the app version you are using:

- **Free Version:** All features and parameters mentioned in this documentation are fully available for the 3x3x3 cube. For other cube sizes, please consider upgrading to the Pro Version of the app. You can download the FREE CubePal app on the [App Store](https://apps.apple.com/app/cubepal/id1501885433).

- **Pro Version:** The Ads Free Pro Version extends CubePal's unlimited capabilities to all cubes. If you wish to explore more and beyond the 3x3x3 cube, we recommend upgrading to the Pro Version of the app.

## Legal Note

CubePal Links are distributed under MIT License, which grants users the freedom to create, use and distribute them without any restrictions.

---------
Notes:
[^1]: `Algorithm` is a pre-established sequence of cube turns or moves designed to transform a scrambled or unsolved cube into the solved state. Algorithm sequence starts from the unsolved state of the cube.
[^2]: `Scramble` is a sequence of cube turns or moves applied to a solved cube creating a randomly shuffled arrangement of its pieces, usually used for solving competitions. Scramble sequence starts from the solved state of the cube.
[^3]: `Reconstruction` is a sequence of cube turns or moves that represents a detailed record of the exact turns applied by someone to the cube, from its initial scrambled state to its final solved state. Reconstruction sequence starts from the unsolved state of the cube.
[^4]: `Pattern` is a sequence of cube turns or moves applied to a solved cube, resulting in a visually appealing and/or symmetric arrangement of colors or stickers on its faces used for artistic and aesthetic purposes. Pattern sequence starts from the solved state of the cube.
[^5]: `Supercube` is a modified version of a standard cube where the additional challenge lies in the requirement to also solve/align the centerpieces, making it more difficult to solve than a regular cube.
