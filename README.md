# medical_seikyu
## 1. 関係のあるホームページ
1. 医療機関等総合ポータルサイト  
https://iryohokenjyoho.service-now.com/csm?id=csm_index
2. 社会保険支払基金  
https://www.ssk.or.jp/seikyushiharai/online/index.html
  

  
## 2. 用意するもの
1. インターネット回線（IP－VPNまたはISDNまたはIPsec＋IKE）  
2. 回線の「お客さまID」（「CAF」+数字10桁）（ONUのラベルに書いてある）
3. 「医療機関等向け総合ポータルサイト」のログインID・PW
4. パソコン２台（オンライン請求用・オンライン資格確認用）  
5. 「オンライン請求」のIP-VPNに接続する際の「ネットワークID・ネットワークパスワード」
6. 「オンライン請求」の電子証明書  
7. 「オンライン資格確認」の電子証明書
  

  
## 3. オンライン請求について
  
### マニュアル一覧
https://iryohokenjyoho.service-now.com/csm?id=kb_article_view&sysparm_article=KB0010259#sousa_01  
  
### オンライン請求のネットワーク
対応回線の一覧:  
https://www.ssk.or.jp/seikyushiharai/online/online_04.files/claimsys35.pdf  
FAQ:  
https://www.ssk.or.jp/goshitsumon/online/online_07.html  
移転で「お客さまID」が変更されると、改めて「回線認証システム」での認証が必要。  
「お客さまID」は、ONU 本体のシールに書いてある。  
  
### オンライン請求のIP-VPN のID・PW
オンライン請求する際には、「ダイヤルアップ接続」で、つど、IP-VPN接続をする。  
その際には、ID とパスワードが必要。  
「オンライン請求ユーザ設定情報（回線接続に関する情報）」に記載されている「ネットワーク ID」と「ネットワークパスワード」である。  
例）：  
ネットワーク ID：12345678@tk123456（数字 8 桁＋@＋tk または os＋数字 6 桁）、  
ネットワークパスワード：A1b2C3d4（数字と大小英文字 8 桁の組合せ）  
医療機関等向けポータルサイト申請画面の「電気通信回線種別」で「1:IP-VPN(提供会社:NTT)」を選択し、接続に利用する回線の「お客さまID」を申請してあり、それと合致すれば、接続できる。  
- ルーターなし：光回線の回線終端装置（ONU）のLANポートに直接パソコンをつなぐ場合。
- ルーターあり：光回線の回線終端装置（ONU）とパソコンのあいだをルータで中継している場合。
IPv6 のDNS を手動設定する。  
優先DNSサーバー 2001:a7ff:f014:d00::53:1  
代替DNSサーバー 2001:a7ff:f014:d00::53:2  
  
### オンライン請求の自己署名証明書
「オンライン請求」セットアッププログラムをダウンロードするのに、まず、「自己署名証明書」をインストールする。  
これは、支払基金のホームページからダウンロードした「Online_Setup_Manual」のなかの「crt」フォルダのなかにある、「OnlineBillingNWCommonRootCA-G1.crt」である。  
  
### オンライン請求のセットアッププログラムを取得
「Online_Setup_Manual」のなかにある「Top.html」ファイルから、「電子証明書ダウンロードサイト等」に接続して、そこからダウンロードする。  
AdobeReaderDC も必要。
なお、おなじサイトから、「電子証明書の証明書発行申請サイト」、「証明書ダウンロードサイト」（専用のID、パスワードが必要）にもリンクがある。


### オンライン請求の電子証明書
審査支払機関の専用認証局が発行、発行事務コスト1,500円（3年更新）。電子証明書は、支払基金、国保連で、共通です。  
支払基金に提出の電子証明書発行依頼書に基づいて発行される、医療機関自身の電子証明書のダウンロード方法は、『共通認証局電子証明書インストールマニュアル』を参照。
https://www.ssk.or.jp/yoshiki/yoshiki_01_h30i.files/yoshiki07_03.docx  
設定方法は「共通認証局ユーザーマニュアル」。  
FAQ:  
https://www.ssk.or.jp/goshitsumon/online/online_09.html  

  
## 4. オンライン資格確認について
  
## 5. ヘルプデスク
ネットワーク回線の準備方法及び接続方法に関するお問い合わせは、ネットワークサポートデスク（電話：0120-220-571）までご連絡ください。  
「9時から17時（土曜日・日曜日・祝日及び年末年始（12月29日から1月3日）を除く。）」  
注記：ただし5日から7日は8時から21時まで、8日から10日は8時から24時まで、対応します。（土曜日・日曜日・祝日を含む。）  
  