#PPIVの建設領域 / BackEnd領域のさかもと個人のまとめ

##チーム議事録集

  - [Team MTG](team-mtg.md)
  - [Design Review](design-review.md)
  - [Others](others-minutes.md)

##PPIV領域OverView

####■PPIV (Procurement/Purchase/Inventory) 領域に含まれる諸要素

業務領域のカバーとして以下の機能が該当する：一般的な組分け

  * Purchase (間接材の購入)
  
    * 一般購買：備品などを購入する
    * 検収管理：備品などの検収を行なう
    * 仕入管理：備品などの仕入後仕訳を立てる -> Assetへ
    
  * Procurement (直接材の購入)
  
    * 見積管理：取引先へ見積依頼を出し取引金額を決定する
    * 発注管理：確定した発注契約を結ぶ
    * 入荷管理：直接材を受入 -> Inventoryへ(即検収では自社在庫)
    * 検査管理：入荷をした物品の検査
    * 検収管理：入荷をした物品の社内受入判断 -> Inventoryへ(自社在庫)
    * 仕入管理：仕入完了と仕訳作成 -> 在庫評価へ
    * 支給管理：外注と外注受けで支給材の管理 -> Inventoryへ(預け/かり在庫)
    
  * Construction (Procurement)
  
    * [出来高管理：後述; Click-> ](progressbased.md)
    * [相殺予定報告管理：後述; Click-> ](plannedoffset.md)
    
  * Inventory
  
    * 在庫管理

##PPIVサブシステム間マップ

  [gimmick:yuml]( [Request|購入依頼]-->[Quotation|見積], [Quotation|見積]-->[Order|発注], [Request|購入依頼]-->[Order|発注], [Order|発注]-->[Acceptance|入荷受入], [Order|発注]->[Progress-Inspection|出来高管理], [Order|発注]-->[Offset|相殺予定], [Progress-Inspection|出来高管理]-->[Offset|相殺予定], [Acceptance|入荷受入]-->[Quarantine-Inspection|検査], [Acceptance|入荷受入]-->[Collating|検収], [Quarantine-Inspection|検査]-->[Collating|検収])

--------

##クラス図の例：境界部分を記述で使う

■見積->発注(システムマップ;No.1)
　[gimmick:yuml]( [User|+Forename;+Surname;+HashedPassword;+Salt|]JavaAPI -.->[Response])


--------

##現在の調達領域(PP)のシステム的な課題

SCMを取り扱うシステムにおけるパッケージ商品から見た問題点

  1. 物流網と商流網の間で、サブシステム間のデータ取扱タイミングが異なるため、各サブシステムを
     統合的に運用するためにはスクラッチ開発を必要とする。
  1. 特に製造業において、生産システムとERPとしての在庫システムとの間で乖離がある。
  1.
  1.
  1.
  1.
  1.
  1.
  1.
  1.



####HUEとしての調達領域(PP)のシステム的な課題

####現在の在庫領域(IV)のシステム的な課題

####HUEとしての在庫領域(IV)のシステム的な課題


----------
##建設領域の詳細




----------
##BackEnd領域の概説
