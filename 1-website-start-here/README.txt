ATHARVA BOKADE PORTFOLIO
========================

WHAT'S IN THIS FOLDER
  index.html   the website
  previews/    short silent clips that play when someone hovers a film
  posters/     still images shown on each film before it plays
  media/       web-quality versions of each film (under 15MB each)

Upload the whole folder, keeping these four together, to any web host
(Netlify, Vercel, Hostinger, cPanel, GitHub Pages and so on) and point
atharvaa.online at it. Nothing needs installing or building.


SHOWING YOUR FULL-QUALITY (1080p / 4K) FILMS
--------------------------------------------
Out of the box, clicking a film plays the web-quality file from media/.
To play your full-quality master instead:

1. Upload the original film to Vimeo, YouTube, Cloudflare Stream or
   Bunny Stream.
2. Copy its link.
3. Open index.html in any text editor and search for the film's id
   (list below). Each film starts like this:

     { id:"puppy", ...M("puppy"), title:"Puppy & Crab", ...

   Add  full:"YOUR LINK"  right after ...M("puppy"), like this:

     { id:"puppy", ...M("puppy"), full:"https://vimeo.com/123456789", title:"Puppy & Crab", ...

4. Save and upload index.html again.

Links that work in full:
  Vimeo            https://vimeo.com/123456789
                   (unlisted links like https://vimeo.com/123456789/abcdef12 work too)
  YouTube          https://www.youtube.com/watch?v=XXXXXXXXXXX  or  https://youtu.be/XXXXXXXXXXX
  Cloudflare       https://customer-xxxx.cloudflarestream.com/VIDEO_ID/iframe
  Bunny Stream     https://iframe.mediadelivery.net/embed/LIBRARY_ID/VIDEO_ID
  Direct file      https://your-storage.com/film.mp4

With a streaming link, the film plays in that service's player, which
picks the best quality for each viewer's connection, up to 4K, and
supports full screen. Hover previews keep playing from previews/.


FILM IDS
--------
  puppy        Puppy & Crab
  vcj          VCJ Vishal Chain
  aakash       Aakash
  cadbury      Cadbury Celebrations
  drools       Drools
  frooti       Frooti
  superyou     SuperYou
  hairserum    Hair Serum UGC
  amaltas      Amaltas Greens
  microdrama   Micro-Drama
  hybrid       2D x Live Action
  desert       Rajput Raider
  lastzone     Last Zone
  spiti        Spiti


CATEGORIES
----------
The "All films" page groups films by category. To change which films
are in a category, search index.html for  const CATS  and edit the
film ids in each  films:[...]  list. A film can be in more than one.


CHANGING TEXT
-------------
Each film's title, client, summary, brief and "how I made it" text are
in the same entry in index.html. Edit the words between the quotes.
