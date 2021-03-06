# AEM Mobile Gestures API for Muse

This Muse Configurable Options Widget (mucow) is a simple way to add the Adobe AEM Mobile Gestures API to Adobe Muse projects, so that tapping the AEMM article will toggle the navigation.

## How To Use

Download the .mucow file, open your Muse project and navigate to the Master page.

`File > Place` the .mucow file into your Master page.

When you export your Muse project to HTML, the JS code for the Gestures API will be added to the end of your index.html file, and tapping the AEMM article should toggle the navigation.

## Considerations

* The JS in the .mucow file targets iOS devices, as tapping on Android devices toggle the navigation without the Gestures API.
* The .mucow file is best placed on the canvas, as placing it off the canvas can result in unexpected dimensions of the HTML article.
* The .mucow file needn't be hidden or otherwise obscured; though a <> icon does appear where the .mucow file is placed in Muse, it will not be visible in the exported HTML.
* The .mucow file has no options.

## About

I developed this widget at [Bates Creative](http://batescreative.com). We are currently using it within our process for creating Adobe AEM Mobile articles in Adobe Muse. We are really happy to be able to share it with the community, as we know there's substantial need to bridge the gap between designer-friendly Adobe Muse and developer-friendly AEM Mobile.

### Disclaimer

This code works for our purposes and will continue to evolve, but it may not work with all Muse project setups or meet all functionality needs.

### Changelog

####v1.5
Changed the event binding such that if .breakpoint exists, the click (tap) event will trigger on that element. Otherwise, it will trigger on the #page element. This should resolve the inconsistency in functionality that existed on iPhone with some articles. Also added more details to the widget options panel.

####v1.4
Added functionality to NOT toggle nav when tapping thumbnails for the built in Muse slideshows.

####v1.3
Changed code to target #page div, rather than .breakpoint, as .breakpoint does not exist in layouts without breakpoints. Reworked code to remove inline onclick event. Added CSS to the #page div to prevent a color flash on tap.

####v1.2
Reworked code to trigger navigation toggle on everything except `<a>links</a>` and `<a><span>links</span></a>`.

####v1.1
Changed code to create the div for the onclick event within each .breakpoint div, as creating it within the body element started to break some articles.
