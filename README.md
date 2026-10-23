# Zenty Place

Zenty Place is a mobile-friendly collaborative pixel canvas on a world map.

## Live backend setup (required once)

The frontend is configured for the Supabase project currently connected to this repository. To activate shared pixels and accounts:

1. Open the Supabase project dashboard.
2. Go to **SQL Editor** → **New query**.
3. Open [supabase/schema.sql](./supabase/schema.sql), copy the entire file, paste it into SQL Editor, and press **Run**.
4. In Supabase **Authentication → Providers → Email**, keep Email enabled. For quick testing you may disable email confirmations; for a public site, keep confirmation enabled and configure the email provider.
5. In **Authentication → URL Configuration**, set the Site URL to `https://zenty1907.github.io/zenty-games-2/` and add that URL to Redirect URLs.
6. Wait for GitHub Pages to deploy the latest commit, then open the site and create an account.

The frontend uses only the Supabase publishable key. No secret/service-role key is included in the website. Pixel placement is performed through the `place_pixel` database function, which enforces a 30-second cooldown server-side. Shared pixels are broadcast through Supabase Realtime.

## Features

- OpenStreetMap world map with pan/zoom and location search
- 16-color palette
- Email/password sign-up and sign-in
- Shared persistent pixel canvas across visitors
- Realtime pixel updates
- Server-validated 30-second pixel cooldown
- Responsive mobile and desktop layout

## Current limitations

- Team creation/joining and the leaderboard UI are still local prototype features and are **not yet shared across accounts**.
- The current database uses a 0.001-degree coordinate grid; pixels may look slightly different by latitude.
- This project has not been verified end-to-end against the newly created Supabase instance until the SQL above is run and a test account successfully places a pixel.
- Map tiles and geocoding are provided by OpenStreetMap services and are subject to their usage policies.

## Deployment

GitHub Pages: https://zenty1907.github.io/zenty-games-2/

## Credits

Map data © OpenStreetMap contributors: https://www.openstreetmap.org/copyright

This is an independent project and is not affiliated with Wplace or Reddit.
