# medical_seikyu

## ダウンロードもと
1. インターネット上の「①ポータルサイト」にログインできること。
2. 「①ポータルサイト」でオンライン資格確認利用申請をすると、「マスタアカウント情報」がダウンロードできるようになる。
3. インターネット上の「②医療機関等ONS」にログインできること。「①ポータルサイト」の一番下にリンクあり。
4. インターネット上の「③カードリーダーのベンダーのホームページ」は、都度、自己情報を入力すれば、ダウンロードページへ進むことができる。
5. 「③カードリーダーのベンダーのホームページ」で、「カードリーダーのマニュアル類」７冊と、「カードリーダーのソフト（９８６MB）」をダウンロードする。「設定画面：ABCDAB」「管理者：123456」「利用者654321」
6. 支払基金のIP-VPN閉域網上の「④電子証明書等ダウンロードサイト」に接続できるようにする。
7. 「①ポータルサイト」で電子証明書発行申請をし、それに対して簡易書留で送られてくる手紙に、「リクエストID・リリファレンスID（パスワード）」が書いてある。
8. 「④電子証明書等ダウンロードサイト」で、「リクエストID・リリファレンスID（パスワード）」を入力すると、電子証明書がダウンロードできる。  


## ダウンロードもと
- 「①ポータルサイト」の「手順書・マニュアル」
https://iryohokenjyoho.service-now.com/csm?id=kb_article_view&sysparm_article=KB0010259
- 「②医療機関等ONS」資格確認端末等のセットアップに関する文書等、アプリケーション等の情報
https://vendorons.service-now.com/sp?id=kb_article_view&sys_id=c8c53e911b1e6010d64633b5cc4bcb04
- 「③カードリーダーのベンダーのホームページ」の「本人認証用カードリーダーソフト」
https://www.pfu.ricoh.com/caora/support/caora01/download/fm-material-2.html
- 「④電子証明書等ダウンロードサイト」
「電子証明書ダウンロードサイト」：  
https://www.cert.download.rece/R01CALoginScr.do  
「電子証明書発行申請サイト」：  
https://cert.obn.managedpki.ne.jp/p/rcr  
「電子証明書の取得サイト」：  
https://cert.obn.managedpki.ne.jp/p/rcd  

## 流れ
1. 「医療機関等向け総合ポータルサイト」にログインできるように申請し、ID・PWをもらう。
2. ポータルサイトで、オンライン利用申請をする。インターネット回線の「お客さまID」などの情報が必要。なお、「お客さまID」は、ONU に貼ってあるシールにも書いてある。  
3. 利用申請から数日で、ポータルサイトから、「マスタアカウント情報」がダウンロードできるようになる。
4. 「オンライン処理用パソコン」を用意する。電子証明書をインストールしたり、IP-VPNの設定をしたりして、通常のインターネットとは切り替えて使う必要があるので、通常のパソコンとは別に専用のパソコンを用意したほうがよい。  
5. 支払基金のホームページから、「オンライン請求」の資料をダウンロードする。  
https://www.ssk.or.jp/seikyushiharai/online/index.html  
1. 「医療機関等ONS」にログインできるように、申請をする。
2. 「医療機関等ONS」にログインし、ブラウザ拡張プラグイン（顔認証ライブラリ含む）などをダウンロードし、そのなかに含まれる「自己署名証明書」をインストールする。
3. 「オンライン処理用パソコン」に「プロキシー」や「DNS」の設定をして、支払基金のIP-VPNの閉域網に接続する。  
4. 「オンライン処理用パソコン」に、IP-VPN 網 のなかにある「電子証明書ダウンロードサイト」から「電子証明書」をダウンロードしてインストールする。そのためには、前段で「医療機関等向け総合ポータルサイト」で電子証明書発行申請をし、それに対して簡易書留で送られてくる「リクエストID・リリファレンスID（パスワード）」を入力すると、電子証明書がダウンロードできる。  
5. 「オンライン処理用パソコン」でIP-VPN 網の「電子証明書ダウンロードサイト」に接続し、電子証明書の発行申請をし、「認証局の電子証明書」をダウンロードしてインストールする。これは１通1,500円で３年更新、接続するパソコン１台ごとに１つ必要である。したがって、「オンライン請求（月１回）」と「オンライン資格確認（診察時間中、受付カウンターで動作）」を１台のパソコンで兼ねるのがよいかもしれない。  
「電子証明書ダウンロードサイト」：  
https://www.cert.download.rece/R01CALoginScr.do  
「電子証明書発行申請サイト」：  
https://cert.obn.managedpki.ne.jp/p/rcr  
「電子証明書の取得サイト」：  
https://cert.obn.managedpki.ne.jp/p/rcd  
1. 「電子証明書等ダウンロードサイト」から、「オンライン請求」のセットアッププログラムと自己証明書をダウンロードして、それぞれインストールする。  
2.   以上で、まずは「オンライン請求」ができる状態になった。
3.   引き続いて、「オンライン資格確認」できるようにする。
4.   「オンライン資格確認」のセットアップ資料に基づいて、Windows にユーザーを追加したり、「医療機関等ONS」から、ブラウザ拡張プラグイン（必須）「OQSFaceApp.zip」 、連携アプリケーション　「OQSComApp.zip」 、配信アプリケーション　「OQSDistroApp.zip」 、MPKIクライアント　「CybertrustManagedPKIClient.zip」を入手してインストールする。  
5.   「医療機関等ONS」:  
https://vendorons.service-now.com/  
1.   「医療機関等ONS」登録申請:  
https://vendorons.service-now.com/nav_to.do?uri=%2Frequest_account  
  
