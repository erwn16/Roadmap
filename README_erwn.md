Trello Boards
=============

Linux Mint 20.1 https://trello.com/b/xAg5vHlI/linux-mint-201

Maintenance
===========

    update mirrors
    update translations for installation guide
    advertise community website in get involved page
    add sum to download page directly

Linux Mint 20
=============

    mintupdate: remove blacklist sync button (confusing). When blacklist changes or is different, alert user with infobar, does he want to sync?

    selection:
        open-vm-tools?
        libinput-gestures?

    mintupdate:
        remove linux-kernel-generic meta? (or shall we do it in ubiquity?)

    meta:
        make it easier to install other DE?

    artwork:
        theme LO
        remove all sound, power, network icons in mint-y-icons/panel/ (needs patches in Xfce and MATE to stop using fullcolor in panel (for MATE power manager) and notifications)
        mint-y-icons: improve computer icon

    mate:
        Ctrl+alt+backspace support

    cinnamon:
        cs_info: Show a distro logo
        remove send-by-email nemo action

    mate:
        theme settings
            folder icons too big
            mint-x background too dark
        hidpi
            titlebar buttons are blurry

    system:
        add CLI support for foreign packages list/removal/downgrade

    artwork:
        new website theme
        use dark-variants for dark apps (xplayer..etc) in Mint-Y (needs fixes in mint-themes and marco: https://github.com/mate-desktop/marco/pull/530)
        icons
            grey-on-grey icons (many in cinnamon-settings)
        update MATE metathemes
        consider manjaro mouse cursor?

    mintupdate:
        safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).

    mintlocale:
        remove language packs and packages when a language is removed

    software:
        Replace Hexchat
        Replace Qt5Settings? (not hidpi compatible)

    drawing:
        implement zoom
        simplify rotation, flip..

    timeshift:
        show a tray when a save is ongoing
        let user cancel save

    A system configuration tool? (to configure systemd and all? The shutdown timeout typically should be configurable in a UI now that we override it)

LMDE 5
======

    live-installer:
        Let user select/deselect swap
        Let user see/edit partition labels
        Let user disable badblock for LUKS


