
This repository contains a project to annotate linguistic data (understatements) using a Language Model (LLM), as well as to evaluate the quality of the annotations and compare them to human annotations for Inter-Annotator Agreement. Finally, the project allows you to create a linguistic dataset of the annotated samples and metadata. The final dataset of understatements is also [available on Kaggle](https://www.kaggle.com/datasets/kstallz/thisbuta/data).

The project uses some of the following libraries:

- [`openai`](https://pypi.org/project/openai/) to interact with the OpenAI API.
- [`pydantic`](https://pypi.org/project/pydantic/) to define a data model for annotations.
- [`instructor`](https://pypi.org/project/instructor/) to validate the LLM responses according to the model.

The annotation guidelines used in this project are included [in the repository](datasets/Annotation-guidelines.pdf).

## Usage

The code for this project is organized in a tutorial-style interactive Python notebook, named [`evaluate-annotations.ipynb`](evaluate-annotations.ipynb). 

The notebook shows how you can:

1. Annotate data with an LLM, in a structured way.
2. Load human-annotated data and normalize their structure.
3. Calculate different metrics for Inter-Annotator Agreement.
4. Create a JSON dataset with annotated samples and metadata.

## Installation

To use the notebook, create an `.env` file at the root of the repository and add your OpenAI API key:

``` env
OPENAI_API_KEY=<YOUR_OPENAI_KEY>
```

The installation of the required Python packages is managed by the `evaluate-annotations.ipynb` notebook. After you add your `.env` file, you should be able to run all cells in the notebook sequentially. 

**Note**: running all cells in the notebook will make API calls to OpenAI, meaning **you will incur a cost**. For this reason, you can find a LLM-annotated dataset, which you can load from file. The code showing you how is in the notebook, under Part 1 — Step 6. 

## Suggestions for future work

- Create JSON lines datasets with the annotated samples for fine-tuning a LLM.
- Pass the annotation guidelines to the LLM as system message and compare agreement between average human annotators and the LLM.
- Use the LLM to generate new samples and evaluate them with the human annotators.
