# map

Map displaying all support groups and events of JLM2017 campaign.

See it on https://jlm2017.github.io/map/.

Include it on web pages with `iframe`, such as :

```html
<iframe style="display:block; width: 90%; margin: auto; margin-bottom: 20px; height: 800px; height: 80vh; border: 1px solid #ccc;"
      src="https://jlm2017.github.io/map/"></iframe>
```

## Params

Params are passed to the app using query variables :

Example :
```html
<iframe
  style="border: none; margin: 0 0; padding: 0 0; width: 80%; height: 400px"
  src="https://jlm2017.github.io/map/?zipcode=[code-postal]&event_type=melenchon&circonscriptions=1">
</iframe>
```

* `event_type`: a column-separated list of event types to display. Available event_types are `groups`, `evenements_locaux`, `melenchon`, and `reunions_circonscription`. Default value is `groups,evenements_locaux,melenchon`
* `zipcode`: a french postal code to zoom in. The map tries to include the 4 closest groups or events (depending on the first element of `event_type`).
* `circonscriptions`: 0 or 1, displays the bounding of Grench electoral circonscriptions in the background. Default value: 0.
* `hide_panel`: 0 or 1, hide the panel. Default value: 0.
* `no_cluster`: 0 or 1, do not group the events on the map. Default value: 0.
* `tags`: comma-separated list of tags. Only display events with those tags. Display all events in undefined.
*  `hide_address` : 0 or 1, hide the search bar. Default value: 0.
*  `borderfit` : fix the limit of the map, provide a parameter like: maxlat,maxlong,minlat,minlong. Caution, it disable zipcode option
* `event_id` : an event ID and a resource name (event or group), for example `9999,events` to display single on the map
