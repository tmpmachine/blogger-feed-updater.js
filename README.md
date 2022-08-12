# blogger-feed-updater.js

# options
option | description
--- | ---
`maxResults` | default to `50`
`updateRange` | 
`onFeedReady` |
`onStateChange` |  
`lang` |

# `updatedRange`
- `uid`
- `publishedMin`
- `publishedMax`

# Language Customization
- `updating`
- `upToDate`

# State Handling
- checkingUpdate : 0
- updating : 1
- upToDate : 2

# Updating State
- current
- total
- batchCurrent
- batchCurrent

# Usage Example
```html
<script src='blogger-feed-updater.js'></script>

<script>

  let options = {
    updateRange: [
      { uid: 1, publishedMin: '2017-01-01T00:00:00', publishedMax: '2021-01-01T00:00:00' },
      { uid: 2, publishedMin: '2021-01-01T00:00:01', publishedMax: '2022-04-01T00:00:00' },
      { uid: 3, publishedMin: '2022-04-01T00:00:01', publishedMax: '2024-01-01T00:00:00' },
    ],
    onFeedReady: function(feed) {
      console.log(feed)
    },
    onStateChange: function(state, data) {
      console.log(state,data)
    },
  };

  let compo = SongManagerComponent(options);
  compo.checkUpdate();
  
</script>
```
