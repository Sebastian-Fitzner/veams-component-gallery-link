# Gallery

This blueprint is based on the blueprint of Veams-Components.

## Requirements 
- `veams-block-overlay`

## Usage

### Include: Page

``` hbs
{{! @INSERT :: START @id: gallery, @tag: component }}
{{! WrapWith START: Form Wrapper }}
{{#with gallery-bp}}
	{{#wrapWith "c-gallery"
	context=options.context
	ajax=options.ajax
	classes=options.classes
	method=options.method
	}}
		{{#each fieldsets}}
			{{> c-gallery__fieldset }}
		{{/each}}
	{{/wrapWith}}
{{/with}}
{{! WrapWith END: Form Wrapper }}
{{! @INSERT :: END }}
```

### Include: SCSS

``` scss
// @INSERT :: START @tag: scss-import , @tag: component
@import "components/_c-gallery";
// @INSERT :: END
```

### Include: JavaScript

#### Import
``` js
// @INSERT :: START @tag: js-import , @tag: component
import Gallery from './modules/gallery/gallery';
// @INSERT :: END
```

#### Initializing in Veams V2
``` js
// @INSERT :: START @tag: js-init-v2 , @tag: component
/**
 * Init Gallery
 */
Helpers.loadModule({
	el: '[data-js-module="gallery"]',
	module: Gallery,
	context: context
});
// @INSERT :: END
```

#### Initializing in Veams V3
``` js
// @INSERT :: START @tag: js-init-v3  , @tag: component
/**
 * Init Gallery
 */
Helpers.loadModule({
	domName: 'gallery',
	module: Gallery,
	context: context
});
// @INSERT :: END
```

#### Custom Events
``` js
// @INSERT :: START @tag: js-events //
/**
 * Events Gallery
 */
EVENTS.gallery = {
	open: 'gallery:open'
};
// @INSERT :: END
```
