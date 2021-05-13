# trackmania-medal-times

Trackmania medal times in JSON format. Can be used for various lookups and statistics.

## Examples

Nightbot command:

```
$(eval
  medals = $(urlfetch json https://raw.githubusercontent.com/Voyager006/trackmania-medal-times/main/turbo.json);
  track = Number.parseInt(decodeURIComponent("$(querystring)"));
  if (Number.isInteger(track) && track > 0 && track < 201) {
    "The Super Trackmaster for #" + track + " is " + medals["Super Trackmaster"][track - 1];
  } else {
    "Please provide a valid track number";
  }
)
```
