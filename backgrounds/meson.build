dataconf = configuration_data()
dataconf.set('BACKGROUNDDIR', backgrounddir)
dataconf.set('datadir', datadir)

backgrounds = [
  'bloom-d.jxl',
  'bloom-l.jxl',
  'line-d.jxl',
  'line-l.jxl',
  'ocean-d.jxl',
  'ocean-l.jxl',
  'pride-d.jxl',
  'pride-l.jxl',
  'steep-d.jxl',
  'steep-l.jxl',
  'sky-d.jxl',
  'sky-l.jxl',
  'wheel-d.jxl',
  'wheel-l.jxl',
  'world-d.jxl',
  'world-l.jxl'
]

install_data(backgrounds, install_dir: backgrounddir)

foreach metadata : [
  'bloom.xml',
  'line.xml',
  'ocean.xml',
  'pride.xml',
  'steep.xml',
  'sky.xml',
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
