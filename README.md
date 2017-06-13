# The Minilogue Sound Librarian Librarian

The Minilogue Sound Librarian Librarian (`miniloguesll`) is a simple script that prepares sound packs (a.k.a. preset files, a.k.a. `.mnlgpreset` files) from Minilogue patch files and bundles of patch files. For some strange reason this feature was left out of KORG's [Minilogue Sound Librarian](http://www.korg.com/uk/products/synthesizers/minilogue/librarian_contents.php) making it cumbersome to manage collections of Minilogue patches.

## Installation

You will need Ruby (which is already available if you use MacOS) and the `rubyzip` gem:

```
$ gem install rubyzip
```

## Usage

To prepare a new sound pack, use the name of your new sound pack as the first argument. This is the label that will show up in the sound pack manager in the Minilogue Sound Librarian, and it will also be used as the name of the sound pack file (with the extension `.mnlgpreset` appended). Then add as many sound packs, patch libraries or individual patches as you like to add to the sound pack:

```
$ miniloguesll "My Patch Collection" strings.mnlglib saw1.mnlgprog
```

As an added bonus (?), `miniloguesll` will ignore repeated patches (only the first copy will be added to the pack), all factory patches, as well as those from the two current official sound packs. If you download patch collections from the internet (e.g. from the [Facebook Minilogue patch sharing group](https://www.facebook.com/groups/1140022976008269/)), these will probably contain some of the factory patches too --- in particular the init patch. Filtering these out means that `miniloguesll` can build sound packs that complement the official ones without any overlap.
