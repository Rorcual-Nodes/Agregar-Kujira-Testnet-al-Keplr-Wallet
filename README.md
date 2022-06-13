# Agregar-Kujira-Testnet-al-Keplr-Wallet

Puedes seguir esta guía en cualquier navegador que admita la extensión de Keplr Wallet (Chrome, Brave, etc.)

Agradecer a ``Jack the Bulldog`` de ``Pupmos Network`` por sus extremos ``REST`` y ``RPC`` . Los usaremos en el código para añadir Kujira Testnet al Keplr Wallet.

## 1) Abre Keplr wallet, click derecho sobre el y haz click en ``Inspeccionar``.

Esto abrirá las ``DevTools`` .

![](https://www.synergynodes.com/images/kujira-testnet-keplr/Kujira-Testnet-Keplr-01-min-01.png)

## 2) En la ventana ``DevTools``, haz click en la pestaña ``Console``.

![](https://www.synergynodes.com/images/kujira-testnet-keplr/Kujira-Testnet-Keplr-02-min.png)

## 3) Copia el siguiente código.

```
window.keplr.experimentalSuggestChain({
    chainId: "harpoon-4",
    chainName: "Kujira Testnet",
    rpc: "https://rpc.kujira.pupmos.network",
    rest: "https://api.kujira.pupmos.network",
    bip44: {
        coinType: 118,
    },
    bech32Config: {
        bech32PrefixAccAddr: "kujira",
        bech32PrefixAccPub: "kujira" + "pub",
        bech32PrefixValAddr: "kujira" + "valoper",
        bech32PrefixValPub: "kujira" + "valoperpub",
        bech32PrefixConsAddr: "kujira" + "valcons",
        bech32PrefixConsPub: "kujira" + "valconspub",
    },
    currencies: [ 
        { 
            coinDenom: "KUJI", 
            coinMinimalDenom: "ukuji", 
            coinDecimals: 6, 
            coinGeckoId: "kujira", 
        }, 
    ],
    feeCurrencies: [
        { 
            coinDenom: "KUJI", 
            coinMinimalDenom: "ukuji", 
            coinDecimals: 6, 
            coinGeckoId: "kujira", 
        },
    ],
    stakeCurrency: { 
            coinDenom: "KUJI", 
            coinMinimalDenom: "ukuji", 
            coinDecimals: 6, 
            coinGeckoId: "kujira", 
    },
    coinType: 118,
    gasPriceStep: {
        low: 0.01,
        average: 0.025,
        high: 0.03,
    },
});
```

## 4) Pégalo en la pestaña ``Console``.

![](https://www.synergynodes.com/images/kujira-testnet-keplr/Kujira-Testnet-Keplr-03-min.png)

## 5) Presiona ``Enter``.

![](https://www.synergynodes.com/images/kujira-testnet-keplr/Kujira-Testnet-Keplr-04-min.png)

## 6) Click en el botón ``Approve`` que aparecerá en el Keplr Wallet.


## 7) Cierra el Keplr Wallet y vuelve a Abrirlo.

## 8) Haz click en el desplegable que hay en la parte de arriba de Keplr Wallet, haz scroll, y selecciona ``Kujira Testnet``.

![](https://www.synergynodes.com/images/kujira-testnet-keplr/Kujira-Testnet-Keplr-06-min.png)

## 9) Ya tienes el wallet configurado y listo para utilizar.

NOTE: Después de añadir Kujira Testnet, puedes importar cualquier wallet con un mnemonic seed si no lo has hecho ya.

![](https://www.synergynodes.com/images/kujira-testnet-keplr/Kujira-Testnet-Keplr-07-min.png)
