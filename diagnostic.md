# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
  Application Router is where you attached urls to specific actions or views.
  Ember route is where you attach data to the specific action or view.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
  ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
  {{#link-to 'campus/Boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
  The second route definition attaches a specific id for products as a whole, and for each product id separately.
  The first route defines a function for the product_id

    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    {{#each movie as |movie|}}
    <li>{{#link-to 'movies' movies}} {{movie.id}} {{/link-to}}</li>
  {{/each}}
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    {{#each movie as |movie|}}
    <li>{{#link-to 'movies' movies}} {{movie.id}} {{/link-to}}</li>
  {{/each}}
    ```
