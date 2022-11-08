# codepipeline-serverless
## 重要なファイル
- template.yaml
  - SAMリソースを定義
- hello_world/app.py
  - Lambdaハンドラーロジック
- hello_world/requirements.txt
  - 依存関係の定義。
  - `sam build`時に利用

## メモ
- `sam build`
  - .aws-samディレクトリに依存関係を解消したものを配置
  - 要らないディレクトリも生成されている(Python経験が無いだけで、必要なのかも)
- `sam deploy --guided`
  - guidedはCLIのプロンプトガイドを表示するオプション
  - 裏ではCloudFormationが動いてるっぽい
- `aws cloudformation delete-stack --stack-name sam-app --region region`
  - クリーンアップ
