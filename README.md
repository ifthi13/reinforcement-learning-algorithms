Reinforcement Learning Visualizer Suite
This project is a single-file, interactive web application designed to provide an intuitive, visual understanding of several fundamental Reinforcement Learning (RL) algorithms. It's a hands-on educational tool that allows users to see how different algorithms learn and behave in simple grid-world environments.
The entire application is self-contained in a single HTML file (Reinforcement_Learning_Suite.html), requiring no build steps, dependencies, or server setup.
Features
All-in-One Suite: Combines five key RL algorithm visualizations into a single, cohesive application.
Tabbed Navigation: Easily switch between different algorithms using a clean, sticky navigation bar.
Fully Interactive: Tweak parameters like learning rate and exploration rate to see their effects in real-time.
Mobile Responsive: The layout is designed to work seamlessly on both desktop and mobile browsers.
Accessible Explanations: Each module includes a clear, concise explanation of how the algorithm works.
Text-to-Speech: An integrated "Listen to Explanation" feature uses the Web Speech API to read descriptions aloud, enhancing accessibility.
Zero Dependencies: The entire project is written in vanilla HTML, CSS, and JavaScript. No libraries or frameworks are needed.
Algorithms Visualized
The suite includes interactive modules for the following algorithms:
1. Monte Carlo (MC) Methods
Concept: Learning from the final outcome of a complete episode.
Visualization: An interactive simulation of estimating the value of Pi (π) by randomly dropping dots. This demonstrates the core idea of using random sampling to approximate a value.
2. Temporal-Difference (TD) Learning
Concept: Learning from every single step without waiting for the final outcome (bootstrapping).
Visualization: An agent learns the "value" of each state in a grid world. Users can directly compare the step-by-step learning of TD against the episode-by-episode learning of Monte Carlo.
3. Q-Learning
Concept: An off-policy algorithm that learns the value of taking a specific action in each state to find the optimal policy.
Visualization: An agent learns a Q-table to navigate a grid world. The display shows the learned optimal path (policy) as arrows, demonstrating how the agent finds the shortest route to the goal.
4. SARSA (vs. Q-Learning)
Concept: An on-policy algorithm that learns based on the actions it actually takes, including exploratory moves.
Visualization: The classic "Cliff Walking" problem is used to highlight the difference between on-policy (SARSA) and off-policy (Q-Learning). Users can see how SARSA learns a "safer" but longer path, while Q-Learning learns the "optimal" but riskier path along the cliff edge.
5. Deep Q-Networks (DQN vs. Double DQN)
Concept: Using neural networks (simulated here with tables) to handle complex problems, enhanced with Experience Replay and a Target Network.
Visualization: A three-panel layout shows the Environment, the Experience Replay Memory, and the Learning Networks. A pop-up calculation box explicitly shows the mathematical difference between how Standard DQN and Double DQN learn, making the concept of "decoupling action selection from evaluation" easy to understand.
How to Run
No installation is required. Simply follow these steps:
Download the Reinforcement_Learning_Suite.html file.
Open the file in any modern web browser (e.g., Google Chrome, Mozilla Firefox, Microsoft Edge, Safari).
Use the navigation bar at the top to select the algorithm you wish to explore.
File Structure
The entire project is self-contained within Reinforcement_Learning_Suite.html.
<head> section: Contains all the necessary CSS for styling and layout. Styles are carefully scoped to apply to the correct modules.
<body> section:
A <nav> element for the tabbed navigation.
A <section> for each algorithm, which acts as a "page". Only the active page is displayed.
Each section contains the HTML structure for its visualization, controls, and explanation.
<script> section (at the end of <body>):
Global Logic: Handles the navigation, tab switching, and the Web Speech API for voice features. It also includes a mechanism to automatically pause simulations when switching tabs.
Scoped Algorithm Logic: The JavaScript for each of the five visualizations is wrapped in its own (() => { ... })(); block. This Immediately Invoked Function Expression (IIFE) isolates the variables and functions for each module, preventing any conflicts between them.
