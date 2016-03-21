# Gallery Link

This blueprint is based on the blueprint of Veams-Components.

## Requirements 
- `veams-block-overlay`

## Usage

### Include: Page

``` hbs
{{! @INSERT :: START @id: gallery-link, @tag: component }}
{{! WrapWith START: Form Wrapper }}
{{#with gallery-link-bp}}
	{{#wrapWith "c-gallery-link"
	context=options.context
	ajax=options.ajax
	classes=options.classes
	method=options.method
	}}
		{{#each fieldsets}}
			{{> c-gallery-link__fieldset }}
		{{/each}}
	{{/wrapWith}}
{{/with}}
{{! WrapWith END: Form Wrapper }}
{{! @INSERT :: END }}
```

### Include: SCSS

``` scss
// @INSERT :: START @tag: scss-import , @tag: component
@import "components/_c-gallery-link";
// @INSERT :: END
```

### Include: JavaScript

#### Import
``` js
// @INSERT :: START @tag: js-import , @tag: component
import GalleryLink from './modules/gallery-link/gallery-link';
// @INSERT :: END
```

#### Initializing in Veams V2
``` js
// @INSERT :: START @tag: js-init-v2 , @tag: component
/**
 * Init Form
 */
Helpers.loadModule({
	el: '[data-js-module="gallery-link"]',
	module: GalleryLink,
	context: context
});
// @INSERT :: END
```

#### Initializing in Veams V3
``` js
// @INSERT :: START @tag: js-init-v3  , @tag: component
/**
 * Init Form
 */
Helpers.loadModule({
	domName: 'gallery-link',
	module: GalleryLink,
	context: context
});
// @INSERT :: END
```
