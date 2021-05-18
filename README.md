# responsive-mediacheck
Use media queries @media. That'll surely do it. Read up about media queries

bootstrap-responsive-ads
======================

Bootstrap with responsive banner ads 
====

This sample code (powered by [W3Masters](http://www.w3masters.nl/), [mediaCheck](https://github.com/sparkbox/mediaCheck) and [Twitter Bootstrap](http://twitter.github.com/bootstrap/) demonstrates how you can use responive banner ads with Twitter bootstrap or other responsive html5 solutions.
This example implements the Toppler strategy from [Ad Formats & Showcase](http://www.responsiveads.com/ad-formats-showcase/).

Please try the [demo](http://w3masters.nl/responsiveads/) or load the demo page in [responsinator.com](http://responsinator.com/?url=http%3A%2F%2Fw3masters.nl%2Fresponsiveads%2F)

Based on device (screenwidth / viewport) different formats of graphic banners are shown. Also the banner postion change.
Banners of the following formats are used: 160x600, 728x90, 468x60 and 320x50 (width x height in pixels).

Only loads banners which will be used. Every banner load is a real view for your stats. Banners will not resized or hide by CSS.

The strategy use three breakpoints: 768, 480 and 320 pixels.

#### media
Type: `string`

This is the mediaquery that will trigger the specified action. It should be in the form:

 * `(min-width: 420px)`
 * `(min-width: 35em)`
 * `(max-width: 800px)`
 * `(max-width: 60em)`

#### entry
Type: `function`

This function will execute once when the mediaquery becomes **active**.

#### exit
Type: `function`

This function will execute once when the mediaquery becomes **inactive**.

#### both
Type: `function`

This function will execute once when the mediaquery **changes** state.


## Usage Example:

```javascript
mediaCheck({
  media: '(max-width: 420px)',
  entry: function() {
    console.log('starting 420');
  },
  exit: function() {
    console.log('leaving 420');
  },
  both: function() {
    console.log('changing state');
  }
});
```

## Change History
 - 1.0.3
   - Fixes a bug that caused the both function to  
     only work on exit, but not entry.
 - 1.0.0
   - Drop support for IE < 10
 - 0.4.6
   - You can now pass combined mediaqueries e.g. `(min-width: 320px) and (max-width: 800px)`
   - It also now accepts `[min|max]-aspect-ratio`
 - 0.4.5
   - Passing `mq` to `entry`, `exit`, and `both`