### 必要な情報
1. 「医療機関等向け総合ポータルサイト」のログインID・PW  
2. インターネット回線の「お客さまID」（ONUのラベルに書いてある「CAF + 数字10桁」）  
3. IP-VPNに接続する際に必要な、「オンライン請求ユーザ設定情報（回線接続に関する情報）」に記載されている「ネットワークID・ネットワークパスワード」  
4. 電子証明書を申請すると、簡易書留で送られてくる「リクエストID」「リファレンスID」（IP-VPNの閉域網上の電子証明書等ダウンロードサイトにログインするID）  
5. 「オンライン請求・資格確認」の利用申請をすると発行される「マスタアカウント」のユーザーID、PW（オンライン資格確認システムに最初にログインするID。）
  
### 必要なプログラム、電子証明書など
1. IP-VPN に接続するにあたっての「自己署名証明書」（支払基金からダウンロードしたマニュアルに同梱）  
2. 請求システムや資格確認システムに接続するための「認証局の電子証明書」。これは、IP-VPN で接続した「電子証明書ダウンロードサイト」からダウンロードする。  
3. 「オンライン請求セットアッププログラム」を「電子証明書ダウンロードサイト」からダウンロードする。
4. 「医療機関等ONS」に登録申請して、ログインして、ブラウザ拡張プラグイン（必須）OQSFaceApp.zip（delegate.crx 目視確認操作用アプリケーション・nopinauth.crx 顔認証用アプリケーション・pinauth.crx 暗証番号認証用アプリケーション） 、連携アプリケーション　OQSComApp.zip 、配信アプリケーション　OQSDistroApp.zip 、MPKIクライアント　CybertrustManagedPKIClient.zip を入手してインストールする。
  
## 関係のあるホームページ
1. 医療機関等総合ポータルサイト  
https://iryohokenjyoho.service-now.com/csm?id=csm_index
2. 社会保険支払基金の「オンライン請求」資料集  
https://www.ssk.or.jp/seikyushiharai/online/index.html
3. 医療機関等総合ポータルサイトの「オンライン資格確認」資料集
ttps://iryohokenjyoho.service-now.com/csm?id=kb_article_view&sysparm_article=KB0010259#sousa_01  
4. 「医療機関等ONS」:  
https://vendorons.service-now.com/  
  
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
別途送付される「ユーザ設定情報」及び「電子証明書」は、オンライン請求及び特定健診・保健指導システムで使用するパソコンを変更するときにも必要になる。  
https://www.ssk.or.jp/yoshiki/yoshiki_01_h30i.files/yoshiki07_03.docx  
設定方法は「共通認証局ユーザーマニュアル」。  
FAQ:  
https://www.ssk.or.jp/goshitsumon/online/online_09.html  
  
### オンライン請求の「認証局の電子証明書」ダウンロードサイト
https://www.cert.download.rece/R01CALoginScr.do
ただしこれは、インターネット上ではなく、IP-VPN 網のなかにある。  

### オンライン請求の「認証局の電子証明書」のダウンロード
電子証明書発行通知書の「電子証明書取得に関する情報」に記載のリクエストIDとリファレンスID及び任意のパスワード（半角数字4桁）を入力すると、ダウンロードできる。  
なお、「オンライン資格確認」でも、この「認証局の電子証明書」が使える。  
「発行者」は「Online Billing NW Common Root CA」である。  
ただし、パソコンが別々で２台ある場合は、各１台ごとに必要？  
もしくは、１台のパソコンで、普段は「オンライン資格確認」パソコンとしておき、請求のときのみ「オンライン請求」につなぎ直す、か。  
  


## 4. オンライン資格確認について
  
## 5. ヘルプデスク
ネットワーク回線の準備方法及び接続方法に関するお問い合わせは、ネットワークサポートデスク（電話：0120-220-571）までご連絡ください。  
「9時から17時（土曜日・日曜日・祝日及び年末年始（12月29日から1月3日）を除く。）」  
注記：ただし5日から7日は8時から21時まで、8日から10日は8時から24時まで、対応します。（土曜日・日曜日・祝日を含む。）  
  