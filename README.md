# Station Reach

How well does a station connect? Pick a home station and see where its trains go, how often, and every journey
across a day to and from a place you care about.

Live at https://commute.tobermory.io

- **Direct services**: a map of every station reached without changing (line thickness is how many trains run each
  stretch), departures per hour, and a table of destinations with frequency and fastest time.
- **Getting to…**: every journey to a destination (a station, street or place) and back, on a day timeline, with
  journeys a day, frequency, fastest and typical time, first and last train, and the longest daytime gap. Hover a
  journey for its legs, operators and connections.
- **Journey settings**: modes of transport, walking speed and a minimum time to change (default 5 minutes, National
  Rail's standard; the router's own station minimum is about 2 minutes everywhere).

Scheduled timetables and routing come from [Transitous](https://transitous.org) (MOTIS, built on operators'
published data), so engineering works and strikes may not show. The map uses OpenStreetMap tiles. There is no
backend and no API key: it is one static page.

## Run locally

```
npm start
```

Then open http://localhost:4400.

## Deploy

```
npm run deploy
```

Deploys `public/` as a Cloudflare Worker with static assets, on the custom domain `commute.tobermory.io`.

## Licence and data

The code is MIT licensed (see `LICENSE`). Timetable data and routing come from Transitous, whose
[usage policy](https://transitous.org/api/) asks for open-source, non-commercial, light use; the page credits its
[data sources](https://transitous.org/sources/) and gives a contact address. Map tiles follow the
[OpenStreetMap tile usage policy](https://operations.osmfoundation.org/policies/tiles/).
