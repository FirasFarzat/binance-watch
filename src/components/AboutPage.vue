<template>
  <section>

    <div class="push-bottom">
      <div class="form-label push-bottom">
        Binance Price Watch Web App <i class="icon-down-open"></i>
      </div>
      <p>
        This application connects to the <a class="text-primary-hover" @click="goBinance" href="#">Binance.com</a>
        public <a href="https://github.com/binance-exchange/binance-official-api-docs" target="_blank">API</a>
        to get live 24h price change data for all crypto trading pairs on their platform and allows you to set
        custom alerts or watch for price change in real time and get desktop notifications when something triggers
        your alerts or price watch settings.
      </p>
    </div>

    <hr />

    <div class="push-bottom">
      <div class="form-label push-bottom">
        Application Technology <i class="icon-down-open"></i>
      </div>
      <p>
        This app runs entirely on the browser and only makes external requests to fetch data from various
        API endpoints related to cryptocurrency. Any persisting data is stored in the browser's
        <a href="https://developer.mozilla.org/en-US/docs/Web/API/Storage" target="_blank">localStorage</a> engine.
        In order to get desktop notifications, you must
        <a href="https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API/Using_the_Notifications_API" target="_blank">Grant Notification Permission</a>
        in your browser.
      </p>
    </div>

    <hr />

    <div class="push-bottom">
      <div class="form-label push-bottom">
        API Endpoints &amp; Assets <i class="icon-down-open"></i>
      </div>
      <ul>
        <li>
          <a href="https://github.com/binance-exchange/binance-official-api-docs" target="_blank">Binance API</a> &nbsp;
          <span>Socket connection for live 24h price change data.</span>
        </li>
        <li>
          <a href="https://github.com/CoinCapDev/CoinCap.io" target="_blank">Coincap API</a> &nbsp;
          <span>Aggregated global data for specific tokens.</span>
        </li>
        <li>
          <a href="https://www.mailgun.com/" target="_blank">Mailgun API</a> &nbsp;
          <span>Mailgun API for outgoing notifications via e-mail.</span>
        </li>
        <li>
          <a href="https://core.telegram.org/bots#creating-a-new-bot" target="_blank">Telegram Bot API</a> &nbsp;
          <span>Telegram Bot API for outgoing notifications via the app.</span>
        </li>
        <li>
          <a href="https://github.com/cjdowner/cryptocurrency-icons" target="_blank">Crypto Icons</a> &nbsp;
          <span>Nice looking crypto icons.</span>
        </li>
      </ul>
    </div>

    <hr />

    <div class="push-bottom">
      <div class="form-label push-bottom">
        Author &amp; Feedback <i class="icon-down-open"></i>
      </div>
      <ul>
        <li>
          <span>Author / Developer:</span> &nbsp;
          <a class="icon-ghub iconLeft" href="https://github.com/rainner" target="_blank">Rainner Lins</a> &nbsp;
          <a class="icon-twtr iconLeft" href="https://twitter.com/raintek_" target="_blank">raintek_</a> &nbsp;
        </li>
        <li>
          <span>Repo / Issues / Feedback:</span> &nbsp;
          <a class="icon-ghub iconLeft" href="https://github.com/rainner/binance-watch" target="_blank">Binance Watch Repository</a> &nbsp;
        </li>
      </ul>
    </div>

  </section>
</template>

<script>
// component
export default {

  methods: {

    // lick to binance site with ref id added
    goBinance( e ) {
      e.preventDefault();
      this.$bus.emit( 'handleClick', 'binance', '/', '_blank' );
    }
  }

}
</script>

