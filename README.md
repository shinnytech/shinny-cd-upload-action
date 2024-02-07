# shinny-cd-upload-action

把项目文件上传到 oss


用例:

```yaml
steps:
  - name: Upload to oss
    uses: shinnytech/shinny-cd-upload-action@master
    with:
      access-key-id: ${{ secrets.OSS_ACCESS_KEY }}
      access-key-secret: ${{ secrets.OSS_SECRET_KEY }}
      upload-from-dir: hedge/dist
      upload-target: hedge
```


参数

- **upload-from-dir**：填写要上传的目录。
- **upload-target**：填写服务名称。
- **access-key-id**：查看方式请参考创建 AccessKey。
- **access-key-secret**：查看方式请参考创建 AccessKey。

