# Uncomment the next line to define a global platform for your project
platform :ios, '13.0'

target 'Example' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  pod 'Texture', '~> 3.0'
  pod 'RxSwift', '~> 6.0'
  pod 'RxCocoa', '~> 6.0'
  pod 'Differentiator', '~> 5.0'

end

post_install do |pod_installer|
  pod_installer.pods_project.targets.each do |t|
    if t.respond_to?(:product_type) and t.product_type == "com.apple.product-type.bundle"
      t.build_configurations.each do |config|
          config.build_settings['CODE_SIGNING_ALLOWED'] = 'NO'
      end
    end
    t.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '13.0'
    end
  end
end
