# Social Pixel Lab Website

Static website for Beth Tellman / Social Pixel Lab. The site is a simple HTML/CSS/JS bundle (Spatial theme by TEMPLATED) with pages such as `index.html`, `people.html`, `publications.html`, etc., plus shared assets under `assets/` and images under `images/`.

## How it works
- Hosted as a user GitHub Pages site (`Beth-Tellman.github.io`), so the contents of the default branch are served directly—no build step needed.
- Update the live site by committing and pushing changes to the repository. GitHub Pages will publish from the root of the branch automatically.
- To preview locally, from the repo root run `python3 -m http.server 8000` and open `http://localhost:8000` in a browser.

## Editing the People page
- The People page is the static file `people.html`. Each person is defined inside a `div` with class `feature` within the `feature-grid`.
- To edit an existing entry, update the name, role, and paragraph text inside that block. Keep links and line breaks as needed.
- To add someone new, copy an existing `div class="feature">…</div>` block, paste it where you want them to appear, and adjust the content.
- Photos live in `images/`. Add a new photo there (use a reasonable size), set the `img src` to that filename, and update the `alt` text.
- After edits, refresh your browser if previewing locally; commit and push to publish via GitHub Pages.


1. **Clone or open the repo**

   ```bash
   git clone https://github.com/Beth-Tellman/Beth-Tellman.github.io.git
   cd Beth-Tellman.github.io
   ```

2. **Drop a square headshot in `/images/`**
   *File name:* `lastname_firstname.jpg`
   *Size:* ≈ 400–600 px square (the page rounds it into a circle).

3. **Edit `people.html`**
 
   `### Current lab members at ...`
   copy any existing `<div class="feature"> … </div>` block and paste it just below the last UW-Madison entry.
   Replace the highlighted bits:

   ```html
   <div class="feature">
     <div class="image rounded">
       <!-- ① image file -->
       <img src="images/bryant_firstname.jpg" alt="FIRST LAST" />
     </div>

     <div class="content">
       <header>
         <!-- ② name -->
         <h4>FIRST LAST</h4>
         <!-- ③ role -->
         <p>Postdoctoral Researcher</p>
       </header>

       <!-- ④ short bio (2-4 sentences) -->
       <p>…</p>

       <!-- ⑤ links (optional) -->
       <p>
         Email: you@wisc.edu<br>
         <a href="https://scholar.google.com/…">Google Scholar</a><br>
         <a href="https://github.com/…">GitHub</a>
       </p>
     </div>
   </div>
   ```

4. **Test Locally**

    run `python -m http.server 8000` in the repo root, then open http://localhost:8000/people.html in any browser.

4. **Commit & push**

   ```bash
   git add images/bryant_firstname.jpg people.html
   git commit -m "Add FIRST LAST to UW-Madison lab members"
   git push
   ```

5. **Verify**
   Wait \~1 min, then browse `https://beth-tellman.github.io/people.html` and check that

   * the photo is round,
   * the bio uses normal sentence case (not all-caps),
   * the card appears in the correct block.