<template>
  <div class="formulario">
    <form @submit.prevent="$emit('infoMonedas', cripto, moneda)">
      <div>
        <label><h4>Moneda Nacional:</h4> </label>
        <select v-model="moneda" required>
          <option value="" disabled selected>Seleccione una moneda...</option>
          <option>AR</option>
          <option>USD</option>
          <option>EUR</option>
        </select>
      </div>

      <div>
        <label><h4>Criptomoneda:</h4></label>
        <select v-model="cripto" required>
          <option value="" disabled selected>
            Seleccione una criptomoneda...
          </option>
          <option>BTC</option>
          <option>ETH</option>
          <option>USDT</option>
          <option>USDC</option>
          <option>BNB</option>
          <option>BUSD</option>
          <option>XRP</option>
          <option>ADA</option>
          <option>SOL</option>
          <option>DOGE</option>
          <option>DOT</option>
          <option>MATIC</option>
          <option>DAI</option>
          <option>SHIB</option>
          <option>AVAX</option>
          <option>LTC</option>
        </select>
      </div>

      <div>
        <button type="submit">Cotizar</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: () => ({
    moneda: "",
    cripto: "",
  }),
};
</script>