Ideas - Todos
==============

    https/apt:
        add https support for packages.linuxmint.com
        switch to https by default?
        add feature in mintsources to list https mirrors only?

    favorite/starred documents (nemo, xapps)

    fingerprint reader -> slick-greeter support
    https://askubuntu.com/questions/46501/why-can-other-users-see-the-files-in-my-home-folder

    artwork:
        revamp sound theme?
        cinnamon
            text-size to be configurable in panel zones?
            cinnamon/gtk mint-y: tooltips don't match theme

    help
        rtd security guide

    mate:
        fix terminal apps not running (gnome-terminal --> mate-terminal)

    mintupdate:
        remember sorting of updates

    port mintstick to python3

    artwork
        add dark variant support to Mint-Y (needs fixes in Caja/marco)
        cursor theme?
        sound theme?
        bump resolution of branded backgrounds

    slick
        would be nice to show release number

    xapps/cinnamon/nemo:
        don't ship icons with generic names in /usr/share/hicolor. All icons should be prefixed (cs-, xapp-, nemo-..etc..) so they don't conflict with other packages
        cinnamon-settings should use gsettingswidgets from xapp and retire its own

    cinnamon
        - spices: Add a button to install a manually downloaded spice
        gtk windows
        - When in tablet mode (that is, the screen is rotated and covering the keyboard) the RotateWindows key doesn't work anymore... It just does nothing...
        - menu-editor: picking a pixmap in /usr/share/pixmaps for a category results in no icon being shown in the menu.
        - Unable to unlock the screensaver via LDAP with libpam-ldap and nscd packages installed pointing to an openldap server.
        - csd power: https://github.com/GNOME/gnome-settings-daemon/commit/82af1816f32a26f28027ea7ce8edc79cd833bc76
        - in HiDPI, keyboard applet, the flags is not the proper size. Hovering it fixes it.
        - mounted volume applet: no notification when unmounting (as opposed to when it's done in nemo).
        - gwl: Enable "application name" label. Open FF, open at least two browser tabs. Close FF. The label slides over the icon and doesn't disappear: https://kepkuldes.com/image/UoNHl

    nemo
        better navbar
        consider sping loaded folders https://www.youtube.com/watch?v=gdUPrMjlLy8

    xed:
        option to remember past opened-documents

Roadmap
=======

    remove-apps
        prevent removal of sensitive packets (for instance, removing GOA removes cinnamon)

    main ideas
        mintsystem apt downgrade

    desktop-search:
        local files
        web engines
        recent
        apps
        dictionary
        translations

    mate:
        switch mozo for menulibre

    mintreport:
        dmesg errors
        foreign packages if pinned by mint
        wrong lsb info..etc.
        slow boot sequence
        slow shutdown sequence
        systray support

    mintupgrade
        list/address foreign packages post-upgrade

    implement an alarm clock

    cinnamon:
        cinnamon slow to start after boot --> delay execution of appsys/docinfo until the DE is loaded
        CSD: support mouse wheel speed? Evdev scrolling distance?
        preferences > keyboard > custom shortcuts. Used with a Spanish keyboard layout. Recorded: crtl+number and ctrl+Shift+number (e.g. ctrl+1 and ctrl+shift+1 = ctrl+!) they are recorded correctly. When using the shortcut the command defined in the shift combination is triggered with just ctrl+number (i.e. ctrl+1). The complete combination triggers nothing (i.e. ctrl+shift+1 does nothing) and the comand defined in ctrl+number can never be used. This worked in 17.3.
        track/troubleshoot shutdown sequence (user should know what is happening when shutdown isn't immediate)
        track/troubleshoot vsync, compositing, unredirected windows and policy
        todo list applet/desklet
        calendar events applet/desklet
        multiple clocks https://github.com/simonwiles/cinnamon_applets
        network applet: airplane mode (quick way to rfkill all)
        nemo: retire computer:/// place (which is completely useless) or revamp it into something better
        alt-tab and panel use icon provided by appsys, ignoring icon set by the application itself (example: a python window using widow.set_icon_name())
        actions in panel launchers aren't translated if not present in .desktop file
        When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
        Is there any reason why there are two names for the same item, eg. "Trash" and "Rubbish Bin"? Would it be better to standardise on only one name?
        add gnome-screenshot to panel, right-click and select "Take screenshot of a selected area". This runs gnome-screenshot -a.. it should work but it doesn't. Is it because of the panel launcher capturing the click event or something?

    xapps
        implement an app-sharing protocol to quickly move a document from one app to another

        gestures support:
            pinch:
                zoom document in pix
                zoom view in nemo

            swipe:
                previous/next document in pix

            scroll:
                sound-volume/seek in xplayer

            click:
                pause/resume in xplayer

            double-click:
                full-screen in xplayer
                full-screen in xviewer

        pix
            doesn't rotate videos when playing them
            vignettes should look better, and the same in all themes
            support prefer-dark-themes
            treeview in sidebar shows unecessary "(empty)" when dirs have no subdirs

    artwork:
        Tray icons are black with mint-y themes.
        mint-x-icons: network status icons have a dark background in panel 33px and bigger (sound icon looks wrong in 41px and bigger).
        mint-y The maximize/restore window control button doesn’t change visually between in maximized and restored state (default theme and Mint-Y-Dark)

    system:
        compiler optimization: consider optimizing compiled binaries for Cinnamon/Xapps

    HiDPI support:
        upstream apps using GTK2: Gimp, Hexchat, Tomboy.

R&D
===

    system
        consider enabling recommends

    network discovery:
        easy out-of-the-box interactions (messaging/presence/file-sharing) over the LAN
        
        


==========================================================================================================================================================        
PROPOSALS of a longitudinal Linux Mint user

For Login, Screensaver, Update manager etc.: A unique functionality of showing the password to be able to correct a mistype. This is nowadays a standard in many apps.

Recommendations with regard to start coding activities: Which projects are suitable for beginners like me? I didn't find recommendations.
Where is "St", the shell toolkit, documented in Github? This is not documented. 

Where can I submit proposals? I didn't find information about that. I guess that this way is not the correct channel.


