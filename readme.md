# Infoscape

A 2002 experimental "proof of concept" web-delivered 3D visualisation interface for multiple information sources originally using VRML. The original plan was to convert it to X3D, but on advice, this is not necessary as the [Web 3D Consortium](https://www.web3d.org/) recognises both VRML and X3D as current valid formats.

The data was about arts- and disability-related organisations in the East Midlands, U.K. and received Arts Council England funding from 2003-4.

From 2020, the aim is to update it to be accessible in modern browsers.

## TO DO

- [ ] update all XHTML to HTML5
- [ ] fix CORS issue JS alert in Bamboozle Theatre Company (see manifest.js)
- [ ] recreate "details.html", "disarts.html" in a new data structure
- [ ] refactor pop-up windows in 'Anchor' tags into in-page modals
- [ ] check through Andreas' [Gitter messages](gitter-text.md)

## DONE

- [x] fix duplicated "info.css"
- [x] FAIL: Bamboozle Theatre Company CORS alert with manifest.js permissions
- [x] integrate Adreas' changes to t1.wrl
- [x] (REDUNDANT) complete VRML-X3D conversion… and break this up into separate jobs
- [x] Try the X_ITE javascript-WebGL library

---

## Resources

- [Convert everything to X3D](https://castle-engine.io/convert.php) ([supported models](https://castle-engine.io/creating_data_model_formats.php))
- [chrome.permissions](https://developer.chrome.com/apps/permissions#manifest)
- [How can I trigger JavaScript in a VRML Anchor—is it possible to use an Event Listener?](https://stackoverflow.com/q/60027233/123033)
- [Answer to "Where are the issues in this conversion from VRML to X3D?"](https://stackoverflow.com/a/60004540/123033)
- [X_ITE javascript-WebGL library](http://create3000.de/x_ite/getting-started/#embedding-x-ite-within-a-web-page)
- [X3Dv4 Highlights](https://www.web3d.org/x3dv4-highlights)
- [VRML V2.0 Editing Kit for VSCode](https://github.com/up-tri/vrml-v2.0-kit)
- [Embedding X_ITE within a Web Page](http://create3000.de/x_ite/getting-started/#embedding-x-ite-within-a-web-page)

## Temporary

- [VRML Anchor Node](http://lighthouse3d.com/vrml/tutorial/index.shtml?anchor)
- [Accessing the External Browser](http://create3000.de/x_ite/accessing-the-external-browser/)
- [x3dom/LOBBY](https://gitter.im/x3dom/LOBBY#)
- [Mailing List: x3dom-users](https://sourceforge.net/projects/x3dom/lists/x3dom-users)
- [Using HTML Elements in a Canvas](http://www.informit.com/articles/article.aspx?p=1903884&seqNum=8)
- [JSON Validator](https://www.jsonschemavalidator.net/)

    <!-- "*://127.0.0.1:5500/*", -->
