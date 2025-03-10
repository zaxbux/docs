# | app

The `| app` filter returns an address relative to the public path of the website. The result is an absolute URL, including the domain name and protocol, to the location specified in the filter parameter. The filter can be applied to any path.

>**NOTE**: If an absolute URL is passed to this filter it will be returned unmodified. Only relative URLs are turned into absolute URLs relative to the web root.

```twig
<link rel="icon" href="{{ '/favicon.ico' | app }}" />
```

If the website address is __https://example.com__ the above example would output the following:

```html
<link rel="icon" href="https://example.com/favicon.ico" />
```

>**NOTE**: When linking to static assets it is recommended to use the [`| asset`](filter-asset) filter instead.

It can also be used for static URLs:

```twig
<a href="{{ '/about-us' | app }}">
    About Us
</a>
```

The above would output:

```html
<a href="https://example.com/about-us">
    About us
</a>
```

> **NOTE**: The `| page` filter is recommended for linking to other pages.
