```
           .WWWW.
          WWWW""'
        .WWWW O O
     .WWWW"WW.'-.
    WWWWWWWWWWWWW.
   WWWWWWWWWWWWWWW
   "WWWWWWWWWW"'\___
    /  /__ __/\___( \
   (____( \X( mrf /||\
      / /||\ \
      \______/
       \ | \ |
        )|  \|
       (_|  /|
       |X| (X|
       |X| |X'._
      (__| (____)
```

# igor

A tool for connecting to lab servers and performing basic tasks like power
cycling them.

## Configuration

System specifications need to be added in `~/.config/igor/systems.toml`. An
example for a system called `foo` is shown below.

```
[foo]

[foo.host]
addr = "foo-host.com"   # mandatory
user = "amd"                # mandatory
pass = "amd123"             # mandatory
port = 22                   # optional, defaults to 22

[foo.bmc]
addr = "foo-bmc.com"    # mandatory
user = "root"               # optional, defaults to "root"
pass = "0penBmc"            # optional, defaults to "0penBmc"
port = 2200                 # optional, defaults to 2200

[foo.pdu]
addr = "lab-pdu.com"    # mandatory
user = "admin"              # optional, defaults to "admin"
pass = "raritan"            # optional, defaults to "raritan"
port = 33      # mandatory
```

## Usage

Once a system is defined, it can be accessed using its name and used with
various options as shown below.

```
igor --connect foo
igor --console foo
igor --cycle-power foo
igor --cycle-inlet foo
```

## Disclaimer

This tool is provided without any guarantees of correctness and maintenance.

## Attributions

Artwork sourced from <https://ascii.co.uk/art/igor>
