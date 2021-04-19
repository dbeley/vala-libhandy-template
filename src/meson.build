vala_libhandy_template_sources = [
  'main.vala',
  'window.vala',
]

vala_libhandy_template_deps = [
  dependency('gio-2.0', version: '>= 2.50'),
  dependency('gtk+-3.0', version: '>= 3.22'),
  dependency('libhandy-1', version: '>= 1.0.0'),
]

gnome = import('gnome')

vala_libhandy_template_sources += gnome.compile_resources('vala_libhandy_template-resources',
  'vala_libhandy_template.gresource.xml',
  c_name: 'vala_libhandy_template'
)

executable('vala-libhandy-template', vala_libhandy_template_sources,
  vala_args: '--target-glib=2.50',  dependencies: vala_libhandy_template_deps,
  install: true,
)
