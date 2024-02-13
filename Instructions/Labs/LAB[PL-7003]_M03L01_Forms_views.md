---
lab:
    title: 'ラボ 4: フォームとビューを構成する'
    module: 'モジュール 3: モデル駆動型アプリでフォーム、グラフ、ダッシュボードを構成する'
---

# 演習 4 - フォームとビューを構成する

## シナリオ

このラボでは、モデル駆動型アプリのフォームとビューを構成します。

Contoso Real Estate は 2 つの重要な要素を追跡したいと考えています:

- 不動産物件一覧
- 不動産物件の内覧予定者

## 学習する内容

- テーブルフォームの設定方法
- テーブルビューを構成する方法

## ハイレベルラボの手順

- 不動産プロパティの設定とメインフォームの表示
- タブとセクションを構成する
- フォームに列を追加する
- サブグリッドを追加する
- 新しいフォームを作成する
- セキュリティロールをフォームに関連付ける
- 不動産プロパティの構成とビューの表示
- ビューのフィルタリング
- クイック検索ビューの構成
  
## 前提条件

- **ラボ 2: データ モデル** を完了している必要があります。

## 詳細な手順

## 演習 1 - 不動産物件メインフォーム

この演習では、Real Estate Property テーブルのメイン フォームを変更します。

### タスク 1.1 – メインフォームのレイアウトと列

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. **Real Estate Property** テーブルを選択します。

1. **Data experiences** で **Forms** を選択します。

1. **Form type** が **Main** である **Information** フォームを選択し、 **Commands** メニュー (...) を選択し、 **Edit** > **Edit in new tab** を選択します。

1. フォームデザイナーの左側にある **Tree view** を選択します。

1. **General** タブを選択します。

1. **Name** に `generalTab` と入力します。

1. 右側の **Properties** ペインで、**Layout** ドロップダウンから **3 columns** を選択します。

    ![Screenshot of main form with 3 column tab.](../media/main-form-general-tab.png)

1. **Tree view** で **General** タブを展開します。最初のセクションを選択し、 **Name** に `generalSection` と入力します。

1. 2番目のセクションを選択し、 **Label** に `Timeline` と入力し、 **Name** に `timelineSection` と入力します。

1. 3番めのせきゅしょんを選択し、 **Label** に  `Related` と入力し、 **Name** に `relatedSection` を入力します。

1. **Owner** フィールドを **Header** 領域にドラッグします。

    ![Screenshot of main form with tree view and names.](../media/main-form-tab-layout.png)

1. 最初のセクションを選択します。

1. フォームデザイナーの左側のナビゲーションから **Table columns** を選択します。

1. **Client** 列を **Property Name** フィールドの下にドラッグします。

1. **Street** 列を選択して、 **Client** の下のフォームに追加します。

1. **City** 列を選択して、 **Street** の下のフォームに追加します。

1. フォームデザイナーの左側のナビゲーションから **Components** を選択します。

1. **1-column section** コントロールを選択してフォームに追加します。

1. **Label** に `Details` を入力し、 **Name** に 'detailsSection' を入力します。

1. フォームデザイナーの左側のナビゲーションから **Table columns** を選択します。

1. **Asking Price** 列を選択して、詳細セクションに追加します。

1. **Currency** 列を選択して、 **Asking Price** の下のフォームに追加します。

1. **Bedrooms** 列を選択して、 **Currency** の下のフォームに追加します。

1. **Bathrooms** 列を選択して、 **Bedrooms** の下のフォームに追加します。

    ![Screenshot of main form with table columns.](../media/main-form-first-tab.png)


### タスク 1.2 – タイムライン コントロールの追加

1. フォームデザイナーの左側のナビゲーションから **Tree view** を選択します。

1. **Timeline** セクションを選択します。

1. フォームデザイナーの左側のナビゲーションから **Components** を選択します。

1. **Display** を展開します。

1. **Timeline** コントロールを選択して、 **Timeline** セクションに追加します。

1. フォームデザイナーの左側のナビゲーションから **Tree view** を選択し、 **General** タブを展開して、 **Timeline** セクションを選択します。

1. 右側の **Properties** ペインで、 **Hide label** ボックスをオンにします。

    ![Timeline control on form.](../media/main-form-timeline.png)

