# Jetpush
Jetpush is a Continues Deployment tool for iOS distribution with automatic signing.  
Also Jetpush can create GitHub and GitLab CI configuration.

<img src="https://github.com/mohamadrezakoohkan/Jetpush/blob/master/jetpush.gif">

## How it works
Jetpush using xcodebuild commandline tool to `archive` and `export` project to an IPA file. 
Jetpush export configurations reads from known `ExportOptions.plist`, At last it commit and push result to git with message of IPA information.


