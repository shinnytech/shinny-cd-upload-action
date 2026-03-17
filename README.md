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
- **endpoint**：可选，默认 `oss-accelerate.aliyuncs.com`。
- **sts-token**：可选，使用 STS 临时凭证时填写。

说明

- 当前 action 仅支持 Linux runner。
- action 会在运行时下载阿里云官方 `ossutil` 二进制，不再依赖 `manyuanrong/setup-ossutil`。
