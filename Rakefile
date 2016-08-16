require 'rake'
require 'fog/aws'

desc 'Preview the site with Jekyll'
task :preview do
    sh "jekyll serve --watch --drafts --baseurl '' --config _config.yml,_config-dev.yml"
end

desc 'Search site and print specific deprecation warnings'
task :check do
    sh "jekyll doctor"
end

desc 'Upload to S3'
task :upload do
  Fog.credentials_path = "../.fog"
  Dir.chdir("_site") do
    assets = FileList['*','**/*'].inject({}) do |hsh, path|
      if File.directory? path
        hsh.update("#{path}/" => :directory)
      else
        hsh.update(path => OpenSSL::Digest::MD5.hexdigest(File.read(path)))
      end
    end
    raise '_site is empty: aborting' if assets.size <= 1

    fog = Fog::Storage.new(provider: 'AWS', region: 'ap-southeast-2')
    bucket = fog.directories.get('www.arcwhite.org')

    assets.each do |file, etag|
      case etag
      when :directory
        puts "Directory #{file}"
        bucket.files.create(key: file, public: true)
      when (bucket.files.get(file)&.etag)
        puts "Skipping #{file} (identical)"
      else
        puts "Uploading #{file}"
        bucket.files.create(key: file, public: true, body: File.open(file))
      end
    end

    # bucket.files.each do |object|
    #   unless assets.key? object.key
    #     puts "Removing #{object.key} (no longer exists)"
    #     object.destroy
    #   end
    # end
  end
end
