# dotfiles
Notes for new desktop installation

# System
Packages nice to have:

    pacman -Sy gnome-tweaks emacs-nativecomp yay

## Terminal
Use *Kitty* for now with *Fira Code* font:

    pacman -Sy kitty ttf-fira-code

Kitty config changes:

    enable_audio_bell      no
    font_family            Fira Code
    font_features          FiraCode-Regular ss05
    font_size              15.0
    tab_bar_edge           top
    tab_bar_style          powerline
    wayland_titlebar_color system

Install kitty theme:

    kitty +kitten themes
    
*Doom One Light* looks ok
### Fish
Switch to vim mode:

    fish_vi_key_bindings

Add accept suggestions to fish config *.config/fish/config.fish*

    bind -M insert \cf accept-autosuggestion

## Gnome

(on Xorg) X11 gestures now working at arch, enable it
    
    yay -Sy touche touchegg gnome-shell-extension-x11gestures 
    # systemctl enable --now touchegg

## Firefox
Enable smooth scrolling

    cat /etc/profile.d/firefox.sh
    #hack to make smooth scrolling
    export MOZ_USE_XINPUT2=1
    export MOZ_ENABLE_WAYLAND=1

Slow down scroll, change:

**about:config** **mousewheel.default.delta_multiplier_y** to **20**
