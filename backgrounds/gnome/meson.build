backgrounddir = join_paths(datadir, 'backgrounds', 'gnome')
metadatadir = join_paths(datadir, 'gnome-background-properties')

conf = configuration_data()
conf.set('BACKGROUNDDIR', backgrounddir)
conf.set('datadir', datadir)

backgrounds = [
  'alt-regular-gnome-d.png',
  'alt-regular-gnome-l.png',
]

metadatas = [
  'alt-regular-gnome.xml',
]

install_data(backgrounds, install_dir: backgrounddir)

foreach metadata : metadatas
  configure_file(
    input: metadata + '.in',
    output: metadata,
    configuration: conf,
    install: true,
    install_dir: metadatadir
  )
endforeach
