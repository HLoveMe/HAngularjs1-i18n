# HAngularjs1-i18n

 
 *  设置语言文件路径
     LanguageConfig.configLanguagePath("./js/a.json")
 
 *  切换语言  默认为"zh-cn"
     LanguageConfig.setLanguage("en-us")
 
 *  通知:
     "language.switchFinish"  完成
     "language.switchFail"    失败
 
 *  标签
 
   ```
     <div class='test' i18n="name"  >zz</div>  使用 'name' 作为key  获取对应值改变 zz
     <a class="button" i18n         >city</a>     使用  'city' 作为key
   ```
 *  历史记录
     在改变语言后 会使用  localStorage.setItem("language",lan); 记录当前语言
     在下次使用 会使用该记录为启动语言
 
 *  错误说明
     在切换语言失败后 自动回滚到之前的语言
 
     说明 i18n 所在标签 智能选择标签
    ```
    <div i18n="name" class='test' >zz</div>
     ====>   <div ng-transclude="" i18n="name" class="test">name</div>
 
     <p i18n="name" class='tpest' >zz</p>
     ====>   <p ng-transclude="" i18n="name" class="test">name</p>
    ```

