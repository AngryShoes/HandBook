# 创建自定义Nuget包

- 创建类库
  
  填写必要的程序集信息 AssemblyInfo.cs

- 使用Nuget.exe
  
  - 下载[Nuget.exe](https://www.nuget.org/downloads)  
  - NuGet会根据项目Guid和版本号对类库进行管理,将nuget.exe与.csproj工程文件放至同一目录。按Shift键右键选择“在此处打开命令窗口”
  - 输入命令
  
    ```shell
    .\nuget.exe spec
    ```

    ![generate spec](https://github.com/AngryShoes/HandBook/blob/master/Git/images/generateNugetSpec.png)
    nuspec文件是一个XML配置文件，带$号表示对应信息会从程序集读取。
  
    ```shell
    .\nuget.exe pack JRWatermarkTextWriter.csproj
    ```

    ![pack](https://github.com/AngryShoes/HandBook/blob/master/Git/images/pack.png)
    开始执行打包。如果出现错误或警告，根据提示修改AssemblyInfo.cs或.nuspec文件，保存后重新编译项目，再次执行打包命令。

    打包成功后会在项目根目录输出.nupkg文件

- 上传至NuGet官方服务器
  - 申请NuGet账号并创建ApiKey
  - 创建完成之后 上传服务器输入命令
  
    ```shell
    nuget push XXXX.nupkg MyApiKey -Source https://www.nuget.org/packages
    ```

    ![push](https://github.com/AngryShoes/HandBook/blob/master/Git/images/push.png)

    这里可以看到红色的提示意味着sepc文件里的licenseUrl和IconUrl没有填写
    BTW,licenseUrl微软认为过时了，需要在spec定义license标签，如果是常见的MIT，APache等license直接在标签写入即可，如果是自定义license可以创建txt文件引入。可以参考微软推荐的[标准](https://docs.microsoft.com/en-us/nuget/reference/nuspec#licenseurl)
  
  - 同样也可以通过Nuget官网上传
    ![upload](https://github.com/AngryShoes/HandBook/blob/master/Git/images/upload.png)

上传成功之后需要几分钟时间审核，审核通过会收到邮件提示。
