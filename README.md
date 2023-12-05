aleo smart contract


Ù†ØµØ¨ Ù¾ÛŒØ´ Ù†ÛŒØ§Ø²Ù‡Ø§ 
------------------------------------------------------------------
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

source $HOME/.cargo/env

rustup install stable

rustup update stable

rustup default stable

git clone https://github.com/AleoHQ/leo
cd leo

apt install clang gcc libssl-dev pkg-config

cargo install --path .

git clone https://github.com/AleoHQ/snarkOS.git --depth 1
cd snarkOS

./build_ubuntu.sh

cargo install --path .


ØªÙˆÛŒÛŒØª Ø¨Ø±Ø§ÛŒ ÙØ§Ø³Øª
------------------------------------------------------------------

@AleoFaucet send 10 credits to aleo1y9s2yr50paljp0rd8wtqzy6ue9cshyyukwfslx2vhpj588vnguzqnndumr

Ø¨Ø¹Ø¯ Ø§Ø² Ø¯Ø±ÛŒØ§ÙØª ÙØ§Ø³Øª Ø¨Ù‡ Ù„ÛŒÙ†Ú© Ø²ÛŒØ± Ø¨Ø±ÛŒØ¯ Ùˆ Ø§ÙØ²ÙˆÙ†Ù‡ Ø±Ø§ Ø¨Ù‡ Ù…Ø±ÙˆØ±Ú¯Ø± Ú©Ø±ÙˆÙ… Ø§Ø¶Ø§ÙÙ‡ Ú©Ù†ÛŒØ¯

https://chrome.google.com/webstore/detail/json-beautifier-editor/lpopeocbeepakdnipejhlpcmifheolpl
------------------------------------------------------------------

cd $HOME

mkdir demo_deploy_Leo_app && cd demo_deploy_Leo_app

WALLETADDRESS=""

APPNAME=helloworld_"${WALLETADDRESS:4:6}"

leo new "${APPNAME}"

PATHTOAPP=$(realpath -q $APPNAME)

cd $PATHTOAPP && cd ..

PRIVATEKEY=""

RECORD=""

snarkos developer deploy "${APPNAME}.aleo" --private-key "${PRIVATEKEY}" --query "https://vm.aleo.org/api" --path "./${APPNAME}/build/" --broadcast "https://vm.aleo.org/api/testnet3/transaction/broadcast" --fee 600000 --record "${RECORD}"

# Aloe
