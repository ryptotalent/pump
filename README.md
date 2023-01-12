# pump
buildspace
require("@nomicfoundation/hardhat-toolbox");

// This is a sample Hardhat task. To learn how to create your own go to
// https://hardhat.org/guides/create-task.html
task("accounts", "Prints the list of accounts", async (taskArgs, hre) => {
    const accounts = await hre.ethers.getSigners();

    for (const account of accounts) {
        console.log(account.address);
    }
});

// You need to export an object to set up your config
// Go to https://hardhat.org/config/ to learn more

/**
 * @type import('hardhat/config').HardhatUserConfig
 */
module.exports = {
    solidity: "0.8.17",
    networks: {
      goerli: {
        url: "https://proud-dry-sheet.ethereum-goerli.discover.quiknode.pro/2875e821c9f02f00bb3aff85d95e75e52c853193/",
        accounts: ["46b5bbb521a89412baa92f8e5ae80cadb05470d18e4e9607ab08397128e74b6c"]
      },
    },
};
