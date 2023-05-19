# About this repo

A GTK theme from Graphite  
https://github.com/vinceliuice/Graphite-gtk-theme  

Personalize for C31\

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

## 2. Outline or box-shadow (Gnome Terminal)

- search * Window Decorations
- active: #14b8a6
- inactive: #0a665b
- target: #E0E0E0

## 3. Misc

- titlebutton.close
- toolbar
- titlebar
- \* window decoration
- .context-menu
- \* Lists
- \* Popovers
- window.csd -> (vscode, chromium)

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