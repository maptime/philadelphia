## Maptime Starter site

Hosting your own meetup? Starter is desgined to be easily forked and tweaked to suit your own needs. Starter is a simple Jekyll theme for Maptime meetups. [Jekyll](http://jekyllrb.com/) is a simple, blog-aware, static site generator for personal, project, or organization sites.

## Creating a new chapter

1. [Create a ticket here](https://github.com/maptime/starter/issues/new/). Outline the name of your Maptime chapter and who the organizers are by their GitHub username.
2. Assign the ticket or mention @geografa. He can create a new repository under the Maptime organization account and include your chapter's organizers to administer it.
3. Edit the [`_config.yml`](https://github.com/maptime/starter/blob/gh-pages/_config.yml) file. Here's a quick rundown of the configuration options:

   **Top-level configuration**

   | Name | Required | Value | Description |
   | --- | --- | --- | --- |
   | `baseurl` | Yes | `post` | This value should always be `post`. |
   | `permalink` | No | How URLs are generated | You can learn more about how they are generated [from the Jekyll documentation](http://jekyllrb.com/docs/   permalinks/). |
   | `markdown` | No | Determines which markdown engine is used | Generally, you don't need to touch this field for your own needs. |
   | `paginate` | Yes | Number of posts on the front page | Starter supports pagination. Control the number of posts on a given page by changing this value |
   | `repo` | Yes | Name of the repo on GitHub | As an example, the name of the starter repo is `starter` |
   | `github_org` | Yes | Name of the organization or username on GitHub | Most of the time this will be `maptime` |

   **`maptime:` section configuration**

   | Name | Required | Value | Description |
   | --- | --- | --- | --- |
   | `chapter` | Yes | Name of your Maptime meetup | |
   | `twitter` | No | Your Maptime Twitter username | |
   | `disqus` | No | Disqus account name | Starter optionally supports comments on posts with [Disqus](http://disqus.com). Create a new Disqus account for site and fill this field with the account name. |

4. Commit your changes to `_config.yml` and push to GitHub.

## Content types

There are two kinds of content in Starter: post and event. You author these types of content in the `_posts` directory. Each content type has unique configuration options that you should declare at the top of the document. This is called [Frontmatter](http://jekyllrb.com/docs/frontmatter/).

#### Event
Events are for actual planned meetups with RSVP information. Note that the filename of the post should match the date of the meetup date.

##### Front matter options

| Name | Required | Value | Description |
| --- | --- | --- | --- |
| `layout` | Yes | `event` | This value should always be `event`. |
| `category` | Yes | `event` | This value should always be `event`. |
| `title` | Yes | The title of your event | |
| `rsvp` | Yes | URL to RSVP | This should be a link to  an [Eventbrite](http://eventbrite.com) date or other service. |

#### Posts

Posts are like blog posts. These are great for meetup follow ups or posts that don't have a meetup event tied to it.

##### Front matter options

| Name | Required | Value | Description |
| --- | --- | --- | --- |
| `layout` | Yes | `post` | This value should always be `post`. |
| `title` | Yes | The title of your post | |
| `author` | No | Author's name | |
| `image` | No | URL path to an image | Images added here will show up as a [Twitter card](https://dev.twitter.com/docs/cards) when a post is shared. |

## Creating an event or post

To create an event or post:

1. In the `_posts` directory, create a new Markdown file. Name the file in the pattern of `YYYY-MM-DD-slug.md`, where *YYYY-MM-DD* is the date of the event or post and *slug* is a short, unique identifier for the event or post. For example, a post dated January 1, 2016 entitled "Mappy New Year" might be named `2016-01-01-mappy-new-year.md`.

2. At the top of the Markdown file, add appropriate front matter for your content type. For example:

   ```
   ---
   layout: post
   title: Oceanographic Maps
   author: Marie Tharp
   ---
   ```
3. Beneath the front matter, write your post or event text. For example:

   ```
   Check out the *unusual* features of the __ocean floor__ in this map of…
   ```

4. Preview your post. In a terminal session, run `jekyll serve` from the root directory of this repository. Jekyll will generate the site and provide you with a URL to open in a browser to see your work.

   **Note**: If you get a `command not found` error, Jekyll may not be installed. See Jekyll's [installation instructions](http://jekyllrb.com/docs/installation/) to get up and running.

5. Once you're satisfied with your new event or post, commit the Markdown file and push to GitHub.

   **Note**: If you're using multiple branches, only those changes merged to the `gh-pages` branch will appear on the Maptime site.


## Help resources

- [Create an issue](https://github.com/maptime/starter/issues) on the Starter repo and we'll respond to it.
- The site is powered by Jekyll. To make custom tweaks to your own site, you should read its [documentation](http://jekyllrb.com/docs/home/).
- Starter makes the assumption you will be running the site on GitHub pages. You can learn more about [GitHub Pages here](https://guides.github.com/features/pages/).

## Examples in the wild

Have you used this starter to create your own meetup site? Let us know and we can add it below!

- [MaptimeDC](https://maptime.github.io/dc/)
- [MaptimeTO](https://maptime.github.io/toronto/)

## Licence

BSD
