---
lab:
    title: 'ラボ 1: パブリッシャーとソリューション'
    module: 'モジュール 1: Dataverse でテーブルを作成する'
---

# 実践 1 - パブリッシャーとソリューション

## シナリオ

このラボでは、パブリッシャーとソリューションを作成します。

## 学習する内容

- Microsoft Dataverse でソリューションを作成する方法
- 既存のコンポーネントをソリューションに追加する方法

## ハイレベルラボの手順

- パブリッシャーの作成
- ソリューションの作成
- テーブル、列、ビュー、フォームをソリューションに追加する
  
## 前提条件

- **ラボ 0: ラボ環境を検証する** を完了している必要があります

## 詳細な手順

## 演習 1 - パブリッシャーとソリューションを作成する

この演習では、Power Apps メーカー ポータル、開発者環境にアクセスし、新しいソリューションを作成します。

### タスク 1.1 – Maker ポータル

1. 新しいタブで Power Apps メーカー ポータル `https://make.powerapps.com` に移動し、再度プロンプトが表示されたら Microsoft 365 資格情報を使用してサインインします。

1. **Phone number** の入力を求められたら、 `0123456789` と入力し、 **Submit** を選択します。

1. 画面右上隅の環境セレクターを使用して環境を切り替えます。

1. リストから **Dev One** 環境を選択します。

    ![Select Development environment in the Power Apps maker portal.](../media/select-dev-one-environment.png)

1. 左側のナビゲーション ペインから **Apps** を選択し、次に **All** を選択します。 Dataverse Accelerator App, Solution Health Hub, Power Pages Management, and Package Management View などのいくつかのアプリがリストされているはずです。

1. 左側のナビゲーション ペインから **Tables** を選択します。取引先と連絡先を含む *Common Data Model* の標準テーブルが表示されるはずです。

### タスク 1.2 – ソリューションと発行者の作成

1. 左側のナビゲーション ペインから **Solutions** を選択します。 *Default Solution* や *Common Data Services Default Solution* など、いくつかのソリューションが表示されるはずです。

    ![List of solutions in Maker portal.](../media/solutions-list.png)

1. **+ New solution** を選択します。

1. **Display name** テキストボックスに、 **`Property listings`** と入力します。

1. **Name** が自動的に入力されることを確認します。

1. **Publisher** ドロップダウンの下にある **+ New publisher** を選択します。

1. **Display name** に `Contoso Real Estate` と入力します。

1. **Name** に `contosorealestate` と入力します。

1. **Prefix** には、 `cre` と入力します。

    ![New publisher.](../media/new-publisher.png)

1. **Save** を選択します。

1. **Publisher** ドロップダウンで、 **Contoso Real Estate (contosorealestate)** を選択します。

1. **Create** を選択します。

    ![New solution.](../media/new-solution.png)

## 演習 2 - ソリューションにコンポーネントを追加する

この演習では、既存のテーブルをソリューションに追加します。

### タスク 2.1 – テーブルの追加

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. 前の演習から、 **Contoso Real Estate** ソリューションを選択します。

    ![Property listing solution objects.](../media/solution-objects.png)

1. **Add existing** を選択し、 **Table** を選択します。

    ![Add existing tables.](../media/add-existing.png)

1. **Account** テーブルを選択します。

    ![Add tables.](../media/add-tables.png)

1. **Next** を選択します。

1. **Account** テーブルの下で、 **Select objects** リンクを選択します。

1. **Columns** タブで、 **Account Number** 列を選択します。

1. **Views** タブを選択します。

1. **Active Accounts** ビューを選択します。

1. **Forms** タブを選択します。

1. **Account** フォームを選択します。

1. **Add** を選択します。

    > **注:** **Acount** テーブルに対して１つのビュー、１つのフォーム、および１つの列を選択しておく必要があります。

    ![Add table objects.](../media/add-objects.png)

1. **Add** を選択します。
