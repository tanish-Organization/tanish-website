TROVÉ MEDIA — Website source code
==================================

FILES
- index.html     The profile page (posts, services, clients, stories, post pop-ups).
- contact.html   The Message page (chat that sends enquiries to WhatsApp / email / Instagram).
- logo-nav.png   Small logo (header, avatars). Transparent background.
- logo-word.png  Large logo (first post). Transparent background.
- fonts/         Newsreader + Geist (free Google Fonts, OFL licence).

No build step. It is plain HTML, CSS and JavaScript. Open index.html in a browser to see it.

1) CHANGE THE LOGO
Replace logo-nav.png and logo-word.png with your new TROVÉ MEDIA logo.
Keep the same file names. Use PNGs with a transparent background.

2) SET YOUR WHATSAPP, EMAIL AND INSTAGRAM
Open contact.html in any text editor (Notepad works). Near the top of the script, change:
    var WHATSAPP='917045944509';        -> (already set) your number with country code, no + or spaces (e.g. 919876543210)
    var EMAIL='hello@yourdomain.com';   -> your email
    var IG='trovemedia.official';       -> your Instagram username
The Instagram username also appears in index.html (search "trovemedia.official") and in contact.html.

3) EDIT TEXT
All post text, captions and stories are in index.html, inside the <script> at the bottom:
    POSTS   = the 9 posts in the grid
    REELS   = the Services tab
    TAGGED  = the Clients tab
    S       = the stories (highlights)
Edit the words between the quotes. If a sentence contains an apostrophe ('), write it as \'

4) PUT IT LIVE ON VERCEL (free)
- Go to vercel.com and log in.
- Add New -> Project -> drag and drop this whole folder (or upload it through GitHub).
- No settings needed (Framework: Other). Click Deploy.
- You get a link like trove-media.vercel.app. You can connect your own domain later in Settings -> Domains.
To update: upload the folder again (or push to GitHub if you connected it).

5) LIKES & COMMENTS
Visitors can like posts (heart button or double-tap) and comment (typed or quick emojis).
Right now these are saved only on the visitor's own phone/browser (localStorage), so other people
don't see them. To make comments public for everyone, connect a free database (e.g. Firebase or
Supabase) in the "likes & comments" part of the script in index.html, and add a way to delete bad comments.

6) GOOGLE SEARCH (hidden for now)
index.html and contact.html have this line near the top:
    <meta name="robots" content="noindex, nofollow">
It tells Google NOT to show the site in search while you test. Anyone with the link can still open it.
When the site is final, delete that line in both files and upload again. Then add the site to
Google Search Console (search.google.com/search-console) so it shows up faster.
