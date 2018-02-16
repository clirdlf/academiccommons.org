require 'fileutils'
require 'jekyll-import'

desc 'Clean _posts directory'
task :clean do
  FileUtils.rm_f Dir.glob('_posts/*')

  FileUtils.rm_rf Dir.glob('_drafts')
  FileUtils.rm_rf Dir.glob('_custom_csss')
  FileUtils.rm_rf Dir.glob('_nav_menu_items')
  FileUtils.rm_rf Dir.glob('_pages/')
  FileUtils.rm_rf Dir.glob('assets/images')
end

#  TODO: make this smarter to get the latest dump
desc 'Import WordPress dump'
task :import do
  JekyllImport::Importers::WordpressDotCom.run(
    {
      "source" => "assets/wordpress/theacademiccommons.wordpress.2018-02-15.xml",
      "no_fetch_images" => false,
      "assets_folder" => "assets/images"
    }
  )
end

desc 'Fix category bug'
task :fix_colons do
  `find ./_posts -type f -exec sed -i '' -e 's/'Games in Education:/'Games in Education-/g' {} \;`
  # grep -rl "Games in Education:" _posts | xargs sed -i 's/Games in Education:/Games in Education/g'
end
