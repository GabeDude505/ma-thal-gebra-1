ARCADE SITE  -  upload this whole folder to the root of your launcher repo

  index.svg, index.html, gams.json     the launcher (open index.svg)
  modern/                              Modern Client (Eaglercraft 1.12.2, JS) split into small files
  tuff/                                Tuff Client (Eaglercraft 1.12, WASM-GC) split into small files

The 843 other games are NOT in this folder. They load from your fork:
  REMOTE_BASE in index.svg / index.html = https://cdn.jsdelivr.net/gh/GabeDude505/ma-thal-gebra@main/

No games/ folder is needed any more.

FILE SIZES (every file is under jsDelivr's 20 MB limit and GitHub's 25 MB browser-upload limit)
  modern/classes.js          15.3 MB
  modern/assets.part1.bin    13.8 MB   (the 27.6 MB asset pack, cut in two; the page joins them)
  modern/assets.part2.bin    13.8 MB
  tuff/assets.part1.bin      11.6 MB   (the 23.1 MB asset pack, cut in two)
  tuff/assets.part2.bin      11.6 MB

URL after upload (jsDelivr):
  https://cdn.jsdelivr.net/gh/GabeDude505/ma-thal-gebra-1@main/index.svg

NOTES
- Keep the .bin files in the same folder as their index.html; they are downloaded and joined on load.
- gams.json entries 1000 (Modern) and 1001 (Tuff) use "dir": "modern/" / "tuff/".
- jsDelivr caches @main; after uploading changes, use a commit hash in the URL or wait for the cache.
- Worlds are saved in the browser under the address you open the site from.
