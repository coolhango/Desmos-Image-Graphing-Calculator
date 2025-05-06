# Desmosify: A Desmos Image Graphing Calculator
Desmosify is a Python-powered tool that intelligently transforms raster images into mathematically expressive plots within the Desmos Graphing Calculator. By analyzing visual content—such as line drawings, handwritten figures, or stylized diagrams—the tool converts contours into mathematical expressions including Bézier-like curves, vertical and oblique lines, all equipped with appropriate domain constraints.

It empowers users to generate Desmos-compatible algebraic visualizations from real-world sketches or digital art. The final result is a plain-text file of equations, ready to be pasted into Desmos for a faithful, math-based rendering of the original image. Whether you're an educator, student, or a mathematically curious artist, Desmosify bridges image processing and algebra in a novel and interactive way.

![image](https://github.com/user-attachments/assets/db09ca0b-8887-4b25-8753-52c2f4de225a)

__________________________
How It Works
1. Desmosify operates through a combination of computer vision and geometric approximation. The workflow starts with edge detection via OpenCV’s Canny algorithm, isolating the most prominent lines and features in the image. It then simplifies these contours with a configurable approximation parameter, effectively reducing noise while maintaining essential structure. From there, it categorizes each segment as either a line or curve and generates a corresponding mathematical expression, formatted for Desmos and constrained to its original bounds.
2. This process makes it easy to represent art, annotations, or schematics as a clean, code-driven plot in a Cartesian system. For best results, the source image should be a high-contrast, black-and-white drawing or logo with minimal noise.

<img width="299" alt="Screenshot 2025-05-06 at 11 47 19" src="https://github.com/user-attachments/assets/cbf2773b-3c05-473d-bbbd-40f04c7b7883" />
<img width="178" alt="Screenshot 2025-05-06 at 11 47 30" src="https://github.com/user-attachments/assets/3af27342-2dde-4543-9be7-5e148287b3f9" />

__________________________

(Setup Instructions) To use Desmosify, follow these steps:
1. Install Python: Ensure Python 3.x is installed on your machine. You can download it from python.org.
2. Install Dependencies: Open a terminal or command prompt and run:
    pip install opencv-python numpy
3. Prepare Your Image:
    Place a black-and-white line drawing (e.g., Hello.png) on your Desktop.
    Modify the image path in the script if you’re using a different name or location.
4. Run the Script:
    Execute the Python script (python desmosify.py) using your terminal or preferred IDE.
    The program will then process the image and create a file called equations.txt in your Downloads folder.
5. Paste Into Desmos:
`  Open the file, copy the contents, and paste them into the Desmos Graphing Calculator.
    Your image will now appear in equation form after a while.

(Customization Options) Desmosify includes configurable parameters that allow you to adjust output fidelity and control complexity, such as:

INACCURACY_VALUE: 
This parameter determines how simplified or detailed the final equations will be.
1. Smaller values retain more curve detail but generate more expressions.
2. Larger values simplify the curves and reduce the number of equations.

Y-Axis Flipping: 
1, Desmosify automatically flips the y-axis to match Desmos' Cartesian layout.

Contour Filtering:
1. Internally, the script filters and prioritizes contours by complexity and hierarchy to preserve structural integrity.

(Ideal Use Cases) Desmosify is well-suited for a variety of applications:
1. Mathematics Education: Teachers can turn student sketches or teaching materials into live graphing visuals.
2. Student Projects: Great for coding competitions, design-based math challenges, and computational art showcases.
3. Art-Tech Explorations: Artists and designers can explore generative design by translating sketches into plotted equations.

(Limitations) While Desmosify is powerful, it’s best used under the following constraints:
1. Works best with clean, black-and-white images.
2. Not ideal for color images or photographs.
3. Complex shapes may require fine-tuning of the INACCURACY_VALUE to balance performance and precision.
4. Complex images might make the equation file too large to be saved on desmos. The image below is one ideal image to use "Desmosify" in. 

![image](https://github.com/user-attachments/assets/dc6b27b2-831f-48b5-89cf-17553d40a4c8)

__________________________________
![image](https://github.com/user-attachments/assets/dc982fab-30bb-4b4b-853b-19e30bb652fe)

Disclaimer:
This script is intended solely for educational purposes and must be used responsibly. It is strictly prohibited to use the script for pranks, harassment, or to send unsolicited emails to individuals or organizations without their consent. Any misuse of this script may result in legal consequences and violations of the terms of service of email providers, such as Gmail. Engaging in spamming or any other non-consensual activities can lead to account suspensions, blacklisting, or more severe legal actions. It is imperative to ensure that all activities conducted with this script adhere to ethical standards and comply with applicable laws and regulations. This repository and its contents are provided to demonstrate the principles of email flooding and payload delivery systems within controlled, ethical testing environments. The use of this script on live targets or for malicious purposes is strictly prohibited. Users assume full responsibility for any consequences resulting from the use of this script.

__________________________________
Built for intense stress testing, spam modeling, phishing sim payloads, or mass mail campaigns.

Author: Gedeon Koh
Copyright © 2025
All rights reserved.

Contributions ✨: We welcome contributions to improve the functionality and usability of this script. If you have identified bugs, security improvements, or new features, feel free to fork the repository and submit a pull request. Please ensure that all contributions follow ethical guidelines and are in line with the educational nature of the project. If you're unsure about any changes, please open an issue to discuss it first. Contributions should adhere to coding standards and include appropriate documentation for any new features or changes.

Other Random Information: No part of this publication may be reproduced, distributed, or transmitted in any form or by any means, including photocopying, recording, or other electronic or mechanical methods, without the prior written permission of the publisher, except in the case of brief quotations embodied in reviews and certain other non-commercial uses permitted by copyright law. THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHOR OR COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE Any unauthorized use or dissemination of the results produced by this program is unethical and may result in legal consequences. Any damage, disciplinary actions or death from this material is not in fault in the publisher's or owner.

