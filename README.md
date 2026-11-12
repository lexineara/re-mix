[README.md](https://github.com/user-attachments/files/34730727/README.md)
# Re:mix

Re:mix is a buildless static site. Serve the project root over HTTPS for a real Spotify connection.

1. Enable the email-and-password provider in Supabase. Add the live `login.html` URL to the project's allowed auth redirect URLs. Configure the site's URL and confirmation email settings in Supabase.
2. In the Spotify developer dashboard, register the exact HTTPS `index.html` URL as a redirect URI and add the approved testers to the Development Mode app.
3. Fill in `config.js` with the Supabase project URL and publishable key, Spotify client ID, exact Spotify redirect URI, and HTTPS live site URL. These identifiers are public. Keep service-role keys and Spotify client secrets out of the repository.
4. Import the GitHub repository into Vercel. Use the project root with no build command or framework preset. Set the four `og:image` tags to the absolute HTTPS URL for `share.png` so link previews can fetch it.

Start at `login.html`. With an approved tester, check sign-up and login, connect Spotify on Home, export the liked songs list, and save a private playlist. If adding tracks fails after playlist creation, use **Retry save to Spotify** in the same tab.

- [Supabase Auth redirect URLs](https://supabase.com/docs/guides/auth/redirect-urls)
- [Spotify Development Mode guide](https://developer.spotify.com/documentation/web-api/tutorials/february-2026-migration-guide)
- [Spotify PKCE authorization](https://developer.spotify.com/documentation/web-api/tutorials/code-pkce-flow)
