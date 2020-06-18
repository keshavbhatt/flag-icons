## About :

Repository contains flags of different countries which are named in [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)  format.
So you can use them in your project easily if your backend output name of countries using the standard.

## Content :

    .
    ├── svgs <directory contaning flags in SVG format>
    ├── pngs <directory contaning flags in PNG format with size 512x512 pixels>
    ├── README.md
    └── LICENSE


## Resize icons for your own project :

**Convert to PNG of size `<width>`** using [bash scripting](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29):

Use SVG icons to resize flags for your own project, on `bash shell` the following script when executed in svgs directory will output the desired sized icons of flags for you. For this to work you should have [Inkscape](https://en.wikipedia.org/wiki/Inkscape) installed on your system.
Don't forget to change `<width>` variable in the following command:


    for file in *.svg; do inkscape -z -f "${file}" -w <width> -e "${file%svg}png"; done

**What does the command do ?** 

The above bash script loops through all the svg files in the base directory (current working directory of shell prompt), and for each file opens inkscape program with `-z (without-gui)` , `-f (filename)` , `-w, (export-width in pixels)` & `-e, (export-png filename)` arguments.

## Contribution :
Feel free to add other methods to resize or convert icons to different formats in pull request.
