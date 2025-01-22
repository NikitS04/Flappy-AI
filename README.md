# **Flappy Bird AI with NEAT**

This project demonstrates an AI-powered Flappy Bird game where birds learn to navigate pipes using the NEAT (NeuroEvolution of Augmenting Topologies) algorithm. It includes training birds to play the game and running the best-performing bird from training.

---

## **Features**
- **Train AI**: Birds evolve through generations to learn how to avoid obstacles.
- **NEAT Algorithm**: Utilizes NEAT for evolving neural networks.
- **Visual Representation**: Watch birds learn and compete in real-time.
- **Saved Best Bird**: Replay the best-performing bird for demonstration.

---

## **Setup Instructions**

### **Prerequisites**
Ensure you have the following installed:
- Python 3.7+
- `pygame` for rendering the game.
- `neat-python` for implementing the NEAT algorithm.
- `PyQt5` (optional, only if needed for external UI).

### **Install Dependencies**
Run the following command to install dependencies:
```bash
pip install pygame neat-python
```

---

## **How to Run**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/flappy-bird-neat.git
   cd flappy-bird-neat
   ```

2. **Prepare Assets**:
   - Ensure all images (`bird1.png`, `bird2.png`, `bird3.png`, `pipe.png`, `base.png`, `bg.png`) are placed in the `imgs/` directory.

3. **Run the Game**:
   - Train new birds:
     ```bash
     python main.py
     ```
     Enter `train` when prompted to start the training process.
   - Run the best-performing bird:
     ```bash
     python main.py
     ```
     Enter `run` when prompted to see the saved bird play.

4. **Configuration**:
   - Modify the NEAT configuration file `config-feedforward.txt` to adjust NEAT parameters like population size, mutation rates, etc.

---

## **Key Components**

- **Bird Class**: Manages the bird's movement, jumping, and collision detection.
- **Pipe Class**: Handles pipe generation, movement, and collision checks.
- **Base Class**: Implements the moving base at the bottom of the screen.
- **NEAT Integration**: Uses `neat-python` to evolve neural networks for controlling birds.

---

## **How It Works**
1. **Training**:
   - Birds are controlled by neural networks.
   - NEAT evolves these networks over generations to maximize their fitness (score).
2. **Fitness Calculation**:
   - Birds earn points for surviving longer and passing through pipes.
   - Collisions or flying out of bounds reduce fitness.
3. **Replay Best Bird**:
   - After training, the best-performing bird is saved and can be replayed using the `run` option.

---

## **Configuration Details**
The `config-feedforward.txt` file includes:
- **Population Size**: Number of birds per generation.
- **Activation Function**: Determines the activation for neural networks.
- **Fitness Threshold**: Stops training when the threshold is met.

---

## **Gameplay Controls**
- No manual input is needed; the birds are controlled entirely by the neural networks.
- Use `Ctrl+C` or close the window to exit the game.

---

## **Future Enhancements**
- Add a GUI for setting configurations.
- Implement additional obstacles or game dynamics.
- Visualize neural network decisions in real-time.

---

## **Acknowledgments**
- **NEAT Algorithm**: Kenneth O. Stanley for the NEAT algorithm.
- **Pygame**: For rendering the game environment.

---

