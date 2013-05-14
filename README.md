# Double A
## A responsive tool for locating breakpoints in a stylesheet
### by Annette Arabasz ([arabasz.com](http://arabasz.com)) & Nick Snyder ([fasterhorses.co](http://fasterhorses.co))

Double A is a responsive tool for locating named breakpoints in a stylesheet. It is helpful for locating the area of your CSS issue without having to open the web inspector. 

Double A works by appending a fixed tab to the bottom of your webpage that shows both the current pixel width of the viewport and a color. The color of the tab is representative of the area where the CSS error will happen. While you can assign your own colors, we suggesting sticking with the ROYGBIV mnemonic, as it is easy to remember.

You can easily adjust the breakpoints and the colors by passing in different parameters. Please refer to the sample code below:

    $(document).ready(function() {
        $(this).doublea({
            format: 'em',
            breakpoints: [30, 40, 50, 60, 75],
            colors: ['#ffb346', '#dfdd4a', '#44ce19', '#7bb8f7', '#c17bf7']
        });
    });

* format: 'em',    // String
* * Allows you to choose whether your breakpoints will be EM or pixel-based. 
* breakpoints: [],         // Array
* * The breakpoints you'd like to test against. If in the previous parameter you chose 'em', be sure to use 30 rather than 480, for example.
* colors: [],              // Array
* * The colors for each of the corresponding breakpoints in the previous parameter. **The number of items in both breakpoints[] and colors[] should match**.

