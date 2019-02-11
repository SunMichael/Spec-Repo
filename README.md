# Spec-Repo
# 创建自己的pod库
### 主要注意事项：

1.必须添加LISENCE    

2.在根目录下创建podspec文件    
  pod spec create NAME
  
  注意文件中 s.source_files 绝对路径  以及 s.frameworks 等的编写不能错     
  
3.验证    
  pod lib lint --verbose    

4.创建tag  
  git tag -m "message" "0.0.1"    
  git push --tags    
  
  会提示输入对面git平台账号密码    

5.添加repo，会将remote的项目clone 到本地cocoapods目录中     
  pod repo add Spec-Repo https://github.com/SunMichael/Spec-Repo.git    

6.上传podspec到 Spec-Repo仓库下    
  pod repo push Spec-Repo Spec-Repo.podspec    
  
7.上传podspec到cocoapods官方     
如果没有注册过账号，需要使用邮箱注册     
  pod trunk register bigsun1992@sina.cn    

验证通过后就可以上传了    
  pod trunk push Spec-Repo.podspec    

  
