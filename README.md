Products with multi-level variants
==================================

**This project has been moved to https://launchpad.net/zoook-esale**


OpenERP is already supporting a product variants at the core level. But
without this module, variants are only mono-axial. OpenERP indeed uses the product.template
as the model object and the product.variant as the instance variant.
Using this module, you can now easily deal with multi-axial variants.

This software was original writed by **Tiny** and **Akretion** for OpenERP 6.x, and
was patched by **Enterprise Objects Consulting** to be more compatible
with **OpenERP 6.1**, and fix some issues.

Also the code generator was modified:

    [_'-'.join([x.option_id.name[:3].upper() for x in o.dimension_value_ids] or [o.code or 'CONF'])_]

The product reference now is parsed with the 3 first upper digits of the dimensions,
and the originals product.product who had no null code are not changed to 'CONF' value. 

This sources are available in https://github.com/eoconsulting/product_variant_multi

__________

[Enterprise Objects Consulting](http://www.eoconsulting.com.ar)
