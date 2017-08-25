NOTE: This is a fork to support dynamicly created elements, such as with jquery. 

For example:

     $("<audio/>", {
                "id": data.id,
                controls: "controls",
                "data-info-album-art": "image.png",
                "data-info-id": data.info.id,
                "data-info-album-title": data.title,
                "data-info-artist": data.artist,
                "data-info-title": data.info.title,
                "data-info-label": data.label, "),
                "data-info-year": data.year,
                "data-info-att": data.attr,
                "data-info-att-link": "/",
                html: "An html5-capable browser is required to play this audio.",
            }).appendTo("#body");

            $("<source>", {
                src: 'my-mp3file.mp3',
                type: "audio/mpeg",
            }).appendTo('#' + data.id);

            // this method initializes the bootstrap3_player
            $("#" + data.id).bootAudio();
            
End.

            

bootstrap3_player
================

An HTML5 Audio Player Skin For Twitter Bootstrap 3

#### Requires:

  * Twitter Bootstrap 3 - http://twitter.github.com/bootstrap/
  * jQuery - http://jquery.com/

#### How to use

Clone or download this repo; then open the included [`index.html`](index.html) file: 
-  with **your browser** to:  
    -  see a live demo on your local machine 
    -  compare it with the [screenshots or live demo](#screenshots) below
- with your [text editor](index.html) to:
    -  see all the css and js files you need to link to
    -  see the `<audio>`  tags in use

#### Styling caveat

Works best when the player is not enclosed in too narrow a container in your page otherwise the player controls can appear jumbled. Both the seek and volume sliders are hidden on narrow (xs) viewports. A good strategy is to start "mobile-first" as usual by enclosing your audio block in a row that uses all twelve grid colums of the page's outer container in an xs viewport. Then, on wider viewports, the player can occupy fewer of the page's grid columns. See the example row widths in  [`index.html`](index.html) and the corresponding [live demo](http://playerdemo.iainhouston.com).   

##### Forked from William Randol's [bootstrap-player](https://github.com/WilliamRandol/bootstrap-player)

 -  `bootstrap-player` is great for Bootstrap 2
 -  All the functionality of William Randol's player is preserved   
 (QUnit / FuncUnit test suite in progress :waxing_crescent_moon:)
 -  `bootstrap3_player` updates the styling of `bootstrap-player`; has fewer dependencies; uses Bootstrap 3

For some info on the differences between `bootstrap-player` and `bootstrap3_player`, [see here.](CHANGES.md)


#### <a name="screenshots">Screenshots and Live demo

[See a live demo](http://playerdemo.iainhouston.com)

-  Audio with no additional data ![](screenshots/bPlayer_demo_data_no.png?raw=true)

-  Audio with data - collapsed ![](screenshots/bPlayer_demo_data_0.png?raw=true)

-  Audio with data - expanded ![](screenshots/bPlayer_demo_data_1.png?raw=true)




