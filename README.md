# renovate-config

[![Licence](https://img.shields.io/github/license/tpu-dsg/renovate-config)](./LICENSE)

このリポジトリは、組織内の各プロジェクトで利用する Renovate の共通設定を一元管理するためのものです。Renovate は依存関係の自動更新ツールであり、統一されたポリシーを適用することで、保守性を向上させることを目的としています。

## 使用方法

1. **Renovate のインストール**: 各プロジェクトに対して [Renovate Bot](https://github.com/apps/renovate)と を導入してください。自動マージを有効にするには、[ルールのバイパスを設定する](https://github.blog/changelog/2021-11-19-allow-bypassing-required-pull-requests/)か、[renovate-approve](https://github.com/apps/renovate-approve)を導入してください。
1. **共通設定の参照**: 各プロジェクトに配置する Renovate 設定ファイル（例: `.github/renovate.json`）に、以下のように共通設定ファイルへの参照を記述します。プロジェクト固有の要件がある場合は、共通設定を上書きする形で追加設定を記述します。

```json
{
  "extends": ["github>tpu-dsg/renovate-config"]
}
```

## 貢献方法

このリポジトリへの改善提案、バグ修正、または新たな機能追加の提案はいつでも歓迎します。手順は[貢献ガイド](https://github.com/tpu-dsg/.github/blob/main/CONTRIBUTING.md)を参照してください。
