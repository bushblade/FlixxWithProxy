# Flixx App

Movie info application built with vanilla JavaScript that uses **version 3** of the [TMDB API](https://developers.themoviedb.org/3)

Adapted from a project in Brad Traversy's [ Modern JS From The Beginning 2.0 ](https://www.traversymedia.com/modern-javascript-2-0) course to use Netlify cloud functions to proxy the requests and so hide the API key from the client.

This includes the most popular movies and TV shows with detail pages, a search box for movies and shows with full pagination and a slider for movies that are currently playing in theaters. The slider uses the [Swiper](https://swiperjs.com) library.

## Usage

Install the [Netlify CLI](https://docs.netlify.com/cli/get-started/) globally on
your system.

```bash
npm i -g netlify-cli
```

Clone or download this project and then register for a free API key at [ https://www.themoviedb.org/settings/api ](https://www.themoviedb.org/settings/api)

Once you get your key, create a **.env.local** file in the root of the project
with the following...

```bash
TMDB_API_KEY=replace_with_your_key
TMDB_API_URL=https://api.themoviedb.org/3/

```

### Install functions dependencies

```bash
cd functions
npm i
```

### Run Netlify CLI in the project root

```bash
netlify dev
```

# Deploying to Netlify

- Connect your Netlify account to your Github account
- Create a repository for the project on Github
- From your Netlify panel choose **Add new site -> import an existing project**
- Choose Github
- Find your Flixx app repository
- In **Settings** set your env variables
- Add a build command of `npm i --prefix functions`
