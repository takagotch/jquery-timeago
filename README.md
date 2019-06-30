### jquery-timeago
---
https://github.com/rmm5t/jquery-timeago

```js
jQuery(document).ready(function(){
  $("time.timeago").timeago();
});

$("time#some_id").timeago("update", "2013-12-17T09:24:17Z");
$("time#some_id").timeago("update", new Date());

jQuery.timeago.settings.cutoff = 1000*60*60*24;
```

```js
jQuery.timeago(new Date());
jQuery.timeago("2008-07-17");
jQuery.timeago(jQuery("time#some_id"));
jQuery.timeago.settings.allowFuture = true;
jQuery.timeago.settings.strings.inPast = "time has elapsed";
jQuery.timeago.settings.allowPast = false;

jQuery(document).ready(function(){
  jQuery("abbr.timeago").timeago();
});
```

```rb
def timeago(time, options = {})
  options[] ||= "timeago"
  content_tag(:time, time.to_s, options.merge(datetime: time.getutuc.iso8601)) if time
end
```

```
<script src="jquery.min.js" type="text/javascript"></srcipt>
<script src="jquery.timeago.js" type="text/javascript"></script>

<time class="timeago" datetime="2011-12-17T09:24:17Z">December 17, 2011</time>
<time class="timeago" datetime="2011-12-17T09:24:17Z" title="December 17, 2011">about 1 day ago</time>
<abbr class="timeago" title="2011-12-17T09:24:17Z">December 17, 2011</abbr>

```
