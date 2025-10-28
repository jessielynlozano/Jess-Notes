```python

Last login: Tue Oct 28 11:13:05 on console
annejessielynlozano@Annes-MacBook-Air ~ % jupyter --version

zsh: command not found: jupyter
annejessielynlozano@Annes-MacBook-Air ~ % pip install jupyter

zsh: command not found: pip
annejessielynlozano@Annes-MacBook-Air ~ % python --version

zsh: command not found: python
annejessielynlozano@Annes-MacBook-Air ~ % python3 --version

Python 3.14.0
annejessielynlozano@Annes-MacBook-Air ~ % python -m venv --help

zsh: command not found: python
annejessielynlozano@Annes-MacBook-Air ~ % python3 -m venv --help

usage: python3 -m venv [-h] [--system-site-packages] [--symlinks | --copies]
                       [--clear] [--upgrade] [--without-pip] [--prompt PROMPT]
                       [--upgrade-deps] [--without-scm-ignore-files]
                       ENV_DIR [ENV_DIR ...]

Creates virtual Python environments in one or more target directories.

positional arguments:
  ENV_DIR               A directory to create the environment in.

options:
  -h, --help            show this help message and exit
  --system-site-packages
                        Give the virtual environment access to the system
                        site-packages dir.
  --symlinks            Try to use symlinks rather than copies, when symlinks
                        are not the default for the platform.
  --copies              Try to use copies rather than symlinks, even when
                        symlinks are the default for the platform.
  --clear               Delete the contents of the environment directory if it
                        already exists, before environment creation.
  --upgrade             Upgrade the environment directory to use this version
                        of Python, assuming Python has been upgraded in-place.
  --without-pip         Skips installing or upgrading pip in the virtual
                        environment (pip is bootstrapped by default)
  --prompt PROMPT       Provides an alternative prompt prefix for this
                        environment.
  --upgrade-deps        Upgrade core dependencies (pip) to the latest version
                        in PyPI
  --without-scm-ignore-files
                        Skips adding SCM ignore files to the environment
                        directory (Git is supported by default).

Once an environment has been created, you may wish to activate it, e.g. by
sourcing an activate script in its bin directory.
annejessielynlozano@Annes-MacBook-Air ~ % cd ~/Downloads

annejessielynlozano@Annes-MacBook-Air Downloads % mkdir my_notebook_project
cd my_notebook_project

annejessielynlozano@Annes-MacBook-Air my_notebook_project % python3 -m venv venv 

annejessielynlozano@Annes-MacBook-Air my_notebook_project % source venv/bin/activate

(venv) annejessielynlozano@Annes-MacBook-Air my_notebook_project % pip install jupyter

Collecting jupyter
  Downloading jupyter-1.1.1-py2.py3-none-any.whl.metadata (2.0 kB)
Collecting notebook (from jupyter)
  Downloading notebook-7.4.7-py3-none-any.whl.metadata (10 kB)
Collecting jupyter-console (from jupyter)
  Downloading jupyter_console-6.6.3-py3-none-any.whl.metadata (5.8 kB)
Collecting nbconvert (from jupyter)
  Downloading nbconvert-7.16.6-py3-none-any.whl.metadata (8.5 kB)
Collecting ipykernel (from jupyter)
  Downloading ipykernel-7.1.0-py3-none-any.whl.metadata (4.5 kB)
Collecting ipywidgets (from jupyter)
  Downloading ipywidgets-8.1.7-py3-none-any.whl.metadata (2.4 kB)
Collecting jupyterlab (from jupyter)
  Downloading jupyterlab-4.4.10-py3-none-any.whl.metadata (16 kB)
Collecting appnope>=0.1.2 (from ipykernel->jupyter)
  Downloading appnope-0.1.4-py2.py3-none-any.whl.metadata (908 bytes)
Collecting comm>=0.1.1 (from ipykernel->jupyter)
  Downloading comm-0.2.3-py3-none-any.whl.metadata (3.7 kB)
Collecting debugpy>=1.6.5 (from ipykernel->jupyter)
  Downloading debugpy-1.8.17-cp314-cp314-macosx_15_0_universal2.whl.metadata (1.4 kB)
Collecting ipython>=7.23.1 (from ipykernel->jupyter)
  Downloading ipython-9.6.0-py3-none-any.whl.metadata (4.4 kB)
Collecting jupyter-client>=8.0.0 (from ipykernel->jupyter)
  Downloading jupyter_client-8.6.3-py3-none-any.whl.metadata (8.3 kB)
Collecting jupyter-core!=5.0.*,>=4.12 (from ipykernel->jupyter)
  Downloading jupyter_core-5.9.1-py3-none-any.whl.metadata (1.5 kB)
Collecting matplotlib-inline>=0.1 (from ipykernel->jupyter)
  Downloading matplotlib_inline-0.2.1-py3-none-any.whl.metadata (2.3 kB)
Collecting nest-asyncio>=1.4 (from ipykernel->jupyter)
  Downloading nest_asyncio-1.6.0-py3-none-any.whl.metadata (2.8 kB)
Collecting packaging>=22 (from ipykernel->jupyter)
  Downloading packaging-25.0-py3-none-any.whl.metadata (3.3 kB)
Collecting psutil>=5.7 (from ipykernel->jupyter)
  Downloading psutil-7.1.2-cp36-abi3-macosx_11_0_arm64.whl.metadata (23 kB)
Collecting pyzmq>=25 (from ipykernel->jupyter)
  Downloading pyzmq-27.1.0-cp312-abi3-macosx_10_15_universal2.whl.metadata (6.0 kB)
Collecting tornado>=6.2 (from ipykernel->jupyter)
  Downloading tornado-6.5.2-cp39-abi3-macosx_10_9_universal2.whl.metadata (2.8 kB)
Collecting traitlets>=5.4.0 (from ipykernel->jupyter)
  Downloading traitlets-5.14.3-py3-none-any.whl.metadata (10 kB)
Collecting decorator (from ipython>=7.23.1->ipykernel->jupyter)
  Downloading decorator-5.2.1-py3-none-any.whl.metadata (3.9 kB)
Collecting ipython-pygments-lexers (from ipython>=7.23.1->ipykernel->jupyter)
  Downloading ipython_pygments_lexers-1.1.1-py3-none-any.whl.metadata (1.1 kB)
Collecting jedi>=0.16 (from ipython>=7.23.1->ipykernel->jupyter)
  Downloading jedi-0.19.2-py2.py3-none-any.whl.metadata (22 kB)
Collecting pexpect>4.3 (from ipython>=7.23.1->ipykernel->jupyter)
  Downloading pexpect-4.9.0-py2.py3-none-any.whl.metadata (2.5 kB)
Collecting prompt_toolkit<3.1.0,>=3.0.41 (from ipython>=7.23.1->ipykernel->jupyter)
  Downloading prompt_toolkit-3.0.52-py3-none-any.whl.metadata (6.4 kB)
Collecting pygments>=2.4.0 (from ipython>=7.23.1->ipykernel->jupyter)
  Downloading pygments-2.19.2-py3-none-any.whl.metadata (2.5 kB)
Collecting stack_data (from ipython>=7.23.1->ipykernel->jupyter)
  Downloading stack_data-0.6.3-py3-none-any.whl.metadata (18 kB)
Collecting wcwidth (from prompt_toolkit<3.1.0,>=3.0.41->ipython>=7.23.1->ipykernel->jupyter)
  Downloading wcwidth-0.2.14-py2.py3-none-any.whl.metadata (15 kB)
Collecting parso<0.9.0,>=0.8.4 (from jedi>=0.16->ipython>=7.23.1->ipykernel->jupyter)
  Downloading parso-0.8.5-py2.py3-none-any.whl.metadata (8.3 kB)
Collecting python-dateutil>=2.8.2 (from jupyter-client>=8.0.0->ipykernel->jupyter)
  Downloading python_dateutil-2.9.0.post0-py2.py3-none-any.whl.metadata (8.4 kB)
Collecting platformdirs>=2.5 (from jupyter-core!=5.0.*,>=4.12->ipykernel->jupyter)
  Downloading platformdirs-4.5.0-py3-none-any.whl.metadata (12 kB)
Collecting ptyprocess>=0.5 (from pexpect>4.3->ipython>=7.23.1->ipykernel->jupyter)
  Downloading ptyprocess-0.7.0-py2.py3-none-any.whl.metadata (1.3 kB)
Collecting six>=1.5 (from python-dateutil>=2.8.2->jupyter-client>=8.0.0->ipykernel->jupyter)
  Downloading six-1.17.0-py2.py3-none-any.whl.metadata (1.7 kB)
Collecting widgetsnbextension~=4.0.14 (from ipywidgets->jupyter)
  Downloading widgetsnbextension-4.0.14-py3-none-any.whl.metadata (1.6 kB)
Collecting jupyterlab_widgets~=3.0.15 (from ipywidgets->jupyter)
  Downloading jupyterlab_widgets-3.0.15-py3-none-any.whl.metadata (20 kB)
Collecting async-lru>=1.0.0 (from jupyterlab->jupyter)
  Downloading async_lru-2.0.5-py3-none-any.whl.metadata (4.5 kB)
Collecting httpx<1,>=0.25.0 (from jupyterlab->jupyter)
  Downloading httpx-0.28.1-py3-none-any.whl.metadata (7.1 kB)
Collecting jinja2>=3.0.3 (from jupyterlab->jupyter)
  Downloading jinja2-3.1.6-py3-none-any.whl.metadata (2.9 kB)
Collecting jupyter-lsp>=2.0.0 (from jupyterlab->jupyter)
  Downloading jupyter_lsp-2.3.0-py3-none-any.whl.metadata (1.8 kB)
Collecting jupyter-server<3,>=2.4.0 (from jupyterlab->jupyter)
  Downloading jupyter_server-2.17.0-py3-none-any.whl.metadata (8.5 kB)
Collecting jupyterlab-server<3,>=2.27.1 (from jupyterlab->jupyter)
  Downloading jupyterlab_server-2.28.0-py3-none-any.whl.metadata (5.9 kB)
Collecting notebook-shim>=0.2 (from jupyterlab->jupyter)
  Downloading notebook_shim-0.2.4-py3-none-any.whl.metadata (4.0 kB)
Collecting setuptools>=41.1.0 (from jupyterlab->jupyter)
  Downloading setuptools-80.9.0-py3-none-any.whl.metadata (6.6 kB)
Collecting anyio (from httpx<1,>=0.25.0->jupyterlab->jupyter)
  Downloading anyio-4.11.0-py3-none-any.whl.metadata (4.1 kB)
Collecting certifi (from httpx<1,>=0.25.0->jupyterlab->jupyter)
  Downloading certifi-2025.10.5-py3-none-any.whl.metadata (2.5 kB)
Collecting httpcore==1.* (from httpx<1,>=0.25.0->jupyterlab->jupyter)
  Downloading httpcore-1.0.9-py3-none-any.whl.metadata (21 kB)
Collecting idna (from httpx<1,>=0.25.0->jupyterlab->jupyter)
  Downloading idna-3.11-py3-none-any.whl.metadata (8.4 kB)
Collecting h11>=0.16 (from httpcore==1.*->httpx<1,>=0.25.0->jupyterlab->jupyter)
  Downloading h11-0.16.0-py3-none-any.whl.metadata (8.3 kB)
Collecting argon2-cffi>=21.1 (from jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading argon2_cffi-25.1.0-py3-none-any.whl.metadata (4.1 kB)
Collecting jupyter-events>=0.11.0 (from jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading jupyter_events-0.12.0-py3-none-any.whl.metadata (5.8 kB)
Collecting jupyter-server-terminals>=0.4.4 (from jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading jupyter_server_terminals-0.5.3-py3-none-any.whl.metadata (5.6 kB)
Collecting nbformat>=5.3.0 (from jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading nbformat-5.10.4-py3-none-any.whl.metadata (3.6 kB)
Collecting prometheus-client>=0.9 (from jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading prometheus_client-0.23.1-py3-none-any.whl.metadata (1.9 kB)
Collecting send2trash>=1.8.2 (from jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading Send2Trash-1.8.3-py3-none-any.whl.metadata (4.0 kB)
Collecting terminado>=0.8.3 (from jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading terminado-0.18.1-py3-none-any.whl.metadata (5.8 kB)
Collecting websocket-client>=1.7 (from jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading websocket_client-1.9.0-py3-none-any.whl.metadata (8.3 kB)
Collecting babel>=2.10 (from jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading babel-2.17.0-py3-none-any.whl.metadata (2.0 kB)
Collecting json5>=0.9.0 (from jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading json5-0.12.1-py3-none-any.whl.metadata (36 kB)
Collecting jsonschema>=4.18.0 (from jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading jsonschema-4.25.1-py3-none-any.whl.metadata (7.6 kB)
Collecting requests>=2.31 (from jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading requests-2.32.5-py3-none-any.whl.metadata (4.9 kB)
Collecting sniffio>=1.1 (from anyio->httpx<1,>=0.25.0->jupyterlab->jupyter)
  Downloading sniffio-1.3.1-py3-none-any.whl.metadata (3.9 kB)
Collecting argon2-cffi-bindings (from argon2-cffi>=21.1->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading argon2_cffi_bindings-25.1.0-cp39-abi3-macosx_11_0_arm64.whl.metadata (7.4 kB)
Collecting MarkupSafe>=2.0 (from jinja2>=3.0.3->jupyterlab->jupyter)
  Downloading markupsafe-3.0.3-cp314-cp314-macosx_11_0_arm64.whl.metadata (2.7 kB)
Collecting attrs>=22.2.0 (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading attrs-25.4.0-py3-none-any.whl.metadata (10 kB)
Collecting jsonschema-specifications>=2023.03.6 (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading jsonschema_specifications-2025.9.1-py3-none-any.whl.metadata (2.9 kB)
Collecting referencing>=0.28.4 (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading referencing-0.37.0-py3-none-any.whl.metadata (2.8 kB)
Collecting rpds-py>=0.7.1 (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading rpds_py-0.28.0-cp314-cp314-macosx_11_0_arm64.whl.metadata (4.1 kB)
Collecting python-json-logger>=2.0.4 (from jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading python_json_logger-4.0.0-py3-none-any.whl.metadata (4.0 kB)
Collecting pyyaml>=5.3 (from jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading pyyaml-6.0.3-cp314-cp314-macosx_11_0_arm64.whl.metadata (2.4 kB)
Collecting rfc3339-validator (from jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading rfc3339_validator-0.1.4-py2.py3-none-any.whl.metadata (1.5 kB)
Collecting rfc3986-validator>=0.1.1 (from jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading rfc3986_validator-0.1.1-py2.py3-none-any.whl.metadata (1.7 kB)
Collecting fqdn (from jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading fqdn-1.5.1-py3-none-any.whl.metadata (1.4 kB)
Collecting isoduration (from jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading isoduration-20.11.0-py3-none-any.whl.metadata (5.7 kB)
Collecting jsonpointer>1.13 (from jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading jsonpointer-3.0.0-py2.py3-none-any.whl.metadata (2.3 kB)
Collecting rfc3987-syntax>=1.1.0 (from jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading rfc3987_syntax-1.1.0-py3-none-any.whl.metadata (7.7 kB)
Collecting uri-template (from jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading uri_template-1.3.0-py3-none-any.whl.metadata (8.8 kB)
Collecting webcolors>=24.6.0 (from jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading webcolors-24.11.1-py3-none-any.whl.metadata (2.2 kB)
Collecting beautifulsoup4 (from nbconvert->jupyter)
  Downloading beautifulsoup4-4.14.2-py3-none-any.whl.metadata (3.8 kB)
Collecting bleach!=5.0.0 (from bleach[css]!=5.0.0->nbconvert->jupyter)
  Downloading bleach-6.3.0-py3-none-any.whl.metadata (31 kB)
Collecting defusedxml (from nbconvert->jupyter)
  Downloading defusedxml-0.7.1-py2.py3-none-any.whl.metadata (32 kB)
Collecting jupyterlab-pygments (from nbconvert->jupyter)
  Downloading jupyterlab_pygments-0.3.0-py3-none-any.whl.metadata (4.4 kB)
Collecting mistune<4,>=2.0.3 (from nbconvert->jupyter)
  Downloading mistune-3.1.4-py3-none-any.whl.metadata (1.8 kB)
Collecting nbclient>=0.5.0 (from nbconvert->jupyter)
  Downloading nbclient-0.10.2-py3-none-any.whl.metadata (8.3 kB)
Collecting pandocfilters>=1.4.1 (from nbconvert->jupyter)
  Downloading pandocfilters-1.5.1-py2.py3-none-any.whl.metadata (9.0 kB)
Collecting webencodings (from bleach!=5.0.0->bleach[css]!=5.0.0->nbconvert->jupyter)
  Downloading webencodings-0.5.1-py2.py3-none-any.whl.metadata (2.1 kB)
Collecting tinycss2<1.5,>=1.1.0 (from bleach[css]!=5.0.0->nbconvert->jupyter)
  Downloading tinycss2-1.4.0-py3-none-any.whl.metadata (3.0 kB)
Collecting fastjsonschema>=2.15 (from nbformat>=5.3.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading fastjsonschema-2.21.2-py3-none-any.whl.metadata (2.3 kB)
Collecting charset_normalizer<4,>=2 (from requests>=2.31->jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading charset_normalizer-3.4.4-cp314-cp314-macosx_10_13_universal2.whl.metadata (37 kB)
Collecting urllib3<3,>=1.21.1 (from requests>=2.31->jupyterlab-server<3,>=2.27.1->jupyterlab->jupyter)
  Downloading urllib3-2.5.0-py3-none-any.whl.metadata (6.5 kB)
Collecting lark>=1.2.2 (from rfc3987-syntax>=1.1.0->jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading lark-1.3.1-py3-none-any.whl.metadata (1.8 kB)
Collecting cffi>=2.0.0b1 (from argon2-cffi-bindings->argon2-cffi>=21.1->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading cffi-2.0.0-cp314-cp314-macosx_11_0_arm64.whl.metadata (2.6 kB)
Collecting pycparser (from cffi>=2.0.0b1->argon2-cffi-bindings->argon2-cffi>=21.1->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading pycparser-2.23-py3-none-any.whl.metadata (993 bytes)
Collecting soupsieve>1.2 (from beautifulsoup4->nbconvert->jupyter)
  Downloading soupsieve-2.8-py3-none-any.whl.metadata (4.6 kB)
Collecting typing-extensions>=4.0.0 (from beautifulsoup4->nbconvert->jupyter)
  Downloading typing_extensions-4.15.0-py3-none-any.whl.metadata (3.3 kB)
Collecting arrow>=0.15.0 (from isoduration->jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading arrow-1.4.0-py3-none-any.whl.metadata (7.7 kB)
Collecting tzdata (from arrow>=0.15.0->isoduration->jsonschema[format-nongpl]>=4.18.0->jupyter-events>=0.11.0->jupyter-server<3,>=2.4.0->jupyterlab->jupyter)
  Downloading tzdata-2025.2-py2.py3-none-any.whl.metadata (1.4 kB)
Collecting executing>=1.2.0 (from stack_data->ipython>=7.23.1->ipykernel->jupyter)
  Downloading executing-2.2.1-py2.py3-none-any.whl.metadata (8.9 kB)
Collecting asttokens>=2.1.0 (from stack_data->ipython>=7.23.1->ipykernel->jupyter)
  Downloading asttokens-3.0.0-py3-none-any.whl.metadata (4.7 kB)
Collecting pure-eval (from stack_data->ipython>=7.23.1->ipykernel->jupyter)
  Downloading pure_eval-0.2.3-py3-none-any.whl.metadata (6.3 kB)
Downloading jupyter-1.1.1-py2.py3-none-any.whl (2.7 kB)
Downloading ipykernel-7.1.0-py3-none-any.whl (117 kB)
Downloading appnope-0.1.4-py2.py3-none-any.whl (4.3 kB)
Downloading comm-0.2.3-py3-none-any.whl (7.3 kB)
Downloading debugpy-1.8.17-cp314-cp314-macosx_15_0_universal2.whl (2.5 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.5/2.5 MB 536.0 kB/s  0:00:04
Downloading ipython-9.6.0-py3-none-any.whl (616 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 616.2/616.2 kB 706.6 kB/s  0:00:00
Downloading prompt_toolkit-3.0.52-py3-none-any.whl (391 kB)
Downloading jedi-0.19.2-py2.py3-none-any.whl (1.6 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.6/1.6 MB 621.4 kB/s  0:00:02
Downloading parso-0.8.5-py2.py3-none-any.whl (106 kB)
Downloading jupyter_client-8.6.3-py3-none-any.whl (106 kB)
Downloading jupyter_core-5.9.1-py3-none-any.whl (29 kB)
Downloading matplotlib_inline-0.2.1-py3-none-any.whl (9.5 kB)
Downloading nest_asyncio-1.6.0-py3-none-any.whl (5.2 kB)
Downloading packaging-25.0-py3-none-any.whl (66 kB)
Downloading pexpect-4.9.0-py2.py3-none-any.whl (63 kB)
Downloading platformdirs-4.5.0-py3-none-any.whl (18 kB)
Downloading psutil-7.1.2-cp36-abi3-macosx_11_0_arm64.whl (238 kB)
Downloading ptyprocess-0.7.0-py2.py3-none-any.whl (13 kB)
Downloading pygments-2.19.2-py3-none-any.whl (1.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.2/1.2 MB 254.4 kB/s  0:00:04
Downloading python_dateutil-2.9.0.post0-py2.py3-none-any.whl (229 kB)
Downloading pyzmq-27.1.0-cp312-abi3-macosx_10_15_universal2.whl (1.3 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.3/1.3 MB 354.5 kB/s  0:00:03
Downloading six-1.17.0-py2.py3-none-any.whl (11 kB)
Downloading tornado-6.5.2-cp39-abi3-macosx_10_9_universal2.whl (442 kB)
Downloading traitlets-5.14.3-py3-none-any.whl (85 kB)
Downloading decorator-5.2.1-py3-none-any.whl (9.2 kB)
Downloading ipython_pygments_lexers-1.1.1-py3-none-any.whl (8.1 kB)
Downloading ipywidgets-8.1.7-py3-none-any.whl (139 kB)
Downloading jupyterlab_widgets-3.0.15-py3-none-any.whl (216 kB)
Downloading widgetsnbextension-4.0.14-py3-none-any.whl (2.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.2/2.2 MB 348.4 kB/s  0:00:06
Downloading jupyter_console-6.6.3-py3-none-any.whl (24 kB)
Downloading jupyterlab-4.4.10-py3-none-any.whl (12.3 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.3/12.3 MB 1.3 MB/s  0:00:09
Downloading httpx-0.28.1-py3-none-any.whl (73 kB)
Downloading httpcore-1.0.9-py3-none-any.whl (78 kB)
Downloading jupyter_server-2.17.0-py3-none-any.whl (388 kB)
Downloading jupyterlab_server-2.28.0-py3-none-any.whl (59 kB)
Downloading anyio-4.11.0-py3-none-any.whl (109 kB)
Downloading argon2_cffi-25.1.0-py3-none-any.whl (14 kB)
Downloading async_lru-2.0.5-py3-none-any.whl (6.1 kB)
Downloading babel-2.17.0-py3-none-any.whl (10.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 10.2/10.2 MB 5.0 MB/s  0:00:02
Downloading h11-0.16.0-py3-none-any.whl (37 kB)
Downloading idna-3.11-py3-none-any.whl (71 kB)
Downloading jinja2-3.1.6-py3-none-any.whl (134 kB)
Downloading json5-0.12.1-py3-none-any.whl (36 kB)
Downloading jsonschema-4.25.1-py3-none-any.whl (90 kB)
Downloading attrs-25.4.0-py3-none-any.whl (67 kB)
Downloading jsonschema_specifications-2025.9.1-py3-none-any.whl (18 kB)
Downloading jupyter_events-0.12.0-py3-none-any.whl (19 kB)
Downloading jsonpointer-3.0.0-py2.py3-none-any.whl (7.6 kB)
Downloading jupyter_lsp-2.3.0-py3-none-any.whl (76 kB)
Downloading jupyter_server_terminals-0.5.3-py3-none-any.whl (13 kB)
Downloading markupsafe-3.0.3-cp314-cp314-macosx_11_0_arm64.whl (12 kB)
Downloading nbconvert-7.16.6-py3-none-any.whl (258 kB)
Downloading mistune-3.1.4-py3-none-any.whl (53 kB)
Downloading bleach-6.3.0-py3-none-any.whl (164 kB)
Downloading tinycss2-1.4.0-py3-none-any.whl (26 kB)
Downloading nbclient-0.10.2-py3-none-any.whl (25 kB)
Downloading nbformat-5.10.4-py3-none-any.whl (78 kB)
Downloading fastjsonschema-2.21.2-py3-none-any.whl (24 kB)
Downloading notebook_shim-0.2.4-py3-none-any.whl (13 kB)
Downloading pandocfilters-1.5.1-py2.py3-none-any.whl (8.7 kB)
Downloading prometheus_client-0.23.1-py3-none-any.whl (61 kB)
Downloading python_json_logger-4.0.0-py3-none-any.whl (15 kB)
Downloading pyyaml-6.0.3-cp314-cp314-macosx_11_0_arm64.whl (173 kB)
Downloading referencing-0.37.0-py3-none-any.whl (26 kB)
Downloading requests-2.32.5-py3-none-any.whl (64 kB)
Downloading charset_normalizer-3.4.4-cp314-cp314-macosx_10_13_universal2.whl (207 kB)
Downloading urllib3-2.5.0-py3-none-any.whl (129 kB)
Downloading certifi-2025.10.5-py3-none-any.whl (163 kB)
Downloading rfc3986_validator-0.1.1-py2.py3-none-any.whl (4.2 kB)
Downloading rfc3987_syntax-1.1.0-py3-none-any.whl (8.0 kB)
Downloading lark-1.3.1-py3-none-any.whl (113 kB)
Downloading rpds_py-0.28.0-cp314-cp314-macosx_11_0_arm64.whl (341 kB)
Downloading Send2Trash-1.8.3-py3-none-any.whl (18 kB)
Downloading setuptools-80.9.0-py3-none-any.whl (1.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.2/1.2 MB 6.7 MB/s  0:00:00
Downloading sniffio-1.3.1-py3-none-any.whl (10 kB)
Downloading terminado-0.18.1-py3-none-any.whl (14 kB)
Downloading webcolors-24.11.1-py3-none-any.whl (14 kB)
Downloading webencodings-0.5.1-py2.py3-none-any.whl (11 kB)
Downloading websocket_client-1.9.0-py3-none-any.whl (82 kB)
Downloading argon2_cffi_bindings-25.1.0-cp39-abi3-macosx_11_0_arm64.whl (31 kB)
Downloading cffi-2.0.0-cp314-cp314-macosx_11_0_arm64.whl (181 kB)
Downloading beautifulsoup4-4.14.2-py3-none-any.whl (106 kB)
Downloading soupsieve-2.8-py3-none-any.whl (36 kB)
Downloading typing_extensions-4.15.0-py3-none-any.whl (44 kB)
Downloading defusedxml-0.7.1-py2.py3-none-any.whl (25 kB)
Downloading fqdn-1.5.1-py3-none-any.whl (9.1 kB)
Downloading isoduration-20.11.0-py3-none-any.whl (11 kB)
Downloading arrow-1.4.0-py3-none-any.whl (68 kB)
Downloading jupyterlab_pygments-0.3.0-py3-none-any.whl (15 kB)
Downloading notebook-7.4.7-py3-none-any.whl (14.3 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 14.3/14.3 MB 10.2 MB/s  0:00:01
Downloading pycparser-2.23-py3-none-any.whl (118 kB)
Downloading rfc3339_validator-0.1.4-py2.py3-none-any.whl (3.5 kB)
Downloading stack_data-0.6.3-py3-none-any.whl (24 kB)
Downloading asttokens-3.0.0-py3-none-any.whl (26 kB)
Downloading executing-2.2.1-py2.py3-none-any.whl (28 kB)
Downloading pure_eval-0.2.3-py3-none-any.whl (11 kB)
Downloading tzdata-2025.2-py2.py3-none-any.whl (347 kB)
Downloading uri_template-1.3.0-py3-none-any.whl (11 kB)
Downloading wcwidth-0.2.14-py2.py3-none-any.whl (37 kB)
Installing collected packages: webencodings, pure-eval, ptyprocess, fastjsonschema, widgetsnbextension, websocket-client, webcolors, wcwidth, urllib3, uri-template, tzdata, typing-extensions, traitlets, tornado, tinycss2, soupsieve, sniffio, six, setuptools, send2trash, rpds-py, rfc3986-validator, pyzmq, pyyaml, python-json-logger, pygments, pycparser, psutil, prometheus-client, platformdirs, pexpect, parso, pandocfilters, packaging, nest-asyncio, mistune, MarkupSafe, lark, jupyterlab_widgets, jupyterlab-pygments, jsonpointer, json5, idna, h11, fqdn, executing, defusedxml, decorator, debugpy, comm, charset_normalizer, certifi, bleach, babel, attrs, async-lru, asttokens, appnope, terminado, stack_data, rfc3987-syntax, rfc3339-validator, requests, referencing, python-dateutil, prompt_toolkit, matplotlib-inline, jupyter-core, jinja2, jedi, ipython-pygments-lexers, httpcore, cffi, beautifulsoup4, anyio, jupyter-server-terminals, jupyter-client, jsonschema-specifications, ipython, httpx, arrow, argon2-cffi-bindings, jsonschema, isoduration, ipywidgets, ipykernel, argon2-cffi, nbformat, jupyter-console, nbclient, jupyter-events, nbconvert, jupyter-server, notebook-shim, jupyterlab-server, jupyter-lsp, jupyterlab, notebook, jupyter
Successfully installed MarkupSafe-3.0.3 anyio-4.11.0 appnope-0.1.4 argon2-cffi-25.1.0 argon2-cffi-bindings-25.1.0 arrow-1.4.0 asttokens-3.0.0 async-lru-2.0.5 attrs-25.4.0 babel-2.17.0 beautifulsoup4-4.14.2 bleach-6.3.0 certifi-2025.10.5 cffi-2.0.0 charset_normalizer-3.4.4 comm-0.2.3 debugpy-1.8.17 decorator-5.2.1 defusedxml-0.7.1 executing-2.2.1 fastjsonschema-2.21.2 fqdn-1.5.1 h11-0.16.0 httpcore-1.0.9 httpx-0.28.1 idna-3.11 ipykernel-7.1.0 ipython-9.6.0 ipython-pygments-lexers-1.1.1 ipywidgets-8.1.7 isoduration-20.11.0 jedi-0.19.2 jinja2-3.1.6 json5-0.12.1 jsonpointer-3.0.0 jsonschema-4.25.1 jsonschema-specifications-2025.9.1 jupyter-1.1.1 jupyter-client-8.6.3 jupyter-console-6.6.3 jupyter-core-5.9.1 jupyter-events-0.12.0 jupyter-lsp-2.3.0 jupyter-server-2.17.0 jupyter-server-terminals-0.5.3 jupyterlab-4.4.10 jupyterlab-pygments-0.3.0 jupyterlab-server-2.28.0 jupyterlab_widgets-3.0.15 lark-1.3.1 matplotlib-inline-0.2.1 mistune-3.1.4 nbclient-0.10.2 nbconvert-7.16.6 nbformat-5.10.4 nest-asyncio-1.6.0 notebook-7.4.7 notebook-shim-0.2.4 packaging-25.0 pandocfilters-1.5.1 parso-0.8.5 pexpect-4.9.0 platformdirs-4.5.0 prometheus-client-0.23.1 prompt_toolkit-3.0.52 psutil-7.1.2 ptyprocess-0.7.0 pure-eval-0.2.3 pycparser-2.23 pygments-2.19.2 python-dateutil-2.9.0.post0 python-json-logger-4.0.0 pyyaml-6.0.3 pyzmq-27.1.0 referencing-0.37.0 requests-2.32.5 rfc3339-validator-0.1.4 rfc3986-validator-0.1.1 rfc3987-syntax-1.1.0 rpds-py-0.28.0 send2trash-1.8.3 setuptools-80.9.0 six-1.17.0 sniffio-1.3.1 soupsieve-2.8 stack_data-0.6.3 terminado-0.18.1 tinycss2-1.4.0 tornado-6.5.2 traitlets-5.14.3 typing-extensions-4.15.0 tzdata-2025.2 uri-template-1.3.0 urllib3-2.5.0 wcwidth-0.2.14 webcolors-24.11.1 webencodings-0.5.1 websocket-client-1.9.0 widgetsnbextension-4.0.14

[notice] A new release of pip is available: 25.2 -> 25.3
[notice] To update, run: pip install --upgrade pip
(venv) annejessielynlozano@Annes-MacBook-Air my_notebook_project % pip3 install jupyter ipykernel
```
