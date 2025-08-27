# 論文タイトル:
ゼロトラスト環境におけるMITRE ATT&CK Cloud Matrixに基づく
段階伝播型リスク評価モデルの提案と評価


## 概要
このリポジトリは、[ゼロトラスト環境におけるMITRE ATT&CK Cloud Matrixに基づく
段階伝播型リスク評価モデルの提案と評価]（[JSSM第38回全国大会、2025年8月23日]）の発表に関連する
- リスク分析結果：IPA方式、SPRE方式
- 補助資料:MITRE ATT&CK Cloud Matrix 攻撃再現性スコアリング結果表(Prevalence_Score_for Cloud Matrix Technique all IDs.xls)

等を提供します。

## 本リポジトリの内容

- `/data/`: Prevalence_Score_for Cloud Matrix Technique all IDs.xls：MITRE CloudMatrix攻撃再現性スコアリング結果表
- `/data/`: ScenarioA_Attack_Path_IPA_20250822.xls：シナリオA_リスク分析結果_IPA方式
- `/data/`: ScenarioB_Attack_Paths_IPA_20250822.xls：シナリオB_リスク分析結果_IPA方式
- `/data/`: ScenarioC_IPA_Risk Score_Attack_Paths_IPA_20250822.xls：シナリオC_リスク分析結果_IPA方式
- `/data/`: ScenarioD_Attack_Paths_IPA_20250822.xls：シナリオD_リスク分析結果_IPA方式
- `/data/`: ScenarioA_SPRE_Risk Score_Attack_Path_IPA_20250803.xls：シナリオA_リスク分析結果_SPRE方式
- `/data/`: ScenarioB_SPRE_Risk Score_Attack_Paths_IPA_20250803.xls：シナリオB_リスク分析結果_SPRE方式
- `/data/`: ScenarioC_SPRE_Risk Score_Attack_Paths_IPA_20250803.xls：シナリオC_リスク分析結果_SPRE方式
- `/data/`: ScenarioD_SPRE_Risk Score_Attack_Paths_IPA_20250803.xls：シナリオD_リスク分析結果_SPRE方式
- `README.md`: 本ファイル

## 必要な環境・依存ライブラリ
- Pythonバージョン: 3.8以上でGoogle Colab上で動作
- 使用ライブラリ: numpy, pandas, matplotlib,networkx, scikit-learn など