1. **Tree view** で、タイムラインの **Note Text** コントロールを選択します。

1. 右側の **Properties** ペインで  **Social Activity** を選択し、 **Enable** ボックスのチェックを外して、 **Done** を選択します。

1. 右側の **Properties** ペインで、 **Sort activities by**　ドロップダウンから **Date Created** を選択します。

1. フォームデザイナーの左側のナビゲーションから **Table columns** を選択します。

1. **Status Reason** 列を **Header** 領域にドラッグします。


### タスク 1.3 – クイック ビュー コントロールの追加

1. フォームデザイナーの左側にある **Tree view** を選択します。

1. **Related** セクションを選択します。

1. フォームデザイナーの左側のナビゲーションで **Components** を選択します。

1. **Display** を展開します。

1. **Quick View** コントロールを選択して、 **Related** セクションに追加します。

1. **Lookup** として **Client** を選択し、 **Contact** として **account contact card** を選択し、 **Done** を選択します。


### タスク 1.4 – タブの追加

1. フォームデザイナーの左側のナビゲーションで、 **Components** を選択します。

1. **1-column tab** コントロールを選択してフォームに追加します。

1. **Label** に `Showings` と入力し、 **Label*** に  `showingTab` を入力します。

1. フォームデザイナーの左側で **Tree view** を選択し、 **Showings** タブを展開して、 **New Section** セクションを選択します。

1. **Label** に `Showings` と入力し、 **Label** に `showingSection` と入力します。

1. フォームデザイナーの左側のナビゲーションで、 **Components** を選択します。

1. **Grid** を展開します。

1. **Subgrid** コントロールを選択して、 **Showings** セクションに追加します。

1. **Show related records** を選択します。

1. **Table** には **Showings** を選択し、 **Default view** には、 **Active Showings** を選択し、 **Done** を選択します。

1. **Label** に `Showings` と入力し、 **Name** に `showingsSG` を入力します。

1. **Hide label** を選択します。

1. **Save and publish** を選択します。

1. フォームデザイナーを **Close** します。


## 演習 2 - メインフォームの表示

この演習では、表示テーブルのメイン フォームを変更します。

### タスク 2.1 – メインフォームのレイアウトと列

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. **Showing** テーブルを選択します。

1. **Data experiences** で、 **Forms** を選択します。

1. **Form type** が **Main** である **Information** フォームを選択し、 **Commands** メニュー (...) を選択して、 **Edit** > **Edit in new tab** を選択します。

1. **Owner** フィールドを **Header** 領域にドラッグします。

1. フォームデザイナーの左側のナビゲーションから **Table columns** を選択します。

1. **Real Estate Property** 列を **Name** フィールドの下にドラッグします。

1. **Shown to** 列を選択して、 **Real Estate Property** の下のフォームに追加します。

1. **Shown by** 列を選択して、 **Shown to** の下のフォームに追加します。

1. **Showing Date** 列を選択して、 **Shown by** の下のフォームに追加します。

1. **Level of Interest** 列を選択して、 **Showning Date** の下のフォームに追加します。

1. **Comments** 列を選択して、 **Level of Interest** の下のフォームに追加します。

1. 右側の **Properties** ペインで、 **Form field height** を **3 rows** に増やします。

1. **Save and publish** を選択します。

1. フォームデザイナーで **Close** を選択します。


## 演習 3 - 複数のフォーム

この演習では、新しいフォームを作成し、セキュリティ ロールを使用してアクセスを制限します。

### タスク 3.1 – セキュリティの役割

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. **+ New** 、 **Security** 、 **Security role** を選択します。

1. **Role Name** に `Property admin` と入力します。

1. **Custom Entities** タブを選択します。

1. **Real Estate Property** テーブルを4回選択して、すべての権限のアクセスレベルを **Organization** に変更します。

    ![Real Estate Propery privileges in security role.](../media/security-role.png)

1. **Showing** テーブルを4回選択して、すべての権限のアクセスレベルを **Organization** に変更します。

1. **Save and Close** を選択します。ソリューションに戻り **Done** を選択して変更を取得します。


### タスク 3.2 – フォームをコピーする

1. **Showing** テーブルを選択します。

1. **Data experiences** で **Forms** を選択します。

1. **Form type** が **Main** である **Information** フォームを選択し、 **Commands** メニュー (...) を選択して、 **Edit** > **Edit in new tab** を選択します。

