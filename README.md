# AWS Console – Classic Dark

A theme for the AWS Management Console.
It brings back the look of the **classic AWS dark mode**:

- Dark navy blue background
- Cool grey text
- **AWS orange** highlights (main button, active tab, checkboxes...)

It is built on top of the theme
[aws-console-ui-theme-ayu-dark](https://github.com/igreg/aws-console-ui-theme-ayu-dark)
by Gregory Becker (MIT licence). That theme finds the colour tokens of the console.
This project only changes the colours.

## What you need

- Firefox or Chrome with the **Stylus** extension.
- The AWS console in dark mode: **Settings → Visual mode → Dark**.

## How to install

1. Install the **Stylus** extension in your browser.
2. Open this link:
   https://raw.githubusercontent.com/pdelaroche/aws-console-classic-dark/main/aws-classic-dark.user.css
3. Stylus opens an install page. Click **Install style**.
4. Open the AWS console and reload the page (Cmd+Shift+R or Ctrl+Shift+R).

That's all. Stylus checks this link for new versions.

**Tip:** in the Stylus options, keep **"Apply to iframes"** on.
Many AWS services show their page inside an iframe.

## How to change the colours

All the colours are in one block called **PALETTE**.

**Option A – in the browser (easy)**

1. Open Stylus → **Manage** → **AWS Console - Classic Dark** → **Edit**.
2. The PALETTE block is at the top. Change the colours you want.
3. Click **Save** and reload AWS.

Note: if you edit the style in Stylus, an update can replace your changes.
Turn off updates for this style if you want to keep them.

**Option B – in the project (for developers)**

1. Edit `palette.css`.
2. Run `python3 build.py`.
3. The script makes a new `aws-classic-dark.user.css`.

| Variable | What it colours |
|---|---|
| `--tpl-bg` | Main background and top bar |
| `--tpl-panel` | Cards, panels and code blocks |
| `--tpl-surface`, `--tpl-surface-2` | Menus and dropdowns |
| `--tpl-hover` | Background when the mouse is over an item |
| `--tpl-border-*` | Borders and lines |
| `--tpl-text-*` | Text, from dark to light |
| `--tpl-heading` | Titles |
| `--tpl-accent` | Highlights: main button, active tab, checkboxes... |
| `--tpl-accent-hover` / `--tpl-accent-active` | Highlight on mouse over / on click |
| `--tpl-nav-title` | Titles in the side menu |

The light versions of the highlight colour are made automatically.

## Change the colours with AI

1. Open `prompt-ai.md`.
2. Write the style you want, for example "dark green, like a terminal".
3. Paste the prompt and your PALETTE block into any AI chat.
4. Replace your PALETTE block with the new one.

## Project files

| File | What it is |
|---|---|
| `aws-classic-dark.user.css` | The theme. This is the file you install. |
| `palette.css` | The colours |
| `build.py` | Makes the theme from the base theme and the palette |
| `base/` | The original Ayu Dark theme and its licence |
| `prompt-ai.md` | A prompt to make new colours with AI |

## Problems and fixes

| Problem | Possible cause | Fix |
|---|---|---|
| Nothing changes | Browser cache | Reload with Cmd+Shift+R |
| No change at all | The console is in light mode | Settings → Visual mode → Dark |
| One AWS service is still grey | AWS changed its internal tokens | Get the new base theme, put it in `base/`, run `python3 build.py` |
| A service page is not themed | "Apply to iframes" is off | Turn it on in the Stylus options |

## How to remove it

Stylus → **Manage** → untick the style, or delete it.

## Credits

- Base theme: Gregory Becker, MIT licence (see `base/LICENSE`).
- Classic Dark colours: based on the classic Cloudscape dark palette (approximate values).
- Unofficial project. It is not connected to Amazon Web Services.
