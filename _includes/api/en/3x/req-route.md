<h3 id='req.route'>req.route</h3>

The currently matched `Route` containing
several properties such as the route's original path
string, the regexp generated, and so on.

{% highlight js %}
app.get('/user/:id?', function(req, res){
  console.log(req.route);
});
{% endhighlight %}

Example output from the previous snippet:

{% highlight js %}
{ path: '/user/:id?',
  method: 'get',
  callbacks: [ [Function] ],
  keys: [ { name: 'id', optional: true } ],
  regexp: /^\/user(?:\/([^\/]+?))?\/?$/i,
  params: [ id: '12' ] }
{% endhighlight %}
