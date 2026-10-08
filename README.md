# Personal site

Plain HTML, CSS and JavaScript. No build step and no dependencies, so you can open `index.html` in a browser to preview it.

## Files

- `index.html`: the whole site (styles, content and script).
- `assets/`: screenshots and photos.
- `play/nebula-web.html`: the original single-file web edition of Nebula Requiem, copied from its repository. The "play in browser" button on its card opens this page.

## Edit

- **Projects:** change the `PROJECTS` list at the top of the `<script>` in `index.html`. The cards, the filter counts, the timeline and the numbers in the hero are all built from it. Set `visibility: "private"` to show a lock and no link. When you add or remove a project, also check the tools list (`STACK`), the three cards in the About section (`like_games`, `like_web`, `like_hw`) and the project counts written in the HTML and in `EL.lead` and `EL.v_code`. The counts are replaced by the real numbers when the page loads, but the written ones are what a visitor without JavaScript sees.
- **Dates:** each project has `started` and `updated` ("YYYY-MM"). They come from each repository's first and latest commit on GitHub, so correct them if a project was really started earlier.
- **Greek:** texts that exist in both languages are written `L("English", "Ελληνικά")`. The Greek for the fixed parts of the page is in the `EL` object, and the English for those parts is in the HTML itself. The site opens in English, remembers the choice from the EN/ΕΛ button, and `…/#el` or `…/#en` opens a specific language. The Greek is written without masculine or feminine forms ("σπουδάζω", "διδάσκω"), so it works for any reader.
- **Headline words:** the words the "I build…" headline types are in `HEADLINE`, one list per language. Keep each word under 18 characters so the line never wraps. Visitors who prefer reduced motion see a plain sentence instead.
- **Email:** `CONTACT_EMAILS` lists the addresses shown in the Contact section (up to two), each with a copy button. A plain address on a public page can be picked up by spam bots.
- **Tools list:** edit `STACK` in the same script.
- **Images:** `assets/`. The Nebula Requiem screenshots come from that repository's `docs/media`.
- **Colors and fonts:** the tokens at the top of the `<style>` block. The page follows the visitor's light or dark setting, and the button in the header overrides it.

## Publish on GitHub Pages

1. Create a public repository named `aloualou56.github.io`.
2. Push these files to its `main` branch.
3. In the repository, open Settings, then Pages, and choose "Deploy from a branch" with `main` and `/ (root)`.
4. The site appears at https://aloualou56.github.io within a minute or two.

Then add that address to the Website field on your GitHub profile and link it from your profile README.
