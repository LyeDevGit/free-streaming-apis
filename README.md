# Free Streaming APIs

> A comprehensive, community-maintained list of **free movie, TV & anime streaming APIs** for developers. These APIs provide embeddable video players, streaming links, and metadata — no hosting required.

**Last updated:** August 2026

> **Disclaimer:** This list is for educational and research purposes only. Always respect copyright laws and the terms of service of any provider. This repository does not host, stream, or distribute any copyrighted content.

---

## Table of Contents

- [Stream Embed APIs (Video Playback)](#-stream-embed-apis-video-playback)
- [Multi-Server Providers](#-multi-server-providers)
- [Self-Hosted / Scraper APIs](#-self-hosted--scraper-apis)
- [Anime Streaming APIs](#-anime-streaming-apis)
- [Metadata APIs (Movie & TV Info)](#-metadata-apis-movie--tv-info)
- [Streaming Availability APIs](#-streaming-availability-apis)
- [Subtitle APIs](#-subtitle-apis)
- [Feature Comparison](#-feature-comparison)
- [Quick Start Examples](#-quick-start-examples)
- [Related Projects](#-related-projects)
- [Contributing](#-contributing)

---

## Stream Embed APIs (Video Playback)

These APIs provide actual video embeds and streaming links. Drop an iframe and you're done.

| Provider | URL(s) | ID Type | Status |
|----------|--------|---------|--------|
| **VidSrc** | [vidsrc.to](https://vidsrc.to), [vidsrc.me](https://vidsrc.me), [vidsrc.xyz](https://vidsrc.xyz), [vidsrc.cx](https://vidsrc.cx), [vid-src.top](https://vid-src.top) | TMDB/IMDB | Active |
| **2Embed** | [2embed.online](https://www.2embed.online), [2embed.cc](https://2embed.cc) | TMDB/IMDB | Active |
| **SuperEmbed** | [superembed.stream](https://www.superembed.stream), [multiembed.mov](https://multiembed.mov) | TMDB/IMDB | Active |
| **MoviesAPI** | [moviesapi.to](https://moviesapi.to) | TMDB/IMDB | Active |
| **VidSpark** | [vidspark.to](https://vidspark.to) | TMDB/IMDB | Active |
| **EmbedMaster** | [embedmaster.com](https://embedmaster.com) | TMDB/IMDB | Active |
| **ezvidapi** | [ezvidapi.com](https://ezvidapi.com) | TMDB | Active |
| **ApiPlayer** | [apiplayer.ru](https://apiplayer.ru) | TMDB/IMDB | Active |
| **embed.su** | [embed.su](https://embed.su) | TMDB/IMDB | Active |
| **vidlink.pro** | [vidlink.pro](https://vidlink.pro) | TMDB | Active |
| **VidBinge** | [vidbinge.to](https://vidbinge.to) | TMDB | Active |
| **VidRock** | [vidrock.ru](https://vidrock.ru) | TMDB | Active |
| **VidFlix** | [vidflix.club](https://vidflix.club) | TMDB | Active |

---

## Multi-Server Providers

These providers aggregate multiple streaming servers in one embed — if one server goes down, another takes over.

| Provider | URL(s) | ID Type | Servers |
|----------|--------|---------|---------|
| **VidCore** | [vidcore.org](https://vidcore.org), [vidcore.net](https://www.vidcore.net) | TMDB | Multiple with failover |
| **ScreenScape** | [screenscape.me](https://screenscape.me) | TMDB/IMDB | Multiple |
| **VidLux** | [vidlux.xyz](https://vidlux.xyz) | TMDB | Multiple |
| **CinemaOS** | [cinemaos.live](https://cinemaos.live) | TMDB | Multiple |
| **RiverStream** | [rivestream.app](https://www.rivestream.app) | TMDB | Multiple |
| **TouStream** | [toustream.xyz](https://toustream.xyz) | TMDB | Multiple |
| **SpencerDevs** | [spencerdevs.xyz](https://spencerdevs.xyz) | TMDB | Multiple |
| **wfs.lol** | [wfs.lol](https://wfs.lol) | TMDB | Multiple |

---

## Self-Hosted / Scraper APIs

These are open-source projects you can self-host. They scrape multiple streaming sites and return stream URLs.

| Project | GitHub | Stars | Description |
|---------|--------|-------|-------------|
| **TMDB-Embed-API** | [Inside4ndroid/TMDB-Embed-API](https://github.com/Inside4ndroid/TMDB-Embed-API) | 125+ | Multi-provider stream aggregation with admin panel |
| **CinePro** | [cinepro-org/core](https://github.com/cinepro-org/core) | 135+ | Multi-site scraper, 50+ unique playable sources |
| **vidsrc.ts** | [cool-dev-guy/vidsrc.ts](https://github.com/cool-dev-guy/vidsrc.ts) | 110+ | VidSrc extractor in TypeScript |
| **vidsrc-bypass** | [heyitswit/vidsrc-bypass](https://github.com/heyitswit/vidsrc-bypass) | 29+ | Embed.su, VidSrc, Vidlink bypass wrapper |
| **MediaVanced** | [yogesh-hacker/MediaVanced](https://github.com/yogesh-hacker/MediaVanced) | 79+ | Parse media links from various streaming sites |
| **vidstream-api** | [WBRK-dev/vidstream-api](https://github.com/WBRK-dev/vidstream-api) | 30+ | VidStream/FlixHQ scraper with RabbitStream parser |
| **flixhq-core** | [shin202/flixhq-core](https://github.com/shin202/flixhq-core) | 33+ | FlixHQ data extraction library |
| **vidsrc-scraper** | [DivineChile/vidsrc-scraper](https://github.com/DivineChile/vidsrc-scraper) | 31+ | Node.js VidSrc scraper, works on all domains |
| **2embed-api** | [parnexcodes/2embed-api](https://github.com/parnexcodes/2embed-api) | 26+ | Get HLS streams from 2Embed |

---

## Anime Streaming APIs

| Provider | URL / GitHub | Type | Notes |
|----------|-------------|------|-------|
| **AniKoto API** | [anikototvapi.vercel.app](https://anikototvapi.vercel.app/) | REST | 30+ endpoints, no API key |
| **MiruroAPI** | [Shineii86/MiruroAPI](https://github.com/Shineii86/MiruroAPI) | REST | 46 endpoints, 12 streaming providers, M3U8 |
| **Shirayuki API** | [Anandadevnath/Shirayuki-Anime-API](https://github.com/Anandadevnath/Shirayuki-Anime-API) | REST | Multi-provider scraper (MegaCloud, VidSrc) |
| **Anime Streaming (RapidAPI)** | [rapidapi.com](https://rapidapi.com/adarsh.chouhan11/api/anime-streaming) | REST | 300 req/min free, M3U8/HLS sources |
| **AniList GraphQL** | [docs.anilist.co](https://docs.anilist.co/) | GraphQL | Metadata + recommendations (no streams) |
| **Jikan** | [docs.api.jikan.moe](https://docs.api.jikan.moe/) | REST | MyAnimeList data wrapper, no API key |
| **Kitsu** | [kitsu.docs.apiary.io](https://kitsu.docs.apiary.io/) | JSON:API | Anime + manga, no API key |

---

## Metadata APIs (Movie & TV Info)

These provide titles, ratings, posters, cast — but not actual video streams.

| API | URL | Free Tier | Auth | Best For |
|-----|-----|-----------|------|----------|
| **TMDB** | [themoviedb.org](https://www.themoviedb.org) | Yes (attribution required) | API Key | Images, credits, discovery, trending |
| **OMDb** | [omdbapi.com](http://www.omdbapi.com) | 1,000 req/day | API Key | Simple IMDb-style lookup |
| **TVmaze** | [tvmaze.com/api](https://www.tvmaze.com/api) | Yes | None | TV shows, episodes, schedules |
| **Trakt** | [trakt.docs.apiary.io](https://trakt.docs.apiary.io) | Yes | OAuth | Watch history, ratings, lists |
| **Simkl** | [simkl.docs.apiary.io](https://simkl.docs.apiary.io) | Yes | API Key | Movies, TV, anime tracking |
| **TasteDive** | [tastedive.com/read/api](https://tastedive.com/read/api) | Yes | API Key | Content recommendations |
| **Kitsu** | [kitsu.docs.apiary.io](https://kitsu.docs.apiary.io/) | Yes | None | Anime-specific |
| **IMDb (API.market)** | [api.market](https://api.market/store/sleeyax/imdb) | Free trial | API Key | Enterprise-grade IMDb data |
| **MoviesDatabase** | [rapidapi.com](https://rapidapi.com) | Freemium | API Key | 9M+ titles, 11M+ cast members |

---

## Streaming Availability APIs

These tell you *where* a movie is available to stream (Netflix, Hulu, etc.) — not actual streams.

| API | URL | Free Tier | Notes |
|-----|-----|-----------|-------|
| **Watchmode** | [api.watchmode.com](https://api.watchmode.com) | Yes | Platform/region filters, deep links |
| **TMDB Watch Providers** | [developer.themoviedb.org](https://developer.themoviedb.org) | Yes | Via JustWatch partnership |
| **JustWatch** | [justwatch.com](https://www.justwatch.com) | Paid | Most comprehensive availability data |

---

## Subtitle APIs

| Provider | URL | Notes |
|----------|-----|-------|
| **Wyzie Subs** | [sub.wyzie.ru](https://sub.wyzie.ru) | Subtitle scraping API, used by millions |

---

## Feature Comparison

### Stream Embed APIs

| Provider | TMDB | IMDB | TV Shows | Anime | Subtitles | HLS | Multi-Server | API Key | Free |
|----------|------|------|----------|-------|-----------|-----|--------------|---------|------|
| VidSrc | ✅ | ✅ | ✅ | ❌ | ✅ | Partial | ❌ | No | ✅ |
| 2Embed | ✅ | ✅ | ✅ | ✅ | Partial | Partial | ❌ | No | ✅ |
| SuperEmbed | ✅ | ✅ | ✅ | Partial | Partial | Partial | ✅ | No | ✅ |
| VidCore | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | No | ✅ |
| EmbedMaster | ✅ | ✅ | ✅ | ❌ | ✅ | ✅ | ✅ | Yes | Freemium |
| ezvidapi | ✅ | ❌ | ✅ | ✅ | ❌ | ✅ | ✅ | No | ✅ |
| CinemaOS | ✅ | ❌ | ✅ | ✅ | Partial | ✅ | ✅ | No | ✅ |

### Metadata APIs

| Provider | Movies | TV | Images | Cast | Search | Discovery | Free |
|----------|--------|-----|--------|------|--------|-----------|------|
| TMDB | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| OMDb | ✅ | Partial | ✅ | Partial | ✅ | ❌ | ✅ |
| TVmaze | ❌ | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |
| Trakt | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ | ✅ |
| Simkl | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

---

## Quick Start Examples

### 2Embed (Easiest)

**Movie:**
```html
<iframe src="https://www.2embed.online/embed/movie/tt23779058" allowfullscreen></iframe>
```

**TV Show:**
```html
<iframe src="https://www.2embed.online/embed/tv/205715/1/1" allowfullscreen></iframe>
```

### VidSrc

**Movie:**
```html
<iframe src="https://vidsrc.to/embed/movie/927085" allowfullscreen></iframe>
```

**TV Show (specific episode):**
```html
<iframe src="https://vidsrc.to/embed/tv/158876/1/5" allowfullscreen></iframe>
```

**Custom subtitles:**
```
https://vidsrc.to/embed/movie/{id}?sub_file=https://example.com/subs.vtt&sub_label=English
```

### SuperEmbed

**Movie (IMDB):**
```html
<iframe src="https://multiembed.mov/?video_id=tt8385148" allowfullscreen></iframe>
```

**Movie (TMDB):**
```html
<iframe src="https://multiembed.mov/?video_id=522931&tmdb=1" allowfullscreen></iframe>
```

**VIP player (multi-quality, HLS, subtitles):**
```html
<iframe src="https://multiembed.mov/directstream.php?video_id=tt6791350" allowfullscreen></iframe>
```

### VidCore

```html
<iframe src="https://vidcore.created.app/embed/movie/603" width="100%" height="600" allowfullscreen></iframe>
```

### CinemaOS (Multi-Server)

```html
<iframe src="https://cinemaos.tech/embed" allowfullscreen></iframe>
```

---

## Related Projects

| Project | Description |
|---------|-------------|
| [best-vidsrc-alternative](https://github.com/samratt5/best-vidsrc-alternative) | Compare VidSrc alternatives |
| [TMDB-Embed-API](https://github.com/Inside4ndroid/TMDB-Embed-API) | Self-hosted multi-provider stream aggregator |
| [CinePro](https://github.com/cinepro-org/core) | Multi-site stream scraper (50+ sources) |
| [vidsrc-bypass](https://github.com/heyitswit/vidsrc-bypass) | Bypass/wrapper for multiple providers |
| [MiruroAPI](https://github.com/Shineii86/MiruroAPI) | Anime streaming API with 12 providers |
| [wyzie-subs](https://github.com/wyziedevs/wyzie-subs) | Libre subtitle scraper API |

---

## Contributing

Found an API not listed? Open a PR or [issue](../../issues)!

When contributing, please include:
- Provider name and URL
- Whether it requires an API key
- ID type supported (TMDB, IMDB, or both)
- Whether it's currently working

---

## License

This list is provided as-is for educational purposes. Use responsibly and respect copyright laws.
