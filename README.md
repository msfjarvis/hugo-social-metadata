# hugo-social-metadata

## About

This is a [Hugo](https://gohugo.io) theme component that automatically generates metadata complying to [The Open Graph Protocol](https://ogp.me/) as well as [Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/getting-started). This is **NOT** a standalone theme and must not be treated as such.

## Usage

1. Add the hugo-social-metadata repository as a submodule to be able to get upstream changes later `git submodule add https://github.com/msfjarvis/hugo-social-metadata.git themes/hugo-social-metadata`

2. Start off by configuring a few things in your `config.toml` (or equivalent file depending on whether you use YAML or JSON). These will be picked up by the theme component and used to provide metadata for the site.

```toml
[params]
  description = "A description for your awesome website goes here"
  keywords = "some, keywords, that, describe, your, content"
  twitterUsername = "@your_twitter_username"
  socialImage = "path/to/the/twitter/card/image"
```

3. Include the `social_metadata.html` partial in your `head.html` like so: `{{ partial "social_metadata.html" . }}`.

## Additional customizations

You can customize some of the generated metadata on a per-page basis. Setting `description`, `socialImage` or `tags` in the frontmatter will override the defaults loaded from the main config file.

```markdown
+++
description = "A nice description for this blogpost"
socialImage = "path/to/an/image/that/describes/this/post/best"
tags = ["this", "blog", "rocks!"]
+++
```

## License

Check out the [LICENSE](/LICENSE) file in the root of this repository.
