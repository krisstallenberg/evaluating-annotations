
This repository contains a project to annotate linguistic data (understatements) using a Language Model (LLM), as well as to evaluate the quality of the annotations and compare them to human annotations for Inter-Annotator Agreement. Finally, the project allows you to create a linguistic dataset of the annotated samples and metadata.

The project uses some of the following libraries:

- [`openai`](https://pypi.org/project/openai/) to interact with the OpenAI API.
- [`pydantic`](https://pypi.org/project/pydantic/) to define a data model for annotations.
- [`instructor`](https://pypi.org/project/instructor/) to validate the LLM responses according to the model.

The annotation guidelines used in this project are included in the repository at `datasets/Annotation-guidelines.pdf`.

## Usage

The `evaluate-annotations.ipynb` interactive notebook shows how you can:

1. Annotate data with an LLM, in a structured way.
2. Load human-annotated data and normalize their structure.
3. Calculate different metrics for Inter-Annotator Agreement.
4. Create a JSON dataset with annotated samples and metadata.

## Installation

To use the notebook, create a `.env` at the root of the repository and add your OpenAI API key:

``` env
OPENAI_API_KEY=<YOUR_OPENAI_KEY>
```

The installation of the required Python packages is managed from the `evaluate-annotations.ipynb` notebook.

## Suggestions for future work

- Create JSON lines datasets with the annotated samples for fine-tuning a LLM.
- Pass the annotation guidelines to the LLM as system message and compare agreement between average human annotators and the LLM.
- Use the LLM to generate new samples and evaluate them with the human annotators.
