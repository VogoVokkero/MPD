
libasound_dep = dependency('alsa', version: '>= 0.9.0', required: get_option('alsa'))

conf.set('ENABLE_ALSA', true)

alsa = static_library(
  'alsa',
  'Version.cxx',
  'AllowedFormat.cxx',
  'HwSetup.cxx',
  'NonBlock.cxx',
  include_directories: inc,
  dependencies: [
    libasound_dep,
  ],
)

alsa_dep = declare_dependency(
  link_with: alsa,
  dependencies: [
    event_dep,
  ],
)
