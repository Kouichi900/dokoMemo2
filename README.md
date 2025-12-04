# どこメモ2 (dokoMemo2)

JSP と Servlet を使った、簡易メモ帳アプリです。  
ユーザーはログイン後、メモをタイトル・内容・日時つきで登録し、一覧で確認できます。  
H2データベース（Embedded モード）を使用しています。

---

## 💻 主な機能

- ログイン機能（セッション管理）
- メモの投稿（タイトル・内容・日付・時刻）
- メモ一覧の表示（最新順）
- メモ削除チェックボックス（今後対応予定）

---

## 🧰 使用技術

| 技術           | バージョンなど                  |
|----------------|-------------------------------|
| Java           | JDK 21（Eclipse Adoptium）     |
| Webサーバー    | Apache Tomcat 10.1.x           |
| IDE            | Eclipse Pleiades 2024-12       |
| DB             | H2 Database 2.x（Embedded）     |
| その他         | JSP / Servlet / HTML / CSS     |

---

## 🛠 セットアップ手順

1. **Eclipseでプロジェクトをインポート**  
   Pleiades（日本語Eclipse）を使って `dokoMemo2` プロジェクトを読み込む

2. **H2 Database の JAR を配置**  
   `h2-x.x.x.jar` を `WebContent/WEB-INF/lib/` にコピー

3. **Tomcat 10.1 をサーバーに設定**  
   Eclipseのサーバータブで Tomcat を設定しておく

4. **起動とアクセス**  
   Tomcatを起動し、以下にアクセス  
   ```
   http://localhost:8080/dokoMemo2/Main
   ```

---

## 📁 プロジェクト構成（例）

```
dokoMemo2/
├── src/
│   └── model/
│       └── Memo.java
│   └── dao/
│       └── MemoDAO.java
│   └── servlet/
│       └── Main.java
├── WebContent/
│   ├── index.jsp        // ログイン画面
│   ├── main.jsp         // メイン画面（メモ登録・表示）
│   └── WEB-INF/
│       └── web.xml      // サーブレット設定
```

---

## 📷 スクリーンショット

![dokoMemo2 コード]
<img width="2434" height="1379" alt="image" src="https://github.com/user-attachments/assets/62b03484-bc27-4595-b996-66999775bfb0" />

![dokoMemo2 メモ画面]
<img width="2473" height="1353" alt="image-1" src="https://github.com/user-attachments/assets/90d4feb5-6354-4c4d-a23e-39fbc84fba1c" />

---

## 👤 開発者

- 渡辺 浩一（Koichi Watanabe）

---

## 📄 ライセンス

MIT License（自由に使ってください）

---

## 📝 補足

このアプリはローカル環境（localhost）用に作られています。  
スマートフォンや他のPCからアクセスするには、PCを起動した状態で、  
IPアドレスとポート（例：`http://localhost:8080/dokoMemo2/index.jsp`）でアクセスする必要があります。

