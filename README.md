# AnimeHub

AnimeHub is a simple platform for reviewing and sharing your favorite anime. You can find a demo [here](http://bitex.me/AnimeHub/).

AnimeHub is written using JavaScript which means you can host it on GitHub Pages. Also, it uses the issues of your GitHub repo to store your anime reviews.

## Features

 - No server needed: hosted on GitHub Pages and use your GitHub issues as storage.
 - Anime info and images from [AniList](https://anilist.co/).
 - [GFM (GitHub Flavored Markdown)](https://help.github.com/articles/github-flavored-markdown/) support.

## Installation

 1. Make sure your GitHub Pages is working. You can set it up [here](https://pages.github.com/).
 2. Create a repo on GitHub for your reviews.
 3. Fork this repo.
 4. Create a client and get your ID & secret on [AniList](http://anilist.co/developer). You may need to create an account.
 5. Create and switch to a new branch named `gh-pages` for your forked repo.
 6. Edit the file `config.js`. You should at least put in your username, repo name (the one you created at step 1), AniList client ID and secret.
 7. Commit and push your changes. Your AnimeHub should be available at **http://yourusername.github.io/AnimeHub**.

By default, GitHub has a limit on the API request rate, which is up to 60 requests per hour. If you find it insufficient, you should create an access token for AnimeHub on [this page](https://github.com/settings/tokens). **Do not select any scope when creating your access token**. You will see your newly created token after submitting your generation form and you should copy and paste it into the `config.js`.

## Configurations

You can customize AnimeHub by editing `config.js`.

```javascript
var _config = {

    // Title of your AnimeHub.
    // This will be shown on both page headers and page titles.
    title: 'AnimeHub',

    // Your GitHub username.
    username: '',

    // Your GitHub repo for anime reviews.
    // This can be any repo in your GitHub, even the same as AnimeHub's repo.
    // However, it's required that issues feature must be enabled for this repo.
    repo: '',

    // Which of the issues should be shown? (all / user / label)
    issue_filter: 'all',

    // Issues created by this user will be shown if issue_filter is set to 'user'.
    issue_filter_username: '',

    // Issues with this label will be shown if issue_filter is set to 'label'.
    issue_filter_label: '',

    // Reviews to show per page.
    per_page: 20,

    // Your access token for AnimeHub.
    // By default GitHub limits the API request rate to 60 requests per hour.
    // You can create an access token at https://github.com/settings/tokens to increase the rate.
    // Make sure **not to select any scope** while generating the token. 
    access_token: '',

    // ID of your AniList client.
    // The ID and the secret below is used for API requests from AniList.
    // You need to create a client at http://anilist.co/developer.
    anilist_client_id: '',

    // Secret of your AniList client.
    anilist_client_secret: '',

    // Custom background image.
    background_url: ''

}
```

## Write your reviews

AnimeHub uses your GitHub issues as the storage of your reviews. Title of your issues must be the ID of the anime on AniList. For the present, there isn't a way that you can fetch the anime ID and write the reviews easily. You must get the ID from AniList yourself and write your texts directly in the GitHub issues page. There will soon be an editor feature you can use to search for the anime and write your reviews. 

## Credits

 - [Dev Ideas](https://devideas.github.io/): for an idea that inspired AnimeHub.
 - [wuhaoworld/github-issues-blog](https://github.com/wuhaoworld/github-issues-blog): for the code. It also inspired me that GitHub issues can be of great use.
 - [AniList](https://anilist.co/): for the anime information and images.
 - [Material Design Lite](http://www.getmdl.io/).
 - [Ractive.js](http://www.ractivejs.org/).
 - [Director](https://github.com/flatiron/director).
 - [markdown-js](https://github.com/evilstreak/markdown-js).
 - [GitHub](https://github.com).

## License

AnimeHub is published under MIT License. Find more from the `LICENSE` file.
