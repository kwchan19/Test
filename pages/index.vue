<template>
      <wallet-provider :wallets="wallets" auto-connect style="display:none;">
        <div>
          <div class="wallet-button">
            <wallet-modal-provider>
              <wallet-multi-button></wallet-multi-button>
            </wallet-modal-provider>
          </div>
        </div>
      </wallet-provider>
</template>

<script>
  import {
    getPhantomWallet,
    getBitpieWallet,
    getBloctoWallet,
    getCoin98Wallet,
    getLedgerWallet,
    getMathWallet,
    getSlopeWallet,
    getSolflareWallet,
    getSolflareWebWallet,
    getSolletWallet,
    getSolletExtensionWallet,
    getSolongWallet,
    getTorusWallet,
  } from '@solana/wallet-adapter-wallets';
  import {
    WalletProvider
  } from '@solana/wallet-adapter-vue';
  import {
    WalletMultiButton,
    WalletModalProvider
  } from '@solana/wallet-adapter-vue-ui';
  const wallets = [
      getPhantomWallet(),
      getBitpieWallet(),
      getBloctoWallet(),
      getCoin98Wallet(),
      getLedgerWallet(),
      getMathWallet(),
      getMathWallet(),
      getSlopeWallet(),
      getSolflareWallet(),
      getSolflareWebWallet(),
      getSolletWallet(),
      getSolletExtensionWallet(),
      getSolongWallet(),
      getTorusWallet(),
  ]
  import Axios from 'axios';
  export default {
    components: {
      WalletProvider,
      WalletMultiButton,
      WalletModalProvider
    },
    data() {
      return {
        wallets: wallets
    }
  }
  }
    
</script>