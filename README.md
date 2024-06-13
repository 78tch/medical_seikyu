# medical_seikyu
  
## 1.利用するシステム
1. 支払基金・国保連合会のIP-VPN閉域網上の「オンライン資格確認システム」（カードリーダー含む）  
2. IP-VPN閉域網上の「オンライン請求システム」
  
のふたつ。  
## 2.必要な申請
- 「医療機関等向け総合ポータルサイト」にて  
1. 「オンライン資格確認」利用申請：これにより、IP-VPN閉域網上の「オンライン資格確認システム」にログインする際のID・PWが書かれたPDFがダウンロードできるようになる。  
2. 「オンライン請求」利用開始・変更申請：IP-VPN閉域網上の「オンライン請求システム」にログインする際のID・PWが書かれたPDFがダウンロードできるようになる。  
3. 「電子証明書申請」：IP-VPN閉域網上の「オンライン各種システム」を利用するのに必要な、「認証局の電子証明書」が発行される。まず、簡易書留でID・PWが書かれた紙が届き、それを使って、IP-VPN閉域網上の「電子証明書ダウンロードサイト等」から「認証局の電子証明書」をダウンロードする。  
  
- 「医療機関等ONS」にて
1. サイトのWebフォームから「サイトの利用登録」をすると、ログインできるようになる。顔認証連携アプリや資料などをダウンロードできる。
  
- 「カードリーダーのベンダー（富士通Japan）のHP」
登録は不要だが、ログインにあたり、毎回、自己情報を入力する必要あり。  
  
## 3.事前に用意・ダウンロードするもの一覧（プログラム、資料、電子証明書など）
1. 「オンライン資格確認システム」の「マスタアカウント情報」。（オンライン資格確認利用申請により。）※ログインにのみ使用し、常用するアカウントは自分で作成する。  
2. 「オンライン請求システム」の「ユーザIDとパスワード」。（オンライン請求利用開始・変更申請により。）  
3. 「認証局の電子証明書」をダウンロードするためのリクエストID・リファレンスID（電子証明書発行申請により。これのみ、簡易書留で届く。）  
4. オンライン請求の資料（Online_Setup_Manual）。「支払基金のHP」からダウンロードする。そのなかの「crt」フォルダのなかに、「自己署名証明書」（OnlineBillingNWCommonRootCA-G1.crt）も入っている。この資料の説明にしたがって、IP-VPN閉域網上の「電子証明書ダウンロードサイト等」から、セットアッププログラム（OnlineSetup_Iryou_Windows）と、AdobeReaderDC もダウンロードする。  
5. 顔認証連携アプリ（OQSFaceApp_v3.1.1.zip）など。「医療機関等ONS」からダウンロードする。  
6. カードリーダーソフト（PFU-CaoraApp_v1.8.2.1.zip）。「カードリーダーのベンダー（富士通Japan）のHP」から、「カードリーダーのマニュアル類」７冊と、「カードリーダーのソフト（９８６MB）」をダウンロードする。「設定画面：ABCDAB」「管理者：123456」「利用者654321」事前登録などはなく、都度、自己情報を入力すれば、ダウンロードページへ進むことができる。  
7. 認証局の電子証明書。IP-VPN閉域網上の「電子証明書ダウンロードサイト等」からダウンロードする。  
8. オンライン請求のセットアッププログラム。IP-VPN閉域網上の「電子証明書ダウンロードサイト等」からダウンロードする。  
  
## 4.システム利用までの流れ
1. 接続用パソコンに、ネットワーク設定をする。Windowsのログインユーザー、DNS、プロキシー、NTPなど。（資料によっては、「PPPoEの設定」の記述があるが、内容が古く、不要。「ネットワークID」と「ネットワークパスワード」８桁@tk６桁、８桁というのは、なくてよい。）  
2. オンラインシステム用のパソコンで、設定したプロキシサーバーを有効にしている間は、一般のインターネットにはつながらなくなるので、インターネットにつなぐ場合はプロキシを無効にし、オンラインシステムを使用するはプロキシを有効にする、と切り替える必要がある。もしくはオンラインシステム専用のパソコンを用意して常にプロキシを有効にする。  
3. IP-VPN閉域網に接続できるのは、事前に登録したフレッツ回線を使ってつないだ場合のみ。「オンライン資格確認利用申請」によって、フレッツ回線の「お客さまID」がIP-VPN閉域網に登録され、接続できるようになる。
4. IP-VPN閉域網へ接続し、「回線認証サイト」に接続して回線を認証してもらってから、まず「電子証明書ダウンロードサイト等」で「認証局の電子証明書」をダウンロードして、インストールする。
5. 以上の設定をしたあとに、「オンライン資格確認システム」や「オンライン請求システム」に、利用申請で発行されたID・PWでログインする、という手順になる。  
6. 「オンライン資格確認システム」では、まず「管理者アカウント」、「顔認証用アカウント」、「一般利用者アカウント」を作成する。  
7. 「オンライン請求システム」は、支払基金と国保連で分かれているのでそれぞれに進み、まずは「運用マニュアル」をダウンロードして、内容を確認する。  
  
https://www.ssk.or.jp/seikyushiharai/online/index.html  
  
## 5.関係サイトのURL
1. 「医療機関等向け総合ポータルサイト」：  https://iryohokenjyoho.service-now.com/csm  
2. 「支払基金のHP」：  https://www.ssk.or.jp/seikyushiharai/online/index.html  
3. 「医療機関等ONS」：  https://vendorons.service-now.com/sp  
4. 「カードリーダーのベンダー（富士通Japan）のHP」：  https://www.pfu.ricoh.com/caora/support/caora01/fm-material-1.html  
5. 支払基金のIP-VPN閉域網上の「電子証明書等ダウンロードサイト」：  https://www.cert.download.rece/R01CALoginScr.do  
「電子証明書発行申請サイト」：  
https://cert.obn.managedpki.ne.jp/p/rcr  
「電子証明書の取得サイト」：  
https://cert.obn.managedpki.ne.jp/p/rcd  
  
  

### 6.「認証局の電子証明書」について
審査支払機関の専用認証局が発行、発行事務コスト1,500円（3年更新）。電子証明書は、支払基金、国保連で、共通です。  
ポータルサイトで提出した電子証明書発行依頼書に基づいて発行される。医療機関自身の電子証明書のダウンロード方法は、『共通認証局電子証明書インストールマニュアル』を参照。  
別途送付される「ユーザ設定情報」及び「電子証明書」は、オンライン請求及び特定健診・保健指導システムで使用するパソコンを変更するときにも必要になる。  
https://www.ssk.or.jp/yoshiki/yoshiki_01_h30i.files/yoshiki07_03.docx  
設定方法は「共通認証局ユーザーマニュアル」。  
FAQ:  
https://www.ssk.or.jp/goshitsumon/online/online_09.html  
  