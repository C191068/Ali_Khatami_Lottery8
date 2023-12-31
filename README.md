# Ali_Khatami_Lottery8(Learning from the video of Patrick collins)

### Deploying the Lottery contract 

It is almost imposiible to write a smart contract without making a mistake <br>

![d1](https://github.com/C191068/Ali_Khatami_Lottery8/assets/89090776/269cb89f-c319-47f6-98bb-b4159fb87f30)

here we create a new folder <br>

![d2](https://github.com/C191068/Ali_Khatami_Lottery8/assets/89090776/1c0090be-5d42-43a6-b8b6-3c47ce668e12)

at our code at here https://github.com/C191068/Ali_Khatami_Lottery7.git <br>
at constructor we see a ton of parameter <br>

We can see in the constructor we are interacting with contract vrfCoordinatorV2 <br>

As in the parameter vrfCoordinatorV2 is the address of the contract <br>

we probably  need to deploy  some mock for this <br>

Since it is the contract that we want to interact which is outside of our project <br>

![d3](https://github.com/C191068/Ali_Khatami_Lottery8/assets/89090776/13c8dad0-8d06-4610-9a96-38dca4ab939c)

here by opening this file we gonna deploy our lottery contract <br>


```js

module.exports = async function ({ getNamedAccounts, deployments }) {
    const { deploy, log } = deployments
    const { deployer } = await getNamedAccounts()
}

```

![d4](https://github.com/C191068/Ali_Khatami_Lottery8/assets/89090776/c326fb4d-8eab-4aa5-9b7f-58890237a2f1)

We have updated hardhat.config.js in the above way <br>
we have set deployer to 0 nad player to 1 <br>

```js

require("@nomiclabs/hardhat-waffle")
require("@nomiclabs/hardhat-etherscan")
require("hardhat-deploy")
require("solidity-coverage")
require("hardhat-gas-reporter")
require("hardhat-contract-sizer")
require("dotenv").config()

/** @type import('hardhat/config').HardhatUserConfig */
module.exports = {
    solidity: "0.8.19",
    namedAccounts: {
        deployer: {
            derfault: 0,
        },
        player: {
            default: 1,
        },
    },
}

```


For now we gonna grab our deployer and get started <br>


![d6](https://github.com/C191068/Ali_Khatami_Lottery8/assets/89090776/aaeb25eb-bdf0-40b0-b75f-1f25c6b60afd)

We have also made another changein the code <br>


In our hardhat config we don't have a network <br>


So we will add network here to get those block confirmation <br>
















