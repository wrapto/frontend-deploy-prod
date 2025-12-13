# How to Use Wrapto

Wrapto provides a simple workflow for moving PAC across chains by handling the wrapping and uwraping transactions.

## Wrapping PAC (PAC → WPAC)

To wrap PAC into WPAC, you can either send a transaction manually or use the Pactus Web Wallet.

### Using Pactus Wallet

1. Go to **[https://wallet.pactus.org](https://wallet.pactus.org)**
2. Select the account you want to send PAC from.
3. Click the **“Bridge”** button.
4. Send the bridge transaction.

### Manual Transaction

1. On Wrapto (**[https://wrapto.app](https://wrapto.app)**), choose **“Transfer From”** as PAC (source token) and select the target chain (e.g., Polygon).
2. Enter the **amount** of PAC you want to wrap/bridge.
3. Under **“Transfer To”**, select the destination network and enter your EVM wallet address.
4. Click **“Bridge”** and confirm the destination address.
5. Follow the instructions by sending the required PAC amount (minimum 10 PAC) to the **Wrapto Deposit** address, including the provided memo.

Once you send the bridge transaction, Wrapto will process it shortly. When completed, you will receive the corresponding amount of WPAC on the selected EVM chain.

---

## Unwrapping WPAC (WPAC → PAC)

1. Open **[https://wrapto.app](https://wrapto.app)** in your browser.
2. Click **“Connect Wallet”** and connect a supported EVM wallet (e.g., MetaMask, Trust Wallet, or any EVM-compatible wallet).
3. Make sure your wallet is on the correct chain (Base, BNB Chain, Kava, Polygon — whichever holds your WPAC).
4. Enter the amount of WPAC you want to unwrap back to PAC.
5. Enter your Pactus wallet address (starting with **pc1…**).
6. Confirm the transaction in your EVM wallet.

After confirmation, the WPAC will be burned, and the equivalent amount of PAC will be released and sent to your Pactus wallet.

---

## Important Notes & Tips

* WPAC is an ERC-20 token, so it behaves like any standard ERC-20 token on EVM chains.
* Always double-check the **target chain** and **destination address** when bridging — sending to the wrong address can result in permanent loss.
* If you submit the wrap transaction manually, make sure the **memo is correct**; an incorrect or missing memo may cause loss of funds.
