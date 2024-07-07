# Nexa_RoomComplexityModel
## Room Complexity Measurement
This project aims to measure the complexity of a room using three methods: area-based complexity, entropy-based complexity, and visual clutter. These scores are combined using a fuzzy logic approach to determine the overall complexity score and level.

### Features
Area-Based Complexity: Measures the ratio of object area to the total room area.
Entropy-Based Complexity: Calculates the entropy of marked objects to measure randomness and disorder.
Visual Clutter: Assesses the overlap and density of objects in the room.
Fuzzy Logic Integration: Combines the three complexity scores to produce an overall complexity score and level.

### Prerequisites
Python 3.x
OpenCV
NumPy
Matplotlib
Pillow
SciPy
scikit-fuzzy

### Installation
1. Clone the repository:

git clone https://github.com/thilinapremachandra/Nexa_RoomComplexityModel.git

cd Nexa_RoomComplexityModel

2. Install the required packages:

pip install -r requirements.txt

### Usage

#### Mark Objects in the Image
Load an image:

image_path = "path_to_your_image.jpg"

The user will be prompted to mark objects in the image by clicking on the vertices of a polygon around each object. Right-click to close the polygon, press 'Enter' to finish marking an object, and 'Esc' to finish marking all objects.

#### Calculate Complexity Scores
The program calculates three complexity scores:

Area-Based Complexity Score: Calculates the ratio of the object area to the total room area.

Entropy-Based Complexity Score: Computes the entropy of marked objects to measure randomness and disorder.

Visual Clutter Score: Measures the overlap and density of objects in the room.

#### Fuzzy Logic Integration
The three complexity scores are combined using a fuzzy logic approach to produce an overall complexity score and level (Low or High).

#### Run the Program
To run the program, execute:

python main.py

#### Example Output

Area-Based Complexity Score: 0.25

Entropy-Based Complexity Score: 0.65

Clutter Score: 0.45

Final Complexity Score: 0.58, Complexity Level: High

#### Functions
display_image(title, image)

Displays an image using Matplotlib.

resize_image(image, max_width=800, max_height=600)

Resizes the image to fit within the specified dimensions.

user_mark_objects(image)
Allows the user to mark objects in the image and returns the regions of interest (ROIs).

calculate_area_based_complexity_score(rois, room_width, room_height, image)
Calculates the area-based complexity score.

load_image(image_path)
Loads and converts an image to grayscale.

calculate_entropy(image_array)
Calculates the entropy of an image array.

normalize_entropy(entropy_value)
Normalizes the entropy value.

calculate_entropy_based_complexity_score(image, rois)
Calculates the entropy-based complexity score.

calculate_visual_clutter_score(rois, image_shape)
Calculates the visual clutter score.


### Acknowledgements
This project uses the following libraries:

OpenCV

NumPy

Matplotlib

Pillow

SciPy

scikit-fuzzy

#### Contributing
Contributions are welcome! Please open an issue or submit a pull request.
