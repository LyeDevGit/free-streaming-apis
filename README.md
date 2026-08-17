# Free Streaming APIs

A working list of free movie, TV and anime streaming APIs for developers. Every entry here
was checked by hand from a real machine — no copy-pasting from other lists. If something is
down, it's either moved to the graveyard section at the bottom or already removed.

These APIs give you embeddable players, stream links and metadata so you can build things
without hosting a single video file.

**Last verified:** August 2026 (checked one by one with curl against real TMDB/IMDB IDs)

Fair warning: this is for learning and personal projects. Streaming sites come and go, some
run heavy ads, and none of it is guaranteed to stay up. Respect copyright laws in your
country and the terms of any service you use. This repo hosts nothing — it's just a list.

---

## Table of Contents

- [Embed APIs](#embed-apis-video-playback) — drop an iframe, get a player
- [Multi-Server Providers](#multi-server-providers) — built-in failover between servers
- [Self-Hosted & Scrapers](#self-hosted--scraper-apis) — open-source, run it yourself
- [Anime APIs](#anime-streaming-apis)
- [Metadata APIs](#metadata-apis-movie--tv-info) — titles, posters, cast (no video)
- [Where-to-Watch APIs](#streaming-availability-apis)
- [Subtitle APIs](#subtitle-apis)
- [Stremio Ecosystem](#stremio-ecosystem)
- [Feature Comparison](#feature-comparison)
- [Quick Start](#quick-start-examples)
- [Graveyard](#graveyard-checked-and-dead) — things that no longer work
- [How I test](#how-i-test-this-stuff)
- [Contributing](#contributing)

Status legend: ✅ working right now · ⚠️ works but with caveats · ❌ dead — see graveyard

---

## Embed APIs (Video Playback)

The bread and butter of this list. Point an iframe at one of these URLs with a TMDB or IMDB
id and it plays.

| Provider | URL(s) | ID Type | Status | Notes |
|----------|--------|---------|--------|-------|
| **VidSrc** | [vidsrc.to](https://vidsrc.to) | TMDB/IMDB | ✅ | The original. Still serving embeds fine |
| **VidSrc (me)** | [vidsrcme.ru](https://vidsrcme.ru) | TMDB/IMDB | ✅ | vidsrc.me now redirects here |
| **vidsrc.in** | [vidsrc.in](https://vidsrc.in) | TMDB/IMDB | ✅ | Wraps vsembed.ru, serves real embeds |
| **vidsrc.io** | [vidsrc.io](https://vidsrc.io) | TMDB/IMDB | ✅ | Full-page player, TV support verified |
| **vidsrc.pm** | [vidsrc.pm](https://vidsrc.pm) | TMDB/IMDB | ✅ | Confirmed serving embeds |
| **vsembed.ru** | [vsembed.ru](https://vsembed.ru) | TMDB/IMDB | ✅ | Same backend as vidsrc.in |
| **vid-src.top** | [vid-src.top](https://vid-src.top) | TMDB/IMDB | ✅ | Big player payload, still healthy |
| **2Embed** | [2embed.cc](https://www.2embed.cc) | TMDB/IMDB | ✅ | Most reliable of the 2Embed family |
| **2Embed (.cc)** | [2embed.online](https://www.2embed.online) | TMDB/IMDB | ⚠️ | Redirects to 2embed.stream which flakes with 522s occasionally |
| **SuperEmbed** | [superembed.stream](https://www.superembed.stream), [multiembed.mov](https://multiembed.mov) | TMDB/IMDB | ✅ | multiembed.mov redirects to streamingnow.mov — this is normal, embeds still resolve |
| **moviesapi.to** | [moviesapi.to](https://moviesapi.to) | TMDB | ✅ | Path changed: use `/movie/{id}` not `/embed/movie/{id}` |
| **VidSpark** | [vidspark.to](https://vidspark.to) | TMDB | ✅ | Same codebase as moviesapi.to, `/movie/{id}` works |
| **embed.su** | [www.embed.su](https://www.embed.su) | TMDB/IMDB | ✅ | Note the `www.` — the apex domain stopped resolving |
| **vidlink.pro** | [vidlink.pro](https://vidlink.pro) | TMDB | ✅ | `/movie/{id}` and `/tv/{id}/{s}/{e}` both verified. JSON responses need a key |
| **vidfast** | [vidfast.vc](https://vidfast.vc) | TMDB | ✅ | New addition. Next.js player at `/movie/{id}`, TV at `/tv/{id}/{s}/{e}` |
| **EmbedMaster** | [embedmaster.com](https://embedmaster.com) | TMDB/IMDB | ⚠️ | Site is up but everything sits behind a login/API key now |
| **VidRock** | [vidrock.ru](https://vidrock.ru) | TMDB | ✅ | Loads an ad script (acscdn) before the player — worth knowing |
| **VidFlix** | [vidflix.club](https://vidflix.club) | TMDB | ✅ | SPA, embeds resolve client-side |
| **vidbinge** | [vidbinge.com](https://vidbinge.com) | TMDB | ⚠️ | vidbinge.to is dead; the .com works but runs fingerprint/bot-check redirects |
| **vidsrc.nl** | [vidsrc.nl](https://vidsrc.nl) | TMDB | ⚠️ | Same bot-challenge wrapper as vidbinge |

> Heads up on vidsrc.xyz, vidsrc.cx, vidsrc.me: those domains are gone (see graveyard).
> If your code hardcodes them, swap to vidsrc.to or the mirrors above.

---

## Multi-Server Providers

These cycle through a stack of upstream servers, so if one dies mid-stream another picks
up. Handy if you don't want to write your own failover logic.

| Provider | URL(s) | ID Type | Status | Notes |
|----------|--------|---------|--------|-------|
| **VidCore** | [vidcore.org](https://vidcore.org), [vidcore.net](https://www.vidcore.net) | TMDB | ✅ | Works on both domains. The old `vidcore.created.app` URL from docs is dead — don't use it. JS "one moment please" gate on first hit, normal |
| **vidlux** | [vidlux.xyz](https://vidlux.xyz) | TMDB | ✅ | Solid embed responses |
| **toustream** | [toustream.xyz](https://toustream.xyz) | TMDB | ✅ | Movies, TV and anime |
| **wfs.lol** | [wfs.lol](https://wfs.lol) | TMDB | ✅ | Embeds actually live on embed.wfs.lol (auto-redirect) |
| **CinemaOS** | [cinemaos.live](https://cinemaos.live), [cinemaos.tech](https://cinemaos.tech) | TMDB | ⚠️ | Still online, but the old `/embed/movie/{id}` path now 404s. It behaves like a watch page (`/watch/movie/{id}`), not a clean embed API anymore |
| **ScreenScape** | [screenscape.me](https://screenscape.me) | TMDB/IMDB | ⚠️ | Same story as CinemaOS — the embed routes are gone, `/watch/movie/{id}` and `/tv/{id}` still serve pages |
| **Rive (rivestream)** | [rivestream.app](https://www.rivestream.app) | TMDB | ⚠️ | Frontend is up but I couldn't find any public embed API path. Treat as a watch site only |

---

## Self-Hosted & Scraper APIs

Open source stuff you deploy yourself. You own the stack, you control the breakage.

| Project | GitHub | Stars | What it does |
|---------|--------|-------|--------------|
| **TMDB-Embed-API** | [Inside4ndroid/TMDB-Embed-API](https://github.com/Inside4ndroid/TMDB-Embed-API) | 130+ | Aggregates Showbox/FebBox, 4KHDHub, Videasy, Vidlink, NoTorrent and more into one API. Admin panel, TMDB key rotation, Docker image, HLS proxy. Actively maintained |
| **CinePro** | [cinepro-org/core](https://github.com/cinepro-org/core) | 145+ | Multi-site scraper, claims 50+ playable sources per title. Has its own docs at docs.cinepro.cc |
| **vidsrc.ts** | [cool-dev-guy/vidsrc.ts](https://github.com/cool-dev-guy/vidsrc.ts) | 110+ | TypeScript extractor for vidsrc.to/.me/.net/.in/.io. PoC, no longer updated but still a good reference |
| **vidsrc-api** | [cool-dev-guy/vidsrc-api](https://github.com/cool-dev-guy/vidsrc-api) | 95+ | Same author's earlier extractor-as-API. Deprecated in favor of vidsrc.ts |
| **vidsrc-to-resolver** | [Ciarands/vidsrc-to-resolver](https://github.com/Ciarands/vidsrc-to-resolver) | 65+ | CLI that pulls m3u8 playlists straight out of vidsrc.to |
| **MediaVanced** | [yogesh-hacker/MediaVanced](https://github.com/yogesh-hacker/MediaVanced) | 75+ | Parses media links from a bunch of streaming sites |
| **EncDecEndpoints** | [smy778/EncDecEndpoints](https://github.com/smy778/EncDecEndpoints) | 75+ | Encryption/decryption API toolkit — the layer under several embed sites (Videasy, Vidlink, LordFlix). Useful if you're digging into how they work |
| **Moviebox-API** | [walterwhite-69/Moviebox-API](https://github.com/walterwhite-69/Moviebox-API) | 45+ | FastAPI scraper for MovieBox.ph — metadata + direct MP4/HLS extraction with Cloudflare bypass. Recently active |
| **vidstream-api** | [WBRK-dev/vidstream-api](https://github.com/WBRK-dev/vidstream-api) | 30+ | FlixHQ scraper with a RabbitStream parser |
| **flixhq-core** | [shin202/flixhq-core](https://github.com/shin202/flixhq-core) | 30+ | FlixHQ data extraction library |
| **vidsrc-scraper** | [DivineChile/vidsrc-scraper](https://github.com/DivineChile/vidsrc-scraper) | 30+ | Node.js VidSrc scraper, domain-agnostic |
| **vidsrc-bypass** | [heyitswit/vidsrc-bypass](https://github.com/heyitswit/vidsrc-bypass) | 25+ | Bypass wrapper for embed.su / VidSrc / Vidlink |
| **2embed-api** | [parnexcodes/2embed-api](https://github.com/parnexcodes/2embed-api) | 25+ | Grabs HLS streams from 2Embed |
| **vidlink decryptor** | [walterwhite-69/Vidlink.pro-Decryptor](https://github.com/walterwhite-69/Vidlink.pro-Decryptor) | 10+ | Pure-Python port of Vidlink's WASM crypto (XSalsa20-Poly1305). No browser needed |
| **vidcore-hls-scraper-resolver** | [sharoon7171/vidcore-hls-scraper-resolver](https://github.com/sharoon7171/vidcore-hls-scraper-resolver) | new | Reverse-engineers VidCore's encrypted catalog, resolves TMDB ids to M3U8, includes an HLS proxy. Node/TS |

---

## Anime Streaming APIs

| Provider | URL / GitHub | Type | Status | Notes |
|----------|-------------|------|--------|-------|
| **AniKoto API** | [anikototvapi.vercel.app](https://anikototvapi.vercel.app/) | REST | ✅ | Vercel-hosted, no API key. Root `/api` returns the endpoint list |
| **AMVstrm** | [amvstrm/api](https://github.com/amvstrm/api) | REST | ⚠️ | Open source anime streaming provider API. The public api.amvstrm.ninja didn't resolve for me — self-host it |
| **MiruroAPI** | [Shineii86/MiruroAPI](https://github.com/Shineii86/MiruroAPI) | REST | ✅ | 46 endpoints, dozen+ providers, M3U8 output |
| **Shirayuki API** | [Anandadevnath/Shirayuki-Anime-API](https://github.com/Anandadevnath/Shirayuki-Anime-API) | REST | ✅ | Multi-provider scraper (MegaCloud, VidSrc). Actively pushed |
| **Anime Streaming (RapidAPI)** | [rapidapi.com](https://rapidapi.com/adarsh.chouhan11/api/anime-streaming) | REST | ✅ | 300 req/min free tier, HLS sources |
| **AniList GraphQL** | [docs.anilist.co](https://docs.anilist.co/) | GraphQL | ✅ | Best metadata source for anime. No streams |
| **Jikan** | [docs.api.jikan.moe](https://docs.api.jikan.moe/) | REST | ✅ | MyAnimeList wrapper, no key needed |
| **Kitsu** | [kitsu.docs.apiary.io](https://kitsu.docs.apiary.io/) | JSON:API | ✅ | Anime + manga, no key |

---

## Metadata APIs (Movie & TV Info)

For building the UI around the player — titles, ratings, posters, cast. No video in these.

| API | URL | Free Tier | Auth | Best For |
|-----|-----|-----------|------|----------|
| **TMDB** | [themoviedb.org](https://www.themoviedb.org) | Yes (attribution required) | API Key | Images, credits, trending, discovery. The ids everything else in this list is built on |
| **OMDb** | [omdbapi.com](http://www.omdbapi.com) | 1,000 req/day | API Key | Quick IMDb-style lookups |
| **TVmaze** | [tvmaze.com/api](https://www.tvmaze.com/api) | Yes | None | TV shows, episode data, schedules |
| **Trakt** | [trakt.docs.apiary.io](https://trakt.docs.apiary.io) | Yes | OAuth | Watch history, ratings, lists |
| **Simkl** | [simkl.docs.apiary.io](https://simkl.docs.apiary.io) | Yes | API Key | Movie, TV and anime tracking |
| **TasteDive** | [tastedive.com/read/api](https://tastedive.com/read/api) | Yes | API Key | Recommendations |
| **Cinemeta (Stremio)** | [v3-cinemeta.strem.io](https://v3-cinemeta.strem.io) | Yes | None | Catalogs + metadata as plain JSON, verified working. Great when you want TMDB-style data without a key |
| **Free-Movie-Series-DB-API** | [GitHub](https://github.com/TelegramPlayground/Free-Movie-Series-DB-API) | Yes | None | Unofficial movie/series search API, no keys at all |
| **IMDb (API.market)** | [api.market](https://api.market/store/sleeyax/imdb) | Free trial | API Key | Cleaner IMDb data than scraping |
| **MoviesDatabase** | [rapidapi.com](https://rapidapi.com) | Freemium | API Key | 9M+ titles, large cast index |

---

## Streaming Availability APIs

These answer "where can I watch this legally?" — Netflix/Prime/etc. links, not streams.

| API | URL | Free Tier | Notes |
|-----|-----|-----------|-------|
| **Watchmode** | [api.watchmode.com](https://api.watchmode.com) | Yes | Region filters, deep links |
| **TMDB Watch Providers** | [developer.themoviedb.org](https://developer.themoviedb.org) | Yes | JustWatch data baked into TMDB |
| **JustWatch** | [justwatch.com](https://www.justwatch.com) | Paid | The source behind most of this category |

---

## Subtitle APIs

| Provider | URL | Status | Notes |
|----------|-----|--------|-------|
| **Wyzie Subs** | [sub.wyzie.io](https://sub.wyzie.io) | ⚠️ | sub.wyzie.ru redirects here. Now needs a free API key (`&key=...`) — grab one at store.wyzie.io/redeem. Open source: [wyzie-subs](https://github.com/wyziedevs/wyzie-subs) |
| **Subdl** | [api.subdl.com](https://api.subdl.com) | ✅ | `GET /api/v1/subtitles` with `api_key` + `film_name`. Key is free with an account. Confirmed the endpoint responds |
| **OpenSubtitles** | [api.opensubtitles.com](https://opensubtitles.stoplight.io/docs/opensubtitles-api/) | ⚠️ | Official REST API now. Free tier exists but registration + API key required, and it's stricter than it used to be |

---

## Stremio Ecosystem

Not embed APIs exactly, but Stremio addons expose streams over plain HTTP, which makes them
usable from your own code too. Too big to ignore in 2026.

| Project | GitHub / URL | What it is |
|---------|--------------|------------|
| **AIOStreams** | [Viren070/AIOStreams](https://github.com/Viren070/AIOStreams) | Super-addon merging many addons + debrid/usenet into one endpoint. 2.5k stars |
| **stremio-addons-list** | [stremio-community/stremio-addons-list](https://github.com/stremio-community/stremio-addons-list) | Community-curated index of addons |
| **stremio-addon-sdk** | [Stremio/stremio-addon-sdk](https://github.com/Stremio/stremio-addon-sdk) | Official Node SDK for writing addons |
| **Cinemeta** | [v3-cinemeta.strem.io](https://v3-cinemeta.strem.io) | Catalog + metadata, verified live |

---

## Feature Comparison

### Embed APIs

| Provider | TMDB | IMDB | TV | Anime | Subtitles | HLS | Multi-Server | Key needed |
|----------|------|------|----|-------|-----------|-----|--------------|------------|
| VidSrc | ✅ | ✅ | ✅ | ❌ | ✅ (custom URL) | Partial | ❌ | No |
| 2Embed (.cc) | ✅ | ✅ | ✅ | ✅ | Partial | Partial | ❌ | No |
| SuperEmbed | ✅ | ✅ | ✅ | Partial | Partial | Partial | ✅ | No |
| vidlink.pro | ✅ | ❌ | ✅ | ❌ | ✅ | ✅ | ✅ | Yes (JSON API) |
| VidCore | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | No |
| vidfast | ✅ | ❌ | ✅ | ❌ | ✅ | ✅ | ✅ | No |
| EmbedMaster | ✅ | ✅ | ✅ | ❌ | ✅ | ✅ | ✅ | Yes |

### Metadata APIs

| Provider | Movies | TV | Images | Cast | Search | Discovery | Free |
|----------|--------|-----|--------|------|--------|-----------|------|
| TMDB | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Cinemeta | ✅ | ✅ | ✅ | Partial | ❌ | ✅ | ✅ |
| OMDb | ✅ | Partial | ✅ | Partial | ✅ | ❌ | ✅ |
| TVmaze | ❌ | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |
| Trakt | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ | ✅ |
| Simkl | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

---

## Quick Start Examples

### 2Embed (easiest entry point)

Movie:
```html
<iframe src="https://www.2embed.cc/embed/movie/tt23779058" allowfullscreen></iframe>
```

TV show (id/season/episode):
```html
<iframe src="https://www.2embed.cc/embed/tv/205715/1/1" allowfullscreen></iframe>
```

### VidSrc

Movie:
```html
<iframe src="https://vidsrc.to/embed/movie/927085" allowfullscreen></iframe>
```

TV show, specific episode:
```html
<iframe src="https://vidsrc.to/embed/tv/158876/1/5" allowfullscreen></iframe>
```

Burning in your own subtitles:
```
https://vidsrc.to/embed/movie/{id}?sub_file=https://example.com/subs.vtt&sub_label=English
```

### SuperEmbed

By IMDB id:
```html
<iframe src="https://multiembed.mov/?video_id=tt8385148" allowfullscreen></iframe>
```

By TMDB id:
```html
<iframe src="https://multiembed.mov/?video_id=522931&tmdb=1" allowfullscreen></iframe>
```

Note: `directstream.php` no longer exists on multiembed.mov — just use the base URL above.

### vidlink.pro

```html
<iframe src="https://vidlink.pro/movie/603" allowfullscreen></iframe>
```

TV:
```html
<iframe src="https://vidlink.pro/tv/1396/1/1" allowfullscreen></iframe>
```

### VidCore

```html
<iframe src="https://vidcore.org/embed/movie/603" width="100%" height="600" allowfullscreen></iframe>
```

TV:
```html
<iframe src="https://vidcore.org/embed/tv/1396/1/1" width="100%" height="600" allowfullscreen></iframe>
```

### vidfast

```html
<iframe src="https://vidfast.vc/movie/603" allowfullscreen></iframe>
```

### Wyzie subtitles (needs free key)

```js
const subs = await fetch(
  `https://sub.wyzie.io/search?id=${tmdbId}&language=en&key=${WYZIE_KEY}`
).then(r => r.json());
```

---

## Graveyard (checked and dead)

RIP. Verified broken as of August 2026. Kept here so you stop seeing them floating around
in older lists.

| What | What happened |
|------|---------------|
| vidsrc.xyz | DNS doesn't resolve anymore |
| vidsrc.cx | DNS doesn't resolve anymore |
| vidsrc.me original domain | Redirects to vidsrcme.ru |
| apiplayer.ru | "Website has been stopped" page |
| ezvidapi.com | Persistent 502 on Cloudflare |
| spencerdevs.xyz | 522, origin unreachable |
| vidbinge.to | 521, origin down (vidbinge.com survives) |
| 2embed.stream | Flaky 522s — 2embed.cc is the working one |
| multiembed.mov/directstream.php | 404, endpoint removed |
| vidcore.created.app | 404, old embed path retired — use vidcore.org |
| cinemaos.live `/embed/` routes | Replaced by `/watch/` pages |
| sub.wyzie.ru old keyless mode | Now requires a free API key |

---

## How I test this stuff

Because streaming APIs lie to you. A domain can return 200 and still be useless. So:

1. **DNS + TLS first.** If a domain doesn't even resolve, it's gone regardless of what
   some blog says.
2. **Hit real endpoints with real ids.** TMDB 603 (The Matrix) for movies, 1396
   (Breaking Bad) S01E01 for TV. An empty HTML shell or a 404 tells me more than a
   homepage ever will.
3. **Follow redirects.** Half of these services bounce you around (wfs.lol → embed.wfs.lol,
   multiembed.mov → streamingnow.mov). That's fine as long as the final stop has a player.
4. **Body check.** A 200 with a "domain for sale" page is a 404 in my book.
5. **GitHub repos** get checked for existence and last push date, not just stars.

Statuses can still flip overnight — these providers move domains constantly. If something
here broke, open an issue.

---

## Related lists

| Project | Description |
|---------|-------------|
| [best-vidsrc-alternative](https://github.com/samratt5/best-vidsrc-alternative) | VidSrc alternative comparison (leans promotional for VidCore, take with salt) |
| [stremio-addons-list](https://github.com/stremio-community/stremio-addons-list) | Index of Stremio addons |
| [awesome-stremio](https://github.com/doingodswork/awesome-stremio) | Curated Stremio tools list |

---

## Contributing

Found something that works and isn't here? PR or issue, please. When you do:

- Provider name and the exact URL format you tested
- TMDB/IMDB — which ids does it take?
- Whether you verified an actual embed loads, not just the homepage
- API key requirements, if any

Stuff that's just a homepage with no working endpoints won't make it in.

---

## License

Provided as-is for educational use. Be decent, build responsibly, respect copyright.
