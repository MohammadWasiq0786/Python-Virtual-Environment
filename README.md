# Create Conda Virtual Environment (`myvenv`)

```bash
conda create -p <myvenv> python=3.12 -y
```

### Activate Conda myvenv
```bash
conda activate <myvenv>
```

### Conda myvenv deactivate
```bash
conda deactivate
```

### Conda List
```bash
conda env list
```

### Remove Conda myvenv

```bash
conda env remove -p <myvenv> -y
```

# Create Python Virtual Environment (`myvenv`)

```bash
python3 -m venv <myvenv>
```

### Activate Python venv

```bash
source <myvenv>//bin/activate  # For Linux/Mac
```

```bash
<myvenv>\Scripts\activate     # For Windows
```

### Deactivate Python myvenv
```bash
deactivate
``` 

### Install `requirements.txt`

```bash
pip install -r requirements.txt
```

### Save all install libraries

```bash
pip freeze > requirements.txt
```

# Create UV Virtual Environment (`myvenv`)

### Create `project.toml` File
```bash
uv init
```

### Create Virtual Environment
```bash
uv venv
```

### Create Virtual Environment for Specific Name 
```bsh
uv venv <myvenv>
```

### Create Virtual Environment for Specific Python Version
```bash
uv venv python 3.12
```

### Activate Python myvenv
```bash
# For Linux/Mac

source .venv/bin/activate

# ----- OR ----- #
source <myvenv>/bin/activate
```

```bash
# For Windows

.venv\Scripts\activate

# ----- OR ----- #
<myvenv>\Scripts\activate
```

### Install Specific Library
```bash
uv add <LibraryName>          #  Using add

# ----- OR ----- #
uv pip install <LibraryName>  # Using pip
```

#### Install Specific Library Version
```bash
uv add '<LibraryName>==2.31.0'
```

### Uninstall Specific Library
```bash
uv remove <LibraryName>
```

### Install `requirements.txt`

```bash
uv pip install -r requirements.txt  # Using pip

# ----- OR ----- #
uv add -r requirements.txt  # Using add

# ----- OR ----- #
uv add -r requirements.txt -c constraints.txt # constraints
```

### Save all install libraries

```bash
pip freeze > requirements.txt
```

### Run Python File
```bash
uv run `<FileName.py>`
```

#### Flask File
```bash
uv run -- flask run -p <PORT> # 5000
```

#### FastAPI File
```bash
uv init --app
```

```bash
uv run fastapi dev
```

#### Streamlit File
```bash
uv streamlit run app.py
```

- **`Note`**: We can also run files in their default/normal manner.

### Deactivate Python myvenv
```bash
uv deactivate

uv deactivate <myvenv>  # Specific Named myvenv
``` 

### Remove Conda myvenv

```bash
uv remove

uv remove <myvenv>  # Specific Named myvenv
```

### List All the UV Python venv
```bash
uv pip list
```
