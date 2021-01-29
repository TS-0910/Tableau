# Tableauでの営業成績の可視化・ダッシュボード作成

現職の人材紹介業における自分の実績の可視化と考察です。

"Placement"と"BI,IV,Offer"の二種類があります。

###Placements
![Placements](https://github.com/TS-0910/Tableau/blob/main/Placements/Placements%20Stats_26.1.2021.png)

###BI,IV,Offer
![BI,IV,Offer](https://github.com/TS-0910/Tableau/blob/main/BI%2C%20IV%2C%20Offer_29.1.2021.png)

##①用語の解説
<u>"Placement Stats"の用語</u>
Placement…企業に候補者を紹介→内定→実際に転職という一連の流れのサポート
Internal IT…いわゆる事業会社と言われる企業の社内情報システム部
Consulting…BIg4等で知られるコンサル企業
Vendor…事業会社からのアウトソース先としてITサービスを提供する企業

<u>"BI, IV, Offer"の用語</u>
ポジション…Clientから依頼のあった求人
IR…"Interview Request"。特定のポジションに対して面接の依頼が入った数
IV…"Interview" = 面接。今回は、IV = 1st interviewとして集計。
Offer…Job Offer = 内定
SL…"Short List"。ポジションに対して、何人の候補者に声をかけたか(=何人をShort Listに入れたか)
BI…"Buy In"。そのポジションに対して、申し込み(= Buy In)のあった数
Client…求人を出している企業。そのポジションに対しての候補者のソーシングを依頼している企業

##②人材紹介・担当分野の流れについて
1.Clientから求人に合う候補者を探してほしいという依頼が入る
2.自社データベースやその他媒体で候補者をソーシングする
3.候補者から申し込み(Buy In)をもらう
4.Clientに紹介し、スクリーニングの結果Interviewが入る
5.面接が通過すれば、Offerが出る

自分は主に外資系企業のInternal ITポジションを担当。

##③ダッシュボードの解説
<u>1."Placements Stats"</u>
●全体の解説
これまで自分がPlacementしてきた候補者のデータを集計
![Placements](https://github.com/TS-0910/Tableau/blob/main/Placements/Placements%20Stats_26.1.2021.png)

●個々の考察
・Sourced By
![Sourced By](https://github.com/TS-0910/Tableau/blob/main/Placements/Sourced%20By.png)
自分かチームメンバーがソースした候補者が約87%を占める

・Background
![Background](https://github.com/TS-0910/Tableau/blob/main/Placements/Background.png)
Internal IT出身の候補者が過半数を占め、その後Vendor、Consultantと続く

・Nationality
![Nationality](https://github.com/TS-0910/Tableau/blob/main/Placements/Nationality.png)
過半数は外国人候補者

・Billingual
![Billingual](https://github.com/TS-0910/Tableau/blob/main/Placements/Bilingual.png)
90%は日本語・英語のバイリンガル候補者

・Average age by background
![Average age by background](https://github.com/TS-0910/Tableau/blob/main/Placements/Average%20age%20by%20background.png)
Internal IT出身の方が年齢が高くても内定が出やすい。逆にVendor出身の場合は年齢が若めの人が好まれる。

・Average age by nationality
![Average age by nationality](https://github.com/TS-0910/Tableau/blob/main/Placements/Agerage%20age%20by%20nationality.png)
日本人の方が年齢が高くても内定が出やすい。逆に外国人の場合は年齢が若めの人が好まれる。

・Age and Salary
![Age and Salary](https://github.com/TS-0910/Tableau/blob/main/Placements/Age%20and%20Salary.png)
赤線は傾向線。個人差はあるものの年齢と年収はおおむね相関関係にある事が分かる。

●まとめ
・バイリンガルかつInternal IT出身の候補者を、自分もしくは自分のチームメンバーがソースする事がPlacementにつながりやすい。
・クライアント側は日本人候補者もしくはInternal IT出身の方が年齢に関してオープン

2."BI, IV, Offer"
●全体の解説
それぞれのポジション毎のBI,IV,Offerの関連性やClient毎の集計

●個々の考察
・IR and IV - Offer %
赤線は傾向線。
IRが多いほどIV - Offerの確率は下がる傾向にある。
これは、候補者が多いほど限られた採用枠へのOffer確率が下がるためと考えられる。
なので、一つのポジションに候補者を紹介し過ぎるのも良くないと言える。

・SL and SL - BI %
赤線は傾向線。
SLが増える程BIがもらえる率が下がる傾向にある。

SLが多いというのには下記のような理由が考えられる
・対象となる候補者が多い職種
・ポジションの要件が明確で無く曖昧
・長期間オープンになっている(中々いい候補者が見つからない/採用側のハードルが高くて採用まで至らない/採用枠が多い)

実際はこれらのコンビネーションである事もある(Ex. 要件が曖昧で、かつ採用側のハードルが高く長期間オープンになっている)。

では、SLの数と多いと良くないのだろうか？次のデータでそれを検証する。

・SL and Offer
SLが70 - 90くらいの場合最もOfferの数が多く、それ以降はSLが多くてもOfferが増えるとは言えない。
サンプル数が少ないため断定は出ないが、SLが90あたりを超えるようであれば、候補者をSLに集めた所でOfferは中々出ずあまり効率は良くない可能性がある。

・Client and Average BI
付き合いの深い代表5Client毎の平均BIの数を比較。左から順にBIの数が多く、候補者からの人気も高い企業と言える。

・Client and BI - IV %
BI(Clientへの紹介)の後にIVが入る確率を集計。左から順にIVが入りやすい企業。

IVが入りやすい理由として下記が挙げられる。
・企業側が積極的に採用をしている
・ポジションで求められている候補者を的確に紹介出来ている
・企業側があまり他に人材紹介を使っていない = エクスクルーシビティが高い
・Clientとの関係性が強く、信頼してもらえている(Ex. 「○○さんの紹介なら大丈夫だろう」)

・Client and IV - Offer %
(1st)IVの数に対してOfferが出る確率。左から順にOfferが出やすい企業と言える。

Offerが出やすい理由としては上記のClient and BI - IV %と同じ。

●まとめ
・IRが入り過ぎるのも良くない。その場合は他のポジションのソーシングにフォーカスしてもいい。
・SLが多すぎるのも良くない。多すぎるとかけた時間に対してのリターンが小さくなる可能性がある。
・Client Mは最も優良顧客。M2はその逆。
