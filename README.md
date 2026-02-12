# Snake (C# WebAssembly)

A browser-based Snake game implemented with **Blazor WebAssembly** so the game logic runs in C# and compiles to WebAssembly.

## Features

- 20x20 board rendered in the browser.
- Snake movement using arrow keys or WASD.
- Food spawning and score tracking.
- Speed increases every 4 food items.
- Game-over detection for wall and self collisions.
- Restart with the `R` key.

## Requirements

- .NET SDK 8.0+ (only needed if running locally)
- Chrome (or any modern browser with WebAssembly support)

## Run in browser **without installing anything locally**

### Option 1: GitHub Pages (recommended)

This repository includes a workflow at `.github/workflows/deploy-pages.yml` that builds and deploys automatically.

1. Push this repo to GitHub.
2. In GitHub, open **Settings → Pages** and set **Source** to **GitHub Actions**.
3. Push to the `main` branch (or run the workflow manually from **Actions**).
4. Open the site URL:
   - `https://<your-username>.github.io/<repo-name>/`

After that, anyone can open the game directly in Chrome with no local setup.

### Option 2: GitHub Codespaces (also no local install)

1. Open the repo on GitHub.
2. Click **Code → Codespaces → Create codespace on main**.
3. In the terminal inside Codespaces run:
   ```bash
   dotnet restore
   dotnet run
   ```
4. When prompted, open the forwarded port in browser.

## Run locally

```bash
dotnet restore
dotnet run
```

When the app starts, open the local URL shown in the console.

## Controls

- `↑` / `W`: Up
- `↓` / `S`: Down
- `←` / `A`: Left
- `→` / `D`: Right
- `R`: Restart game

## Project structure

- `Snake.Wasm.csproj` — Blazor WebAssembly project file.
- `Pages/Index.razor` — Snake game UI and gameplay logic.
- `Program.cs` / `App.razor` — app bootstrapping and routing.
- `wwwroot/index.html` — browser host page.
- `.github/workflows/deploy-pages.yml` — CI/CD workflow to publish to GitHub Pages.
