# CNN Challenge: Small Image Dataset Classification

## ITCS 6169 – Assignment 2
This project explores how different attention methods perform in self-supervised learning. The experiments are based on the DINO (self-**DI**stillation with **NO** labels) framework using Vision Transformers (ViTs). They cover standard DINO and three sparse attention patterns: random, window, and dilated.

Fibottention [1] was also included, to test how a structured form of sparse attention performs on a small dataset.

## Setup

```bash
cd Assignment2_SSL
python3 -m venv venv
source venv/bin/activate        
pip install -r requirements.txt
```

## Running

Open a notebook and run all cells:
   - `dino_test.ipynb` → DINO
   - `Dino/fib_dino.ipynb` → Fib-DINO
   - `Dino/sparse_dino.ipynb` → Sparse variants + comparison (run the other two first if you want them in the plot)

Each notebook trains the model, saves the teacher weights to `Models/`, runs k-NN evaluation
Individual settings can be overridden without editing a file:

Use the headers provided at the top of each notebook if running in Google Colab and make sure to first download the Assignment2_SSL in a google Drive folder.

**Note:** The notebooks use relative paths (`data/train`, `data/test`, `Models/`). If you get a "file not found" error, update those paths to match where you launched Jupyter from.

## Evaluation

The models are saved in the  

## Final Results Can Be Found at the Bottom of ITCS_6169_8169_Assignment1_2026_Starter.ipynb
Run test.ipynb in CNN to see every model tested.

## Evaluation

All trained models are saved in the `Models` folder and can be compared in `evaluate.ipynb`.

*Note: `evaluate.ipynb` is not implemented yet.*

## References

[1] Rahimian, A. K., Govind, M. K., Maity, S., Reilly, D., Kümmerle, C., Das, S., & Dutta, A. (2024). *Fibottention: Inceptive visual representation learning with diverse attention across heads.* arXiv preprint arXiv:2406.19391.