# Sample Project

A template for a Synthetix project using the [Python SDK](https://github.com/Synthetixio/python-sdk)

## Getting Started

First, make sure you have the following:
* A RPC endpoint like [Infura](https://infura.io/) or [Alchemy](https://www.alchemy.com/)
* A wallet address **and** the private key for that address
* Installed Python 3.8 or greater
    * Run `python --version` in your terminal to check

Then, clone this repository to some location on your machine. For example:

```bash
git clone https://github.com/Synthetixio/project-template-python.git
cd project-template-python
```

Then, install the dependencies in a virual environment:

```bash
python3 -m venv env
source env/bin/activate

pip install --upgrade pip
pip install -r requirements.txt
```

Then, copy the `.env.example` file to `.env` and fill in the values for your RPC and wallet.

Finally, run the status script:

```bash
python status.py
```

You should expect some result that shows some balances and market info, like this:

```bash
$ python status.py

Address: 0xD199157bB8a47bEF78e539908dEE5A41e7d5FE9f
ETH balance: 1.287
WETH balance: 0.0
sUSD balance: 10238.922

Perps accounts: 100, 101, 102
Perps default account: 100
Perps markets: BTC, ETH, LINK, OP, SNX
```

Congratulations! If you've made it this far you can start to build your own project using the Python SDK. More scripts are available in the `scripts` directory.

## Running Scripts

If you've completed the steps above, you can run any of the scripts in the `scripts` directory. For example:

```bash
python scripts/create_account.py
```

These will not submit transactions unless you edit the script to set `submit=True`. This is a safety measure to prevent you from accidentally submitting transactions to the blockchain.
Always use caution and carefully review the code before submitting transactions.

## Documentation

For a full list of available methods, see the [Python SDK documentation](https://synthetixio.github.io/python-sdk/).