# AnimeHub

AnimeHub is a simple platform for reviewing and sharing your favorite anime. You can find a demo [here](http://bitex.me/AnimeHub/).

AnimeHub is written using JavaScript and [Ractive.js](http://www.ractivejs.org/) which means you can host it on GitHub Pages. Also, it uses the issues of your GitHub repo to store your anime reviews.

## Installation

 1. Make sure your GitHub Pages is working. You can set it up [here](https://pages.github.com/).
 2. Create a repo on GitHub for your reviews.
 3. Fork this repo.
 4. Create a client and get your ID & secret on [AniList](http://anilist.co/developer). You may need to create an account.
 5. Create and switch to a new branch named `gh-pages` for your forked repo.
 6. Edit the file `config.js`. You should at least put in your username, repo name (the one you created at step 1), AniList client ID and secret.
 7. Commit and push your changes. Your AnimeHub should be available at **http://yourusername.github.io/AnimeHub**.

By default, GitHub has a limit on the API request rate, which is up to 60 requests per hour. If you find this rate insufficient, you should create an access token on [this page](https://github.com/settings/tokens). **Deselect all the scopes when creating your access token**. You will see your newly created token after submitting your generation form and you should copy and paste it in the `config.js`.

## Write your reviews

AnimeHub uses your GitHub issues as the storage of your reviews. Title of your issues must be the ID of the anime on AniList. For the present, there isn't a way that you can fetch the anime ID and write the reviews easily. You must get the ID from AniList your self and write your texts directly in the GitHub issues page. There will soon be a editor feature you can use to search for the anime and write your reviews. 

## Credits

AnimeHub was inspired by an idea from [Dev Ideas](https://devideas.github.io/). It's a great email newsletter for insteresting dev ideas.

This project uses the anime information and images from [AniList](https://anilist.co/).

Material Design tastes good and [Material Design Lite](http://www.getmdl.io/) is a great bunch of tools.

And of course, thanks [GitHub](https://github.com/) for the tremendous service.

## License

AnimeHub is published under MIT License. Find more from the `LICENSE` file.
