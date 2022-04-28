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

rename `env.example` to `.env`

## Add the NodeJS kernel

#### Linux

```
npm install -g ijavascript
ijsinstall
```

#### MacOS

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/main/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
brew install pkg-config node zeromq
sudo easy_install pip
pip install --upgrade pyzmq jupyter
npm install -g ijavascript
ijsinstall
```

## Tips

#### Load environment variables

environment variables are lazy loaded from `.env` file. To use in a notebook
you need to add the following line to the top of the notebook:

```
Etherscan_APIKEY = config('ETHERSCAN_APIKEY')
```

#### Using a forked network

```
ganache-cli --fork "RPC_FORK_URL"
```

#### Variable explorer
