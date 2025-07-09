# Two Dice Detection Game with YOLOv8 and Tkinter

This project combines YOLOv8 object detection with a Python-based GUI to detect two dice in an image, display their values, and compute a game score. The game ends if both dice show the same number.

## Project Overview

- Trained a custom YOLOv8 model to detect dice faces (1–6)
- Built a Tkinter-based GUI for users to load images and play the "two dice game"
- Detection logic selects the two largest dice and calculates score based on face values
- Automatically ends the game when both dice show the same number

## How It Works

1. **User loads an image** containing multiple dices
2. YOLOv8 detects only 2 dices, creates a boundary around those and predicts their face values (1–6)
3. The app displays the image with bounding boxes and values
4. If the two dice match, the game ends; otherwise, the score is updated

## YOLOv8 Training Results

- **Epochs**: 50  
- **mAP@0.5**: 94.5%  
- **Classes**: Dice face values 1 to 6  
- **Best Model Path**: `runs/detect/train6/weights/best.pt`

## GUI Demo

![GUI Screenshot](https://github.com/IffaKashif/two-dice-game-yolo/blob/main/yolo_diceDetection_gui.png)

## Folder Structure

- 'dice_game.py': Main application script
- 'data.yaml','test.zip','train.zip': Training dataset and labels
- 'best.pt': YOLO training logs and best model
- `yolo_diceDetection_gui.png`: App preview

## Requirements

- `ultralytics`
- `opencv-python`
- `numpy`
- `pillow`
- `tkinter` (standard in most Python installations)

Install with:

```bash
pip install ultralytics opencv-python pillow numpy
