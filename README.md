# Sorting Visualizer 


# # --> Basic: 
Description: 
            Developed an interactive Sorting Visualizer using HTML, CSS, and JavaScript to demonstrate the functionality of sorting algorithms visually and audibly.
Features:
            Implemented bubble sort algorithm with step-by-step visual representation.
            Integrated audio feedback to enhance the user experience.
            Provided controls to initialize and play the sorting process dynamically.
Technologies:
            HTML, CSS, JavaScript, Web Audio API.

# The architecture of this project:

User Interface Layer (HTML/CSS):
UI Elements: Buttons, Container for bars.
Styling: Bar colors, Layout.
Logic Layer (JavaScript):
Data Handling: Array initialization.
Sorting Logic: Bubble sort algorithm.
Animation Handling: Visual and audio feedback for sorting operations.
User Interaction: Handling button clicks to initialize and play the animation.

Start
   |
   v
User clicks "Init"
   |
   v
Initialize array with random values
   |
   v
Display bars based on array values
   |
   v
User clicks "Play"
   |
   v
Apply bubble sort algorithm
   |
   v
Animate each swap/comparison with visual and audio feedback
   |
   v
Continue until array is sorted
   |
   v
Display final sorted bars
   |
   v
End

# # ==> Complex: 
Description: This code enhances the Sorting Visualizer by rendering the bars using the HTML5 <canvas> element, adding more sophisticated visual and audio effects, and improving the animation of the sorting process.

# Canvas Setup:
Canvas Dimensions: The canvas is set to a width of 500 pixels and a height of 400 pixels.
Margins and Spacing: The margin around the canvas is set to 30 pixels. The bars are spaced evenly within the canvas, with the spacing calculated based on the canvas width and number of elements (n=30).
Initialization
Array Initialization: An array of random values is generated and stored in the array array. The cols array holds Column objects, each representing a bar with specific dimensions.
Column Dimensions: Each column's height is proportional to its corresponding array value, and its width is determined by the spacing.
Audio Context
Audio Generation: Audio feedback is generated using the Web Audio API. Different waveform types ("square" and "sine") are used to differentiate between swap and non-swap operations.
playNote Function: This function generates a sound for a given frequency (freq) and waveform type (type). The duration of each note is set to 0.2 seconds.
Sorting Logic
Bubble Sort Implementation: The bubbleSort function implements the bubble sort algorithm. It returns a list of moves that include the indices of elements being compared and whether a swap occurred.
Swap and Comparison Tracking: The sorting process is tracked by recording each comparison and swap. These actions are stored in the moves array.
Animation
Animation Function: The animate function is responsible for rendering the bars on the canvas and playing the sorting animation. It clears the canvas on each frame and redraws the columns.
Column Movement: If a swap occurs, the columns swap their positions on the canvas, and a sound is played. If no swap occurs, the columns "jump" to indicate a comparison.
Continuous Animation: The animation is driven by requestAnimationFrame, ensuring smooth and continuous updates.

# Key Components of the Code:
Canvas (myCanvas): The area where bars representing the array elements are drawn.
Columns (Column Class): Each bar on the canvas, representing an element in the array.
Audio (playNote): Generates sound based on the height of the columns and whether a swap occurs.
Sorting Algorithm (bubbleSort): The logic for sorting the array, which generates the moves for animation.
Animation (animate): Handles the visual updates on the canvas and synchronizes with the audio output.

# # --> Advanced:
Description: This advanced version of the Sorting Visualizer project introduces more complex animations, including a bird character that interacts with the sorting process. It also features a more sophisticated rendering of elements on the canvas, making the visualization more engaging and dynamic.

# Canvas Setup:
Canvas Dimensions: The canvas is set to a width of 500 pixels and a height of 300 pixels, providing a smaller, more compact visualization area.
Spacing and Margins: The canvas has a margin of 30 pixels, with bars (or "socks") spaced evenly within the available width. The spacing is calculated to fit 18 elements (n=18) across the canvas.

Sock Representation:
Sock Colors: The socks are colored using a predefined set of colors. Each color is paired to represent matching socks, with colors shuffled randomly to simulate an unsorted state.
Column Heights: The heights of the socks are determined by values in the array, which are scaled and randomized to create variety in the visual representation.

Bird Character:
Bird Introduction: A bird character is introduced, which moves between the socks during the sorting process. The bird adds an additional layer of animation and interaction, making the visualization more lively.

Sorting Logic:
Bubble Sort Algorithm: The project uses a bidirectional bubble sort (or cocktail shaker sort) algorithm, where the sorting passes alternate directions. This adds complexity and a unique visual pattern to the sorting process.
Moves Tracking: The algorithm tracks each comparison and swap, storing them as "moves" that are used to drive the animation.

Animation:
Bezier Curve for String: A bezier curve is drawn on the canvas to represent the string from which the socks hang. This string adds a playful, realistic touch to the visual.
Sock Animation: Each sock object (Sock class) is animated based on the sorting algorithm's moves. When a swap occurs, the socks slide to their new positions, and the bird follows the action.
Bird Movement: The bird moves between socks, either following a swap or simply observing a comparison. Its movement is smooth and timed to match the sorting process.

Physics Simulation:
Physics Engine: The project incorporates basic physics principles to simulate realistic sock and bird movements. The socks and bird respond to the forces in a visually pleasing manner, adding depth to the animation.

Timing and Synchronization:
Frame Updates: The animate function is responsible for updating the canvas frame by frame. It clears the canvas, redraws the string, updates the socks and bird, and applies any pending moves from the sorting algorithm.
Tweening: Movement between positions is smooth, using tweening (interpolating between points) over a set duration (tweenLength), enhancing the visual effect.

# Key Components of the Code:
Canvas (myCanvas): The visual area where the sorting and animations take place.
Socks (Sock Class): Represents the individual elements being sorted. They are drawn as colorful, hanging socks.
Bird (Bird Class): A character that interacts with the sorting process, moving between socks based on the sorting algorithm.
Sorting Algorithm (bubbleSort): Implements a bidirectional bubble sort to create a dynamic sorting visualization.
Animation (animate): Continuously updates the canvas, applying moves and rendering the socks and bird with smooth transitions.
