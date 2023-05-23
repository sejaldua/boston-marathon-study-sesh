# boston-marathon-study-sesh

Medium article: https://towardsdatascience.com/running-with-pandas-ai-an-exploration-of-the-boston-marathon-ad9516b34d8a

## Setup instructions

Step 1: Create your Open AI developer API key from [here](https://platform.openai.com/account/api-keys)

Step 2: Copy your API key to your clipboard

Step 3: In a terminal window, run `export OPEN_AI_KEY={insert key}`

Step 4: Paste this code into a Jupyter notebook:

```python
import pandas as pd
from pandasai import PandasAI
from pandasai.llm.openai import OpenAI
import matplotlib.pyplot as plt
from dotenv import load_dotenv
load_dotenv()
import os

# Instantiate a LLM
llm = OpenAI(api_token=os.environ.get('OPENAI_KEY'))
pandas_ai = PandasAI(llm, conversational=True)
```

