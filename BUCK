xcode_developer_dir = read_config('apple', 'xcode_developer_dir', '/Applications/Xcode.app/Contents/Developer')

genrule(
  name = 'io-kit-framework', 
  out = 'IOKit.framework', 
  cmd = 'cp -r ' + xcode_developer_dir + '/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/System/Library/Frameworks/IOKit.framework $OUT', 
)

prebuilt_apple_framework(
  name = 'io-kit', 
  framework = ':io-kit-framework', 
  preferred_linkage = 'static', 
  visibility = [
    'PUBLIC', 
  ], 
)
