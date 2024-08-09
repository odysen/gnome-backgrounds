dataconf = configuration_data()
dataconf.set('BACKGROUNDDIR', backgrounddir)
dataconf.set('datadir', datadir)

backgrounds = [
  'bloom-d.svg',
  'bloom-l.svg',
  'line-d.svg',
  'line-l.svg',
  'ocean-d.svg',
  'ocean-l.svg',
  'pride-d.svg',
  'pride-l.svg',
  'steep-d.svg',
  'steep-l.svg',
  'wheel-d.svg',
  'wheel-l.svg',
  'world-d.svg',
  'world-l.svg'
]

install_data(backgrounds, install_dir: backgrounddir)

foreach metadata : [
  'bloom.xml',
  'line.xml',
  'ocean.xml',
  'pride.xml',
  'steep.xml',
  'wheel.xml',
  'world.xml']
  configure_file(
    input: metadata + '.in',
    output: metadata,
    configuration: dataconf,
    install: true,
    install_dir: metadatadir
  )
endforeach