1. **Level of Interest** を選択し、プロパティペインで **Read-only** を選択します。

1. **Comments** を選択し、プロパティペインで、 **Read-only** を選択します。

1. **Save a copy** を選択します。

1. **Display Name** に `Showing admin form` と入力し、 **Save** を選択します。

    ![Copy of Showing main form.](../media/main-form-copy.png)

1. **Form Settings** を選択します。

1. **Property admin** セキュリティロールを選択します。

    ![Main form security roles.](../media/main-form-settings.png)

1. **Save and publish** を選択します。

1. フォームデザイナーを **Close** 、 **Done** を選択します。


## 演習 4 - 不動産プロパティのビュー

この演習では、Real Estate Property テーブルのビューを変更します。

### タスク 4.1 – 不動産物件のパブリックビュー

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. **Real Estate Property** テーブルを選択します。

1. **Data experiences** で、 **Views** を選択します。

1. **Active Real Estate Properties** ビューを選択し、 **Commands** メニュー (...) を選択して、 **Edit** > **Edit in new tab** を選択します。

1. **Created On** 列の横にあるキャレットを選択し、 **Remove** を選択します。

1. **Asking Price** 列を選択してビューに追加します。

1. **City** 列を選択してビューに追加します。

1. **Bedrooms** 列を選択してビューに追加します。

1. **Bathrooms** 列を選択してビューに追加します。

1. **Client** 列を選択してビューに追加します。

1. プロパティペインで、 **Sort by** の下の **Property Name** を削除します。

1. プロパティペインで、 **Sort by** を選択し、 **Asking Price** を選択します。

    ![Real Estate Property active view.](../media/public-view.png)

1. **Save and publish** を選択します。

1. ビューデザイナーを **Close** を選択し、 **Done** を選択します。


### タスク 4.2 – 不動産物件のクイック検索ビュー

1. **Quick Find Real Estate Properties** ビューを選択し、 **Commands** メニュー (...) を選択して、 **Edit** > **Edit in new tab** を選択します。

1. **Created On** 列にあるキャレットを選択し、 **Remove** を選択します。

1. 右側の **Quick Find Active eal Estate Properties** ペインで、 **Find by** の下の **Edit find table columns** を選択します。

1. 次の列を選択し、 **Apply** を選択します。

    - City
    - Client
    - Property Name

1. **Save and publish** を選択します。

1. ビューデザイナーで **Close** を選択し、 **Done** を選択します。


## 演習 5 - ビューの表示

この演習では、表示テーブルのビューを変更します。

### タスク 5.1 – パブリック ビューの表示

1. Power Apps メーカー ポータル `https://make.powerapps.com` に移動します。

1. **Dev One** 環境にいることを確認します。

1. **Solutions** を選択します。

1. **Property listings** ソリューションを開きます。

1. **Showing** テーブルを選択します。

1. **Data experiences** で **Views** を選択します。

1. **Active Showings** ビューを選択し、 **Commands** メニュー (...) を選択して、 **Edit** > **Edit in new tab** を選択します。

1. **Created On** 列の横にあるキャレットを選択し、 **Remove** を選択します。

1. **Real Estate Property** 列を選択してビューに追加します。

1. **Showing Date** 列を選択してビューに追加します。

1. **Shown to** 列を選択してビューに追加します。

1. **Level of Interest** 列を選択してビューに追加します。

1. **Related** タブを選択します。

1. **Real Estate Property** を展開します。

1. **Asking Price** 列を選択してビューに追加します。

1. プロパティペインで、 **Sort by** の下の **Name** を削除します。

1. プロパティペインで、 **Sort by** を選択し、 **Showing Date** を選択します。

1. **Save and publish** ドロップダウンメニューで、 **Save only** を選択します。


### タスク 5.2 – 新しい表示ビュー

1. **Save As** を選択します。

1. **Name** に `High Interest showings` と入力します。

1. **Save** を選択します。

1. **Level of Interest** 列の横にあるキャレットを選択し、 **Filter by** を選択します。

1. **Equals** を選択し、 **Very High** と **High** を選択します。

1. **Apply** を選択します。

1. **Save and publish** を選択します。

1. ビューデザイナーで **Close** を選択し、 **Done** を選択します。


