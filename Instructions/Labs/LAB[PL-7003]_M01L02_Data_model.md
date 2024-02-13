---
lab:
    title: 'ラボ 2: データ モデル'
    module: 'モジュール 1: Dataverse でテーブルを作成する'
---

# 演習 2 - データ モデル

## シナリオ

このラボでは、Dataverse のテーブル、列、リレーションシップを作成します。

Contoso Real Estate は、次の 2 つの重要な要素を追跡したいと考えています:

- 不動産物件一覧
- 不動産物件の内覧予定者

## 学習する内容

- Dataverse でテーブルを作成する方法
- Dataverse テーブルに列を追加する方法
- テーブル間のリレーションシップを作成する方法

## ハイレベルラボの手順

- テーブルの作成
- 列の作成
- 関係を築く
  
## 前提条件

- **ラボ 1: パブリッシャーとソリューション** を完了している必要があります

## 詳細な手順

## 演習 1 - テーブルの作成

この演習では、テーブルを作成してソリューションに追加します。

### タスク 1.1 – 不動産物件テーブルの作成

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. **+ New** を選択し、 **Table** を選択し、再度、 **Table** を選択します。

    ![Screenshot of new table pane](../media/new-table-pane.png)

1. **Display Name** に `Real Estate Property` と入力します。複数名は、自動的に入力されます。

1. **Primary column** タブを選択します。

1. **Display Name** に `Property Name` を入力します。

1. **Advanced options** を展開し、利用可能なオプションを確認します。ただし、ここでは、何も変更しません。

    ![Screenshot of table primary column tab](../media/primary-column-tab.png)

1. **Properties** タブを選択します。

1. **Advanced options** を展開します。

1. **Creating a new activity** にチェックを入れます。

1. **Appear in search results** をオンにします。

    ![Screenshot of table advanced options](../media/table-options.png)

1. **Save** を選択します。


### タスク 1.2 – 表示テーブルの作成

1. **Objects** ペインで、 **All** を選択します。

1. **+ New** を選択し、 **Table** を選択し、再度、 **Table** を選択します。

1. **Display Name** に 'Showing' と入力します。複数名は、自動的に入力されます。

1. **Advanced options** を展開します。

1. **Appear in search results** にチェックを入れます。

1. **Save** を選択します。


### タスク 1.3 – オープンハウステーブルの作成

1. **Objects** ペインで、 **All** を選択します。

1. **+ New** を選択し、 **Table** を選択し、再度、 **Table** を選択します。

1. **Display Name** に `Open House` と入力します。複数名は、自動的に入力されます。

1. **Advanced options** を展開します。

1. **Record ownership** として **Organization** を選択します。

1. **Save** を保存します。


### タスク 1.4 – 連絡先テーブルの追加

1. **Objects** ペインで、 **All** を選択します。

1. **Add existing** を選択し、 **Table** を選択します。

1. **Contact** テーブルを選択します。

1. **Next** を選択します。

1. **Add** を選択します。


## 演習 2 - 列の作成

この演習では、ソリューションのテーブルに列を作成します。

### タスク 2.1 – 不動産プロパティ列の作成

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** ソリューションを選択します。

1. **Property listings** ソリューションを開きます。

1. **Real Estate Property** テーブルを選択します。

1. **Properties** を選択します。

    ![Screenshot of Real Estate Property table](../media/real-estate-property-table.png)

1. **Enable attachments** をオンにして、 **Save** を選択します。

1. **Schema** で **Columns** を選択します。

1. **+ New column** を選択します。

    ![Screenshot of new column pane](../media/new-column-pane.png)

1. **Display name** に `Asking Price` と入力します。

1. **Data type** ドロップダウンで、 **Currency** を選択します。

1. **Required** ドロップダウンで、 **Business required** を選択します。

1. **Save** を選択します。

1. **+ New column** を選択します。

1. **Display name** に `Street` と入力します。

1. **Required** ドロップダウンで、 **Business required** を選択します。

1. **Save** を選択します。

1. **+ New column** を選択します。

1. **Display name** に `City` と入力します。

1. **Required** ドロップダウンで、 **Business required** を選択します。

1. **Save** を選択します。

1. **+ New column** を選択します。

1. **Display name** に `Bedrooms` と入力します。

1. **Date type** ドロップダウンで、 **Choice** を選択し、再度、 **Choice** を選択します。

    ![Screenshot of new choice column pane](../media/add-choice.png)

1. **Sync with global choice** で **Yes** を選択します。

1. **+ New choice** を選択します。

    ![Screenshot of new global choice pane](../media/new-global-choice.png)

1. **Display name** に `Number of Rooms` を入力します。

1. **Label** に `1` を入力し、 **Value** に '1' を入力します。

1. **+ New choice** を選択し、 **Label** に `2` を入力し、 **Value** に '2' を入力します。

