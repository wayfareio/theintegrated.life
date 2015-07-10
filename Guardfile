guard :copy, from: '_assets/images',
             to: 'assets/images',
             mkpath: true,
             delete: true,
             run_at_start: true do
  watch(%r{^_assets/images/.+$})
end

guard :sass, output: 'assets/stylesheets',
             style: :compressed,
             all_on_start: true do
  watch(%r{^_assets/stylesheets/public.scss})
  watch(%r{^_assets/stylesheets/sticky-footer.scss})
  watch(%r{^_assets/stylesheets/sticky-footer-ie.scss})
  watch(%r{^_assets/stylesheets/home.scss})
end

guard :uglify, input: "_assets/javascripts/public.js",
               output: "assets/javascripts/public.js",
               run_at_start: true do
  callback(:start_begin) { FileUtils.mkdir_p("assets/javascripts") }
end
