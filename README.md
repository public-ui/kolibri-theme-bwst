# Public UI - BWSt-Theme

This is the `BWSt` theme for the [Public UI web component library](https://public-ui.github.io). You can customize this theme by using `css variables` or by creating a new theme.

## Integration in React

```tsx
import { register } from '@public-ui/components';
import { defineCustomElements } from '@public-ui/components/dist/loader';
import { BWSt } from '@public-ui/theme-bstw';

register(BWSt, defineCustomElements).then(() => {
	ReactDOM.createRoot(document.getElementById('root')!).render(
		<React.StrictMode>
			<App />
		</React.StrictMode>,
	);
});
```

## Windows hints

- Clone the repo: `git clone https://github.com/public-ui/kolibri-theme-bwst.git`
- Use the `Git Bash`
- Install PNPM in Version 9: `npm i -g pnpm^9`
- Node-Version: `node -v` -> Output: `v20.12.2`
- PNPM-Version: `pnpm -v` -> Output: `9.0.6`
- Repo irectory: `pnpm i`

```bash
Packages: +1305
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Progress: resolved 1305, reused 1304, downloaded 1, added 1305, done
node_modules/.pnpm/chromedriver@124.0.1/node_modules/chromedriver: Running install script, done in 3.2s

devDependencies:
+ @public-ui/components 2.1.1
+ @public-ui/visual-tests 2.1.1
+ @rollup/plugin-commonjs 25.0.8
+ @rollup/plugin-node-resolve 15.2.3
+ @rollup/plugin-typescript 11.1.6
+ @types/node 20.12.8
+ @typescript-eslint/eslint-plugin 7.11.0
+ @typescript-eslint/parser 7.11.0
+ eslint 8.57.0
+ nodemon 3.1.2
+ npm-check-updates 16.14.20
+ postcss 8.4.38
+ prettier 3.2.5
+ rollup 4.18.0
+ rollup-plugin-postcss 4.0.2
+ sass 1.77.3
+ typescript 5.4.5
```

- Start dev: `npm start`
- Edit files

## Full documentation

👉 [https://public-ui.github.io](https://public-ui.github.io)

## Usage (DE)

Das Default-Theme ist ein _Token-Based_ Theme, das mit minimalen Anpassungen sofort verwendet werden kann. Es bringt bereits alle notwendigen Stylings mit und kann
über Design Tokens, in Form von _CSS Custom Properties_ an das eigene Design angepasst werden.

### Variablen

| Variable                          | Standard-Wert                                    | Bedeutung                                          |
| --------------------------------- | ------------------------------------------------ | -------------------------------------------------- |
| `--kolibri-border-radius`         | `5px`                                            | Border-Radius für abgerundete Elemente             |
| `--kolibri-font-family`           | `Calibri, Verdana, Arial, Helvetica, sans-serif` | Allgemeine Schriftart                              |
| `--kolibri-font-size`             | `16px`                                           | Allgemeine Schriftgröße                            |
| `--kolibri-spacing`               | `0.25rem`                                        | Allgemeiner Abstand zwischen Elementen             |
| `--kolibri-border-width`          | `1px`                                            | Allgemeine Rahmen-Breite                           |
| `--kolibri-color-primary`         | `#004b76`                                        | Primärfarbe                                        |
| `--kolibri-color-primary-variant` | `#0077b6`                                        | Alternative Variante der Primärfarbe               |
| `--kolibri-color-danger`          | `#c0003c`                                        | Farbe für Fehlermeldungen und gefährliche Aktionen |
| `--kolibri-color-warning`         | `#c44931`                                        | Farbe für Warnungen                                |
| `--kolibri-color-success`         | `#005c45`                                        | Farbe für Erfolgsmeldungen                         |
| `--kolibri-color-subtle`          | `#576164`                                        | Farbe für feine Akzente wie z.B. Rahmen            |
| `--kolibri-color-light`           | `#ffffff`                                        | Helle Farbe für z.B. Hintergründe                  |
| `--kolibri-color-text`            | `#202020`                                        | Textfarbe                                          |
| `--kolibri-color-mute`            | `#f2f3f4`                                        | Farbe für deaktivierte Elemente                    |
| `--kolibri-color-mute-variant`    | `#bec5c9`                                        | Alternative Farbe für deaktivierte Elemente        |

### Verwendung

Theme importieren und registrieren:

```js
import { register } from '@public-ui/components';
import { defineCustomElements } from '@public-ui/components/dist/loader';
import { BWSt } from '@public-ui/theme-bstw';

register(BWSt, defineCustomElements);
```

Für mehr Details und weitere Optionen siehe [Erste Schritte](https://public-ui.github.io/docs/get-started/first-steps#einbinden-in-ein-bestehendes-projekt).

Um die _Design Tokens_ anzupassen, reicht ein einfaches Stylesheet, das die gewünschten Custom Properties überschreibt. Es ist dabei nicht notwendig, alle Properties zu setzen, sondern nur solche, die auch überschrieben werden sollen. Beispiel:

```css
:root {
	--kolibri-border-radius: 3px;
	--kolibri-font-size: 18px;
	--kolibri-spacing: 0.3rem;
	--kolibri-color-primary: #cc006e;
	--kolibri-color-primary-variant: #ff64b9;
}
```

```html

<!doctype html>
<html lang="de" dir="ltr">
	<head>
		<title>Code-Samples | KoliBri – Public UI</title>
		<meta charset="UTF-8" />
		<meta name="description" content="Webanwendung mit der KoliBri-Komponentenbibliothek." />
		<meta name="viewport" content="width=device-width, initial-scale=1" />
		<link rel="shortcut icon" type="image/x-icon" href="assets/kolibri.ico" />

		<link rel="stylesheet" href="assets/codicons/codicon.css" />
	<!---	<link rel="stylesheet" href="assets/fontawesome-free/css/all.min.css" />-->
		<link rel="stylesheet" href="assets/noto-sans/noto-sans.css" />
		<link rel="stylesheet" href="main.css" />
		<meta name="robots" content="noindex" />
		<meta name="kolibri" content="dev-mode=false;experimental-mode=true;" />
	</head>
	<body>
		<div id="app"></div>
		<script async src="main.js"></script>
		<noscript>Diese Webseite erfordert, dass Sie JavaScript aktivieren.</noscript>
	</body>
</html>

```
