# The Functional Playroom: website

A simple website with five pages, made only from plain HTML and CSS files, so it can be hosted for free.

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | **Home** page |
| `services.html` | **Services** page (four services and common questions) |
| `about.html` | **About** page |
| `contact.html` | **Contact** page with the consultation request form |
| `privacy.html` | **Privacy Policy** (a template to fill in) |
| `css/styles.css` | The "look" of the site: colours, fonts, spacing, phone layout |
| `images/` | A folder for your photos |
| `images/brand/` | Your logo files (`logo-mark.svg` is the sharp version used on the site) |

An `.html` file holds the words on a page. The `.css` file controls how every page looks.

---

## 1. Preview the site on your computer

You don't need to install anything.

1. Download this folder to your computer. On GitHub: green **Code** button → **Download ZIP**, then unzip it.
2. Open the folder and **double-click `index.html`**. It opens in your web browser.
3. Click around with the menu at the top. Every page and link works on your computer.

**To see the phone version:** make the browser window very narrow. Or, in Chrome, right-click the page → **Inspect** → click the small phone/tablet icon at the top left of the panel that opens.

> The contact form only sends messages once you've connected it to Formspree (step 3) **and** the site is online (step 4).

## 2. Fill in your details

Open each `.html` file in a plain text editor. On a Mac, [VS Code](https://code.visualstudio.com/) (free) works well; on Windows, Notepad also works. Look for text in **[square brackets]** and replace it, including the brackets:

- `[Your Name]` and your story on the About page
- `[Your City]` (on most pages, at the bottom)
- `[Add your price]` on the Services page
- `[2 business days]` on the Contact page
- Everything in brackets on the Privacy Policy page

Also replace `hello@example.com` with your real email address. It appears at the bottom of every page and on the Contact and Privacy pages.

**Tip:** Most editors have "Find in all files" (in VS Code: Ctrl+Shift+F, or Cmd+Shift+F on a Mac). Use it to search for `[` or `example.com` to find every placeholder.

After saving, refresh the browser to see your change.

> The menu and footer are copied into each page. If you change them, change them in all five files.

## 3. Add your photos

Every pink striped box that says "Your photo here" is a placeholder.

1. Put your photo in the `images` folder. Use simple file names with no spaces, such as `playroom-after.jpg`.
2. In the `.html` file, find the matching box. It looks like this, with a note above it:

   ```html
   <!-- PHOTO: replace this box with your best "after" playroom photo -->
   <div class="photo-placeholder tall" role="img" aria-label="Photo coming soon">
     Your photo here:<br>a calm, organized playroom
   </div>
   ```

3. Replace the whole `<div ...> ... </div>` part (keep the note if you like) with:

   ```html
   <img src="images/playroom-after.jpg" alt="A bright playroom with low shelves and labelled baskets">
   ```

   The `alt` text describes the photo for people who use screen readers and for Google.

**Photo tips:** Landscape photos work best. Resize them to about 1600 pixels wide before adding them so the site loads quickly. [Squoosh.app](https://squoosh.app) is a free tool for this. Only use photos of clients' homes with their permission.

## 4. Connect the contact form (Formspree, free)

The form uses **[Formspree](https://formspree.io)**. Its free plan forwards up to 50 messages a month to your email, with no coding.

1. Sign up at formspree.io and click **+ New Form**. Name it "Consultation requests" and choose which email should receive messages.
2. Formspree shows you a form address like `https://formspree.io/f/abcdwxyz`. The last part (`abcdwxyz`) is your form ID.
3. In `contact.html`, find this line:

   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

   Replace `YOUR_FORM_ID` with your ID and save.
4. Once the site is online, send yourself a test message. Formspree asks you to confirm your email the first time.

After someone submits the form, Formspree shows them a short "Thanks" page. A hidden spam trap is already built into the form.

**Alternative:** If you host with Netlify (see below), you can use **Netlify Forms** (free, 100 messages a month) instead. Ask for help switching if you'd prefer that.

## 5. Put the site online for free

**Option A: GitHub Pages** (this folder is already on GitHub)
1. On the GitHub page for this project, go to **Settings → Pages**.
2. Under "Branch", choose your main branch and the `/ (root)` folder, then click **Save**.
3. After a minute or two, GitHub shows your web address, something like `https://yourname.github.io/functional-playroom/`.

**Option B: Netlify Drop** (easiest if you don't want to use GitHub)
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop) and create a free account.
2. Drag the whole website folder onto the page. It's live within seconds.
3. To update the site later, drag the folder in again.

Both options let you connect your own domain name (like `thefunctionalplayroom.com`) later, which you'd buy separately for about $15–20 a year.

## 6. Changing colours or fonts

Open `css/styles.css`. The colours are listed at the top with notes such as `/* main accent (buttons, links) */`. Change a colour code (for example `#8fa98b`) and every page updates.

## A note on the Privacy Policy

`privacy.html` is a plain-language starting template, not legal advice. Fill in the bracketed parts and check that it meets the privacy rules where you work before you publish.
