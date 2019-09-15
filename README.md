# Sympathies
![WhatIsSympathies](https://user-images.githubusercontent.com/32694823/64917752-abf97d00-d7ce-11e9-8c09-e262e1ef81cb.png)

# Table of contents
  - [Description](#Description)
  - [Usage](#Usage)
  - [Dependencies](#Dependencies)
  - [Installation](#Installation)
  - [Licence](#Licence)

# Description
Empowerment for Students.
"Sympathies" is a web service for sharing teaching documents and knowledge at universities.
This service is using Spring (Java).

ユーザ（学生）は授業ノート、参考資料、過去問、課題の解答等、授業に関する様々な資料を他学生と共有することができます。各学生はシステム内で使用できるポイントを持っており、それを消費することで他学生が投稿した資料を見ることができます。資料を共有した学生は、その資料がポイントで購入されるたびに、指定したポイントが加算されます。

# Usage
## Run the application
1. Javaのバージョン確認
   - 動作が確認されているJavaのバージョンは1.8です。1.8となっていることを確認ください。
1. アプリケーションの実行
   - 直接実行する場合は `./mvnw spring-boot:run` とコマンドを入力することで実行できます。
   - JARファイルを作成してから実行する場合は、 `./mvnw clean package` とコマンドを入力することで、 `target/` にJARファイルが作成されます。
  
## Change the initial data
現状ではデータベース（DB）はシステムが稼働しているときのみ保持されます（将来的には保存の機能を付ける予定です）。

データベースは次の3つがあります。
  - User DB - 学生ユーザの情報が記録されたDB。
  - Goods DB - 各ユーザが共有した資料に関するDB。
  - Transaction DB - ユーザの取引記録に関するDB。
  
また、DBの関係は次のようになっています。

![ER](https://user-images.githubusercontent.com/32694823/64917760-dcd9b200-d7ce-11e9-8f6f-7a1b680bb5fd.png)

初期値は [SympathiesApplication.java](/src/main/java/com/example/demo/SympathiesApplication.java) ファイルに記述されています。ここを変更することで初期値を自由に変更可能です。

# Dependencies
全ての依存関係は [pom.xml](/pom.xml) ファイルに記述しています。
pom.xmlの見方は [Maven – POM Reference](https://maven.apache.org/pom.html) を参照ください。

# Installation
`git clone` したのち、好きな場所に配置してください。

# Licence
[LICENCE](/LICENCE)
