# Bot DataLayer

A standalone browser script that pushes only bot signals into your data layer.

## Output fields

- event
- isBot (1 or 0)
- botAgent (user agent string when isBot=1)

## Install

```html
<script>
  window.MALBotLayerConfig = {
    dataLayerName: 'dataLayer',
    eventName: 'mal_bot_signal',
    autoPush: true
  };
</script>
<script src="./src/bot-datalayer.js" defer></script>
```

## Manual push mode

```html
<script>
  window.MALBotLayerConfig = { autoPush: false };
</script>
<script src="./src/bot-datalayer.js" defer></script>
<script>
  window.MALBotLayer.push();
</script>
```

## Notes

- Client-side bot detection is probabilistic.
- Pair with server-side detection for higher confidence.

## License

MIT
