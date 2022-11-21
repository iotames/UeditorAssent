
## UEditor for yiiframework------Yii2.0下的百度编辑器小插件


## 使用方法：



1. yii Advanced 高级版。

覆盖到 frontend 目录下面，直接使用。

使用方法：

`widget('Classname',[]);`

例：

```
<?= $form->field($model, 'comment')->widget('frontend\assets\UeditorWidget',[

/*serverparam为后端PHP配置项，如myuploadpath设置图片上传路径*/
    'serverparam'=>[
        'myuploadpath'=> Yii::getAlias('@web/Uploads/').$model['id'],
    ],

/*options为前端视图JS配置项，如toolbars设置百度编辑器工具栏*/
    'options'=>[
        'focus'=>true,
        'toolbars'=> [
            ['fullscreen', 'source', 'undo', 'redo','paragraph','fontfamily','fontsize', 'justifyleft', 'justifyright', 'justifycenter','link','unlink','emotion', 'simpleupload', 'insertimage', 'map','print', 'spechars','horizontal'],
            ['bold', 'italic', 'underline', 'fontborder', 'strikethrough', 'superscript', 'subscript', 'removeformat', 'formatmatch', 'pasteplain', '|', 'forecolor', 'backcolor', 'insertorderedlist', 'insertunorderedlist', 'cleardoc','drafts', 'background', 'preview']
        ],
    ],

        'attributes'=>[
            'style'=>'height:80px'
        ]
    ]); ?>
```






2. yii basic 基础版。


项目覆盖到根目录。

修改 assets 目录下，UeditorWidget 和 UeditorAsset 两个文件的命名空间。

如: 
`frontend\assets\UeditorWidget;`
改为 
`assets\UeditorWidget;`

`use frontend\assets\UeditorWidget;`
改为 
`use assets\UeditorWidget;`

`<?= $form->field($model, 'comment')->widget('assets\UeditorWidget',[]); ?>`


 * ━━━━━━神兽出没━━━━━━
 * 　　　┏┓　　　┏┓
 * 　　┏┛┻━━━┛┻┓
 * 　　┃　　　　　　　┃
 * 　　┃　　　━　　　┃
 * 　　┃　┳┛　┗┳　┃
 * 　　┃　　　　　　　┃
 * 　　┃　　　┻　　　┃
 * 　　┃　　　　　　　┃
 * 　　┗━┓　　　┏━┛Code is far away from bug with the animal protecting
 * 　　　　┃　　　┃    神兽保佑,代码无bug
 * 　　　　┃　　　┃
 * 　　　　┃　　　┗━━━┓
 * 　　　　┃　　　　　　　┣┓
 * 　　　　┃　　　　　　　┏┛
 * 　　　　┗┓┓┏━┳┓┏┛
 * 　　　　　┃┫┫　┃┫┫
 * 　　　　　┗┻┛　┗┻┛
 *
 * 在git@OSC中，@web会被转码成@xiaogg。
 * 
 * ━━━━━━
