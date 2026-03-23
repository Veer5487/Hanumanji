🐢 SVG-to-Turtle Sketcher
An automated sketching engine that converts SVG path data into real-time Turtle graphics animations.

🚀 Features
Path Parsing: Extracts complex vector paths using svgpathtools.

Auto-Coloring: Custom HEX-to-RGB conversion to maintain the original SVG color palette.

Progress Tracking: Integrated tqdm progress bars for handling large SVG files.

Dynamic Scaling: Configurable scale and offset parameters to fit any screen resolution.

📦 Prerequisites
You will need Python 3.x and the following libraries:

Bash
pip install svgpathtools tqdm
⚙️ How It Works
Load: The load_svg method reads the .svg file and extracts dimensions and path attributes.

Translate: It converts SVG coordinates into Cartesian coordinates suitable for the Turtle screen.

Render: The draw method iterates through the coordinates, applying begin_fill() and end_fill() to recreate the vector shapes.

💻 Usage
Place your .svg file in the project directory and update the path in the script:

Python
# Initialize the sketcher
# scale: Adjusts size | x_offset/y_offset: Centers the drawing
pen = sketch_from_svg("your_file.svg", scale=70, x_offset=350, y_offset=350)

# Execute the drawing
pen.draw()
🛠 Tech Stack
Language: Python

Graphics: Turtle (Standard Library)

Libraries: svgpathtools (Path extraction), tqdm (Progress visualizer), os (Path management)
