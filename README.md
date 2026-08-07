# Free Movie Streaming APIs

A comprehensive list of free movie streaming APIs for developers. These APIs provide embeddable video players and streaming links for movies and TV shows.

> **Disclaimer:** This list is for educational purposes. Always respect copyright laws and terms of service.

---

## Table of Contents

- [Embed/Streaming APIs (Video Playback)](#embedstreaming-apis-video-playback)
- [Metadata APIs (Movie Information)](#metadata-apis-movie-information)
- [Streaming Availability APIs](#streaming-availability-apis)

---

## Embed/Streaming APIs (Video Playback)

These APIs provide actual video embeds and streaming links for movies and TV shows.

| API | URL | ID Type | Notes |
|-----|-----|---------|-------|
| **VidSrc** | [vidsrc.to](https://vidsrc.to) | TMDB/IMDB | Popular, multiple domains (vidsrc.me, vidsrc.xyz, vidsrc.cx) |
| **2Embed** | [2embed.online](https://www.2embed.online) | TMDB/IMDB | Free, responsive player, auto-updates links |
| **SuperEmbed** | [superembed.stream](https://www.superembed.stream) | IMDB/TMDB | Free, multiple servers, customizable player |
| **MoviesAPI** | [moviesapi.to](https://moviesapi.to) | TMDB/IMDB | High-performance, since 2023 |
| **VidSpark** | [vidspark.to](https://vidspark.to) | TMDB/IMDB | Alternative to VidSrc and 2Embed |
| **VidCore** | [vidcore.org](https://vidcore.org) | TMDB | Developer-focused, anime support, subtitles |
| **ezvidapi** | [ezvidapi.com](https://ezvidapi.com) | TMDB | Multi-provider failover, ad-free, direct HLS URLs |
| **Multiembed** | [multiembed.mov](https://multiembed.mov) | IMDB/TMDB | Works with various CMS templates |
| **embed.su** | [embed.su](https://embed.su) | TMDB/IMDB | Alternative embed provider |
| **vidlink.pro** | [vidlink.pro](https://vidlink.pro) | TMDB | Video link provider |
| **CinePro** | [cinepro.cc](https://cinepro.cc) | TMDB | Multi-site scraper, 50+ sources |

### Usage Examples

**2Embed - Movie:**
```html
<iframe src="https://www.2embed.online/embed/movie/tt23779058" allowfullscreen></iframe>
```

**2Embed - TV Show:**
```html
<iframe src="https://www.2embed.online/embed/tv/1396/1/1" allowfullscreen></iframe>
```

**VidSrc - Movie:**
```html
<iframe src="https://vidsrc.to/embed/movie/27205" allowfullscreen></iframe>
```

**VidSrc - TV Show:**
```html
<iframe src="https://vidsrc.to/embed/tv/1396/1/1" allowfullscreen></iframe>
```

**SuperEmbed - Movie:**
```html
<iframe src="https://multiembed.mov/?video_id=tt8385148" allowfullscreen></iframe>
```

**VidCore - Movie:**
```html
<iframe src="https://vidcore.created.app/embed/movie/603" allowfullscreen></iframe>
```

---

## Metadata APIs (Movie Information)

These APIs provide movie/TV metadata (titles, ratings, posters, cast) but not actual video streams.

| API | URL | Free Tier | Notes |
|-----|-----|-----------|-------|
| **TMDB** | [themoviedb.org](https://www.themoviedb.org) | Yes (with attribution) | Most popular, images, credits, discovery |
| **OMDb** | [omdbapi.com](http://www.omdbapi.com) | 1,000 req/day | Simple IMDb-style lookup |
| **TVmaze** | [tvmaze.com](https://www.tvmaze.com/api) | Yes (free, no key) | TV shows, episodes, schedules |
| **Trakt** | [trakt.docs.apiary.io](https://trakt.docs.apiary.io) | Yes (with OAuth) | Watch history, ratings, lists, recommendations |
| **Simkl** | [simkl.docs.apiary.io](https://simkl.docs.apiary.io) | Yes | Movies, TV, anime, user tracking |
| **TasteDive** | [tastedive.com/read/api](https://tastedive.com/read/api) | Yes | Content-based recommendations |
| **Kitsu** | [kitsu.docs.apiary.io](https://kitsu.docs.apiary.io) | Yes (free, no key) | Anime-specific |
| **IMDb API (API.market)** | [api.market/store/sleeyax/imdb](https://api.market/store/sleeyax/imdb) | Free trial | Paid after trial ($5/mo+) |

---

## Streaming Availability APIs

These APIs tell you *where* a movie is available to stream (not actual streams).

| API | URL | Notes |
|-----|-----|-------|
| **Watchmode** | [api.watchmode.com](https://api.watchmode.com) | Platform/region filters, deep links |
| **TMDB Watch Providers** | [developer.themoviedb.org](https://developer.themoviedb.org) | Via JustWatch partnership |
| **JustWatch** | [justwatch.com](https://www.justwatch.com) | Paid API, comprehensive availability |

---

## Related Projects

- [best-vidsrc-alternative](https://github.com/samratt5/best-vidsrc-alternative) - Compare VidSrc alternatives
- [vidsrc-api](https://github.com/topics/vidsrc-api) - VidSrc API projects on GitHub

---

## Contributing

Found an API not listed? Open a PR or issue!

---

## License

This list is provided as-is for educational purposes. Use responsibly.
