# mdbook-machlit

The core documentation theme for Machlit; used with the [mdbook](https://github.com/rust-lang/mdBook) markdown-based documenting tool.

## Installation

1. Create a new mdBook project with the `--theme` flag:

```bash
mdbook init --theme
```

2. Navigate to the directory and in the **theme/** folder, delete everything except **index.hbs**.

3. Clone this repository:

```bash
git clone https://github.com/machlit/mdbook-machlit.git
```

4. Copy the CSS files from `src/` from the cloned repo and paste it into the `theme/` folder.

5. In your **book.toml** file, add the following line under the `[output.html]` section:

```toml
[output.html]
default-theme = "machlight"
preferred-dark-theme = "machlit"
additional_css = ["./theme/machlit.css", "./theme/machlight.css"]
```

6. Edit the **index.hbs** file and modify the theme navigation menu's contents:

```diff
- <li role="none"><button role="menuitem" class="theme" id="light">Light</button></li>
- <li role="none"><button role="menuitem" class="theme" id="rust">Rust</button></li>
- <li role="none"><button role="menuitem" class="theme" id="coal">Coal</button></li>
- <li role="none"><button role="menuitem" class="theme" id="navy">Navy</button></li>
- <li role="none"><button role="menuitem" class="theme" id="ayu">Ayu</button></li>
+ <li role="none"><button role="menuitem" class="theme" id="machlit">machlit</button></li>
+ <li role="none"><button role="menuitem" class="theme" id="machlight">machlight</button></li>
```

7. Run `mdbook serve` to preview your book locally.

8. Enjoy!

## License

This project is licensed under the [MIT](LICENSE) license.