1. **+ New choice** を選択し、 **Label** に `3` を入力し、 **Label** に `3` を入力します。

1. **+ New choice** を選択し、 **Label** に `4` を入力し、 **Label** に `4` を入力します。

1. **+ New choice** を選択し、 **Label** に `5` を入力し、 **Label** に `5` を入力します。

    ![Screenshot of completed global choice pane](../media/global-choice.png)

1. **Save** を選択します。

1. **Sync this choice with** で **Number of Rooms** を選択します。

1. **Save** を選択します。

1. **+ New column** を選択します。

1. **Display name** に `Bathrooms` と入力します。

1. **Data type** ドロップダウンで、 **Choice** を選択し、再度、 **Choice** を選択します。

1. **Sync this choice with** で **Number of Rooms** を選択します。

1. **Save** を選択します。


### タスク 2.2 – 表示列の作成

1. **Objects** ペインで、 **All** を選択します。

1. **Showing** テーブルを選択します。

1. **Schema** の下で、 **Columns** を選択します。

1. **+ New column** を選択します。

1. **Display name** に `Showing Date` を入力します。

1. **Data type** ドロップダウンで、 **Date and time** を選択します。

1. **フォーマット** ドロップダウンで、 **Date only** を選択します。

1. **Required** 土ラップダウンで、 **Business required** を選択します。

1. **Save** を選択します。

1. **+ New column** を選択します。

1. **Display name** に `Comments` を入力します。

1. **Data type** ドロップダウンで、 **Text** を選択し、 **Multiple lines of text** で、 **Plain text** を選択します。

1. **Save** を選択します。

1. **Display name** に `Level of Interest` を入力します。

1. **Data type** ドロップダウンで、 **Choice** を選択し、再度、 **Choice** を選択します。

1. **Sync with global choice** で、 **No** を選択します。

1. **Label** に `Very High` と入力します。

1. **+ New choice** を選択し、**Label** に 'High' と入力します。

1. **+ New choice** を選択し、 **Label** に `Medium` と入力します。

1. **+ New choice** を選択し、 **Label** に `Low` と入力します。

1. **+ New choice** を選択し、 **Label** に `No interest` と入力します。

1. **Save** を選択します。

1. **+ New column** を選択します。

1. **Display name** に `Shown by` と入力します。

1. **Data type** ドロップダウンで、 **Lookup** を選択し、再度 **Lookup** を選択します。

1. **Related table** ドロップダウンで、 **User** を選択します。

1. **Save** を選択します。


### タスク 2.3 – オープンハウスの列を作成する

1. **Objects** ペインで、 **All** を選択します。

1. **Open House** テーブルを選択します。

1. **Schema** 下で、 **Columns** を選択します。

1. **+ New column** を選択します。

1. **Display name** に `Open House Date` と入力します。

1. **Data type** ドロップダウンで、 **Date and time** を選択します。

1. **フォーマット** ドロップダウンで、 **Date only** を選択します。

1. **Required** ドロップダウンで、 **Business required** を選択します。

1. **Save** を選択します。


## 演習 3 - リレーションシップを作成する

この演習では、ソリューションに対するテーブル間の関係を作成します。

### タスク 3.1 – 不動産物件と連絡先のリレーションシップ

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. **Real Estate Property** テーブルを選択します。

1. **Schema** スキーマ下で、 **Relationships** を選択します。

1. **+ New relationship** を選択し、 **Many-to-one** を選択します。

1. **Related (One) Table** ドロップダウンで、 **Contact** を選択します。

1. **Lookup column display name** に `Client` と入力します。

1. **Lookup column requirement** ドロップダウンで、 **Business Required** を選択します。

1. **Done** を選択します。


### タスク 3.2 – 不動産物件と表示関係

1. **+ New relationship** を選択し、 **One-to-many** を選択します。

1. **Related (Many) Table** ドロップダウンで、 **Showing** を選択します。

1. **Lookup column requirement** ドロップダウンで、 **Business Required** を選択します。

1. **Done** を選択します。


### タスク 3.3 – 不動産物件とオープンハウスの関係

1. **+ New relationship** を選択し、 **One-to-many** を選択します。

1. **Related (Many) Table** ドロップダウンで、 **Open House** を選択します。

1. **Lookup column requirement** ドロップダウンで、 **Business Required** を選択します。

1. **General** を選択します。

1. **Relationship name** に `realestateproperty_openhouse` と入力します。

1. **Done** を選択します。


### タスク 3.4 – 連絡先リレーションシップの表示

1. **Objects** ペインで、 **All** を選択します。

1. **Showing** テーブルを選択します。

1. **Schema** の下で、 **Relationships** を選択します。

1. **+ New relationship** を選択し、 **Many-to-one** を選択します。

1. **Related (One) Table** ドロップダウンで、 **Contact** を選択します。

1. **Lookup column display name** に `Shown to` と入力します。

1. **Done** を選択します。

