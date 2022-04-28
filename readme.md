# Notebooks

Prototype python and javascript notebooks.

## Setup
create a virtual environment:

```
python3 -m venv venv
source venv/bin/activate                           
```

then install packages:

```
pip install -r requirements.txt
yarn
```

create a `.env` file with the following variables:

```
RPC_Endpoint="YORR_RPC_URL"
Etherscan_APIKEY="YOUR_API_KEY"
FRAME_RPC="127.0.0.1:1248"
```

## Add the NodeJS kernel

#### Linux

```
npm install -g ijavascript
ijsinstall
```
#### MacOS

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install pkg-config node zeromq
sudo easy_install pip
pip install --upgrade pyzmq jupyter
npm install -g ijavascript
ijsinstall
```

## Usage
environment variables are lazy loaded from `.env` file. To use in a notebook 
you need to add the following line to the top of the notebook:

```
Etherscan_APIKEY = config('ETHERSCAN_APIKEY')
```