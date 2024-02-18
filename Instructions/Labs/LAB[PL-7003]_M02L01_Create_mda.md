---
lab:
    title: 'ラボ 3: モデル駆動型アプリを作成する'
    module: 'モジュール 2: Power Apps でモデル駆動型アプリを開始する'
---

# 演習 3 - モデル駆動型アプリの作成

## シナリオ

このラボでは、モデル駆動型アプリを作成し、そのアプリにテーブルを追加します。

Contoso Real Estate は 2 つの重要な要素を追跡したいと考えています:

- 不動産物件一覧
- 不動産物件の内覧予定者

## 学習する内容

- モデル駆動型アプリの作成方法
- アプリにテーブルを追加する方法

## ハイレベルラボの手順

- モデル駆動型アプリを作成する
- アプリにテーブルを追加する
  
## 前提条件

- **ラボ 2: データ モデル** を完了している必要があります。


## 詳細な手順

## 演習 1 - モデル駆動型アプリを構築する

この演習では、モデル駆動型アプリを作成します。

### タスク 1.1 – プロパティ管理アプリの作成

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. **+ New** を選択し、 **App** 、 **Model-driven app** を選択します。

    ![Screenshot of new model-driven app dialog.](../media/new-mda.png)

1. **Name** に `Property Management` と入力します。

1. **Create** を選択します。

    ![Screenshot of model-driven app designer.](../media/mda-designer.png)


### タスク 1.2 – テーブルの追加

1. **+ Add page** を選択します。

    ![Screenshot of add page to model-driven app dialog](../media/mda-new-page.png)

1. **Dataverse table** を選択します。

1. **Next** を選択します。

1. **Search** に `cre` と入力します。

    ![Screenshot of add page to model-driven app dialog.](../media/mda-add-tables.png)

1. **Open House**、 **Real Estate Property**、**Showing** を選択します。

1. **Search** に 'account' と入力し、 **Account** を選択します。

1. **Search** に `contact` と入力し、 **Contact** を選択します。

1. **Add** を選択します。

    ![Screenshot of model-driven app designer with tables.](../media/mda-designer-with-tables.png)

1. **Save** を選択します。

1. **Publish** を選択します。


### タスク 1.3 – テスト

1. **Property Management** アプリデザイナーを開いた状態で、 **Play** ボタンを選択します。

1. **Contacts** に移動します。

1. **+ New** を選択します。

1. **First Name** に `Jon` と入力します。

1. **Last Name** に `Doe` と入力します。

1. **Save & Close** を選択します。

1. **Real Estate Properties** に移動します。

1. **+ New** を選択します。

1. **Property Name** に `Test Property` と入力します。

1. **Save** を選択します。

1. **Related** と **Showings** を選択します。

    ![Screenshot of model-driven form related tables.](../media/mda-related-records.png)

1. **+ New Showing** を選択します。

1. **Name** に `First Showing` と入力します。

1. **Save & Close** を選択します。

1. **Save & Close** を選択します。

