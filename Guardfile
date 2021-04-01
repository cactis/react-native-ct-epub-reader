excludeString =  "#{ENV['excludeString']},example/android/build"
p excludeString
`mkdir ~/ramdisk/ct-epub-reader`
apps_sync = "rsync -avzhPR --delete . --exclude={#{excludeString}} ~/ramdisk/ct-epub-reader/"
p apps_sync
`#{apps_sync}`

p Time.now

guard :shell do
  watch(/(.*).*/) {|m|
    p apps_sync
    p Time.now
    `#{apps_sync}`  
  }
end
