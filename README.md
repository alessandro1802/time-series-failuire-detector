# Time-series failure classification and localization

## Data

- Synthetically generated *50 000* examples of various length (50 - 60) sequences of 3 sensors on a factory and *5 classes* of defects (Boolean: occurred or not). 

- There is no information where and on which sensor(s) a defect appeared.

## Models

- For both classification of a given sequence and defect localization *Recurrent Neural Networks* were used. The detailed description of the architectures are provided.

- The advantage of knowing how the data was generated is **not** taken. Hence, the approach is suitable for any data, of course, after re-training.

## Set-up

1.  After cloning the repository, create a `Python 3.8` virtual environment inside it:
   
```bash
python3.8 -m venv venv
```
   
2. Activate it (depending on your OS) e.g.
   
```bash
source venv/bin/activate
```

3. Install the libraries:
   
```bash
pip install -r requirements.txt
```

## File-structure

- In `dataGeneration` notebook there are plots of the data examples as well as saving it into files.

- `data` folder contains the serialized raw generated data.

- `detection` notebook is the core of this project, it's the detailed step-by-step explanation of the data preprocessing, model architectures (layer structure, metric and loss function selection), training and output interpretation.
