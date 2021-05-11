# Regex Lib

## Setup.typoscript
```json
lib.wrapCM = TEXT
lib.wrapCM {
    current = 1
    stdWrap.replacement {
        10 {
            search = #(\d+\scm)#i
            replace = <div class="no-break">${1}</div>
            useRegExp = 1
        }
    }
}
```

## Augabe im Template
```xml
{product.name -> f:cObject(typoscriptObjectPath: 'lib.wrapCM')}
```

# Maxwidth for Fluid styled TextPic
``` json
styles.content.textmedia.maxWInText = 1200
styles.content.image.maxWInText = 1200
```


# Image enlarge OnClick

## Constants.txt

```json
styles.content.textmedia.linkWrap.lightboxCssClass = lightbox
styles.content.textmedia.linkWrap.lightboxEnabled = 1
```

## Setup.txt
```json
lib.fluidContent.settings.media.popup.linkParams.ATagParams {
    dataWrap = title="{field:imagecaption}" class="{$styles.content.textmedia.linkWrap.lightboxCssClass}" rel="{$styles.content.textmedia.linkWrap.lightboxRelAttribute}"
}
```