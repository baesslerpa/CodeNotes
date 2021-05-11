## FAL as Background Image

```html
{v:content.resources.fal(field: 'bgImg', uid: '{record.uid}') -> v:iterator.first() -> v:variable.set(name: 'bgImg')}

<div class="bg-img" style="background-image: url({f:uri.image(src: '{bgImg.id}', treatIdAsReference: 1)})"></div>
```

## Content Element rendern

```xml
<v:content.render contentUids="{0: settings.element.uid}"/>
```

## Assets Viewhelper

```xml
<v:asset.script path="EXT:extname/Resources/Public/JavaScript/Dist/file.js" />
```

## Link Input
```xml
<flux:field.input name="target" label="Link" config="{ renderType: 'inputLink' }"/>
```

## Action Link
```xml

```
