The `evaluate-annotations.ipynb` interactive notebook shows how you can:

1. Annotate data with an LLM in a structured way.
2. Load annotated data and normalize its structure.
3. Calculate different metrics for Inter-Annotator Agreement.

The project makes use of the `pydantic` and `instructor` libraries to define a data model for annotations and validate the LLM responses according to the model.

## Installation

To use the notebook, create a `.env` at the root of the repository and add your OpenAI API key:

``` env
OPENAI_API_KEY=<YOUR_OPENAI_KEY>
```

The installation of the required Python packages is managed from the `evaluate-annotations.ipynb` notebook.
