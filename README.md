📌 運用方法
	1.	rules-management リポジトリを作成して rules.txt を管理
	2.	ルール変更が承認されたら ChatGPTが最新版を生成
	3.	アップロード or API経由でcommit
	•	手動：GitHubで「Upload file」→ Commit
	•	自動：Make＋GitHub APIでcommit
	4.	以後は Raw URL を常に参照して運用

⸻

📌 ポイント
	•	バージョン管理：すべての更新は commit として記録 → 差分確認・ロールバック可能
	•	Commitメッセージを明確に：Update rules.txt: add email subject tags など
	•	キャッシュ遅延に注意：Raw URLの反映に数分かかることがある
	•	承認フロー一貫性：ChatGPTが全文＋差分提示 → あなたの承認後のみ commit
	•	将来は自動化：承認 → .eml生成 → MakeがGitHub API経由で更新、という流れでミス防止
