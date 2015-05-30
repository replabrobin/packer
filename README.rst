

::

    
    
    SYNOPSIS
           pacman <operation> [options] [packages]
    
    DESCRIPTION
           Packer is a bash wrapper for pacman and the AUR. It was designed to be
           a simple and very fast replacement for the basic functionality of
           yaourt. It allows you to install, update, search, and show information
           for any package in the main repositories and in the AUR.
    
    OPERATIONS
           -R* | -D* | -U* | -Sc*
               Run pacman as root with given arguments.
    
           -S
               Install a package.
    
           -Sd[d]
               Install a package without dependency version checks.
    
           -Syu | -Su
               Sync with repositories.
    
           -Ss | -Ssq
               Search for a package.
    
           -Si
               Show information for a package.
    
           -G
               Download and extract AUR package tarballs, but don’t install
               anything.
    
           -h | --help
               Show packer usage.
    
    OPTIONS
           --force
               Bypass file conflict checks.
    
           --ignore <'package'>
               Ignore packages. Separate package names with a comma.
    
           --noconfirm
               Perform commands without confirmation from the user.
    
           --noedit
               Perform commands without asking if the user wants to edit any
               installation files.
    
           --quickcheck
               Check for updates and exit.
    
    
           --makepkg-log logfilepath.
               path to makepkg logfile.
    
           --assume-installed pkg=version
               assume pkg version is installed.
    
           --nodeps
               don't check dependencies.
    
           --preview
               Always offer to edit the pkgbuild before sourcing it.  To always
               force preview, 'alias packer="packer --preview"'
    
           --build-only
               Only build aur packages; useful to just create the binary package.
    
           --install-only
               Install an aur package already built with --build-only.
    
           --aurpkg pkg
               Only install this particular aur package. Can be used with glob
               patterns.
    
    INTERACTIVE MODE
           Use packer without any operations or options to use the interactive
           mode. Packer will show a numbered list of search results. To install a
           package, enter the corresponding number.
    
    EXAMPLE USAGE
           ·   Sync and update all packages: packer -Syu
    
           ·   Update only AUR packages: packer -Syu --auronly
    
           ·   Update, and reinstall packages that were installed from a revision
               control source: packer -Syu --devel
    
           For a package called name:
    
           ·   Search: packer -Ss name
    
           ·   Install: packer -S name
    
           ·   Install without confirmations: packer -S --noconfirm name
    
           ·   Get information about a package: packer -Si name
    
           ·   Search and install in interactive mode: packer name
    
    CONFIGURATION
           Packer uses these settings in /etc/pacman.conf:
    
    AUTHORS
           Matthew Bruenig <matthewbruenig@gmail.com>
           Kyle Keen https://github.com/keenerd/packer
           Gavin Hungry https://github.com/gavinhungry/packer
           Robin Becker
    
    Packer                             May 2015                           **PACKER(8)**
