---
lab:
    title: 'ラボ 5: モデル駆動型アプリを構成する'
    module: 'モジュール 3: モデル駆動型アプリでフォーム、グラフ、ダッシュボードを構成する'
---

# 演習 5 - モデル駆動型アプリを構成する

## シナリオ

このラボでは、モデル駆動型アプリを構成します。

## 学習する内容

- モデル駆動型アプリのナビゲーションを構成する方法
- モデル駆動型アプリでビューを制限する方法

## ハイレベルラボの手順

- ナビゲーションにグループを追加する
- ナビゲーション内のテーブルを移動する
- アプリ内での閲覧を制限する
  
## 前提条件

- **ラボ 2: データ モデル**, **ラボ 3: モデル駆動型アプリを作成する**, と **ラボ 4: フォームとビューを構成する** を完了している必要があります。

## 詳細な手順

## 演習 1 - モデル駆動型アプリを構成する

この演習では、モデル駆動型アプリのナビゲーションとテーブルを構成します。

### タスク 1.1 – グループの構成

1. Power Apps メーカー ポータル <https://make.powerapps.com> に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. 左側の **Objects** ペインで、 **Apps** を選択します。

1. **Property Management** アプリを選択し、 **Commands** メニュー (...) を選択して、 **Edit** > **Edit in new tab** を選択します。

1. **Navigation** ペインで **New Group** を選択します。

    ![Screenshot of model-driven app group.](../media/mda-group.png)

1. プロパティ ペインで、 **Title** に `Clients` と入力します。

1. **Navigation** を選択し、 **Commands** メニュー (...) **...** を選択して、 **New group** を選択します。

1. プロパティ ペインで、 **Title** に `Properties` と入力します。

1. **Navigation pane** で、 **Showings view** を選択し、 **Commands** メニュー (...) を選択して、 **Move down** を選択します。

1. **Navigation pane** で、 **Real Estate Properties view** を選択し、 **Commands** メニュー (...) を選択して、 **Move down** を選択します。

1. **Navigation pane** で、 **Open Houses view** を選択し、 **Commands** メニュー (...) を選択して、 **Move down** を3回選択します。

    ![Screenshot of model-driven app designer with navigation.](../media/mda-navigation.png)


### タスク 1.2 – ビューを制限する

1. **Navigation** ペインで、 **Showings view** を選択します。

1. **Showings** ペインで、 **Views** タブを選択します。

1. 右側のペインで、 **Inactive Showings view** を選択し、 **Commands** メニュー (...) を選択して、 **Remove** を選択します。

    ![Screenshot of removing a view in the model-driven app designer.](../media/mda-remove-view.png)

1. **Save** を選択します。

1. **Publish** を選択します。

1. アプリデザイナーで、 **Close** を選択し、 **Done** を選択します。

