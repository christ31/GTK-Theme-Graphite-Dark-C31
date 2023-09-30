# About this repo

A GTK theme from Graphite  
https://github.com/vinceliuice/Graphite-gtk-theme  

Personalize for C31

![Screenshot from 2023-05-20 02-29-54](https://github.com/christ31/GTK-Theme-Graphite-Dark-C31/assets/37174502/ddf14c5d-95f2-4477-ba68-fb33ee302fa9)

# Editing your own Gnome Theme

1. Go to ./themes
2. go to GTK3 folder, and edit gtk.css
3. Find `headerbar {` and set `min-height` to 24 px

# Granite Themes Stuff

## 1. Apps specific 

> Currently active > dark theme

### GTK3

- Gnome Tweak apps using gtk-dark.css
- Gedit using gtk.css
- Chrome and Chromium using gtk.css

### GTK4

- VScode using gtk-dark.css on csd
- button.minimize
- button.close

## 2. Outline or box-shadow (Gnome Terminal)

- search * Window Decorations
- active: #14b8a6
- inactive: #0a665b
- target: #E0E0E0
- BG: #23252E

## 3. Misc (GTK 3)

- titlebutton.close
- titlebutton.minimize
- toolbar
- titlebar
- \* window decoration
- .context-menu
- \* Lists
- \* Popovers
- window.csd -> (vscode, chromium)
- button

## 4. Gnome Shell
- .panel-button: #0a665b => Tombol yang ada di panel seperti clock, date, dan tombol menu system
- .popup-menu .popup-menu-item 
- .popup-menu .popup-menu-content => Klik kanan shell

## LibreOffice Active Cell Border Color
- gtk-dark.css
- Line 55


## Chromium and VSC
GTK3 (gtk.css)
- window.background.chromium menu

Chromium has limited css
Only background, foreground, and border color can be set

https://chromium.googlesource.com/chromium/src/+/acc4214c4dece4e70fb53355d557bd45f35965d6/docs/linux_gtk_theme_integration.md

## General Name
- .csd.popup decoration => Buat popup yang ada di menuList, sama klik kanan terminal
- .context-menu menuitem => Buat item list yang ada di klik kanan terminal
- window.background.chromium menu => Klik kanan di Chromium
- headerbar button => Buat pengaturan size pada header
- button.image-button => Buat pengaturan size button pada header

# Shortcut to activate GTK+ Inspector

>  CTRL + Shift + D

https://wiki.gnome.org/Projects/GTK/Inspector

GtkInspector is the built-in interactive debugging support in GTK+. It was added in GTK+ 3.14, based on a copy of the well-established gtkparasite.

The debugger is disabled by default. To enable it, make sure you have the libgtk-3-dev(debian-naming) or gtk3-devel(fedora-naming) package installed and run in a terminal:

gsettings set org.gtk.Settings.Debug enable-inspector-keybinding true
If the application you are using happens to be a Flatpak it will likely have a separate GSettings storage than your host system, you will need to modify that environment separately like the following.


flatpak run --command='sh' org.gnome.Polari
gsettings set org.gtk.Settings.Debug enable-inspector-keybinding true
If you are developing the application via Gnome Builder, open the "Runtime terminal" from the "Open Menu", and run the same gsetting command.


gsettings set org.gtk.Settings.Debug enable-inspector-keybinding true
To launch the GTK Inspector, focus your GTK application and press Control-Shift-D. Alternatively, move your mouse cursor to your desired widget and press Control-Shift-I to specifically inspect the widget under the mouse cursor.

If you don't want to use the shortcuts, you can also open the Inspector directly when running your app with:

GTK_DEBUG=interactive your-app
