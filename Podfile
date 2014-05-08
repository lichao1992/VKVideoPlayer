platform :ios, '5.0'
pod 'DTCoreText', '1.6.10'
pod 'AFNetworking', '1.3.3'
pod 'SBJson', '3.1'
pod 'BlocksKit', '~> 1.8.3'
pod 'CocoaLumberjack', '~> 1.7.0'
pod 'VKFoundation', :git => "https://github.com/viki-org/VKFoundation.git"
#pod 'VKFoundation', :podspec => "~/Develop/viki/libs/VKFoundation/VKFoundation.podspec"
pod 'CocoaHTTPServer'

target 'VKVideoPlayerTests' do
  pod 'Specta',      '~> 0.2.1'
  pod 'Expecta',     '~> 0.3.0'
  pod 'OCMock',      '~> 2.2.1'
  pod 'CocoaHTTPServer'
end

# Remove 64-bit build architecture from Pods targets
post_install do |installer|
  installer.project.targets.each do |target|
    target.build_configurations.each do |configuration|
      target.build_settings(configuration.name)['ARCHS'] = '$(ARCHS_STANDARD_32_BIT)'
    end
  end
end
