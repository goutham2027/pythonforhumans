---
title: Python datetime snippets
---

# TODO
* To get local timezone

{% highlight python %}
# Current system time
from datetime import datetime
current_time = datetime.now()
print current_time
>>> 2017-02-01 23:52:20.987374
{% endhighlight %}

{%highlight python %}
# Curent UTC time
from datetime import datetime
current_utc_now = datetime.utcnow()
print current_utc_now
>>> 2017-02-01 18:25:11.283255
{% endhighlight %}

{% highlight python %}
# Format date-time
from datetime import datetime
now = datetime.now()
# Format: YYYY-MM-DD HH:MM:SS
print now.strftime("%Y-%m-%d %H:%M:%S")
>>> '2017-02-01 23:51:48'
{% endhighlight %}

{% highlight python %}
# Current time in Unix time stamp
import calendar
from datetime import datetime
now = datetime.now()
timestamp = calendar.timegm(now.timetuple())
print timestamp
>>> 1485994420
{% endhighlight %}

{% highlight python %}
# Unix timestamp to utc time
from datetime import datetime
# considers system time zone
date_time = datetime.utcfromtimestamp(1485994420)
print date_time
>>> 2017-02-02 00:13:40
# to get real utc time
date_time = datetime.fromtimestamp(1485994420)
print date_time
>>> 2017-02-02 05:43:40
{% endhighlight %}


{% highlight python %}
# Date in ISO 8601 format.
# isoformat() returns string instead of datetime.
from datetime import datetime

print datetime.utcnow().isoformat()
>>> 2017-02-01T18:54:19.178888

print datetime.now().isoformat()
>>> 2017-02-02T00:27:02.386565
{% endhighlight %}




