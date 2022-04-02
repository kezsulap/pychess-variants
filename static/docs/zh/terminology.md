# 介紹

在整個網站和規則說明中，使用了許多不同的術語。其中有些術語適用於所有象棋變體，有些只適用於其中幾種（例如byo-yomi），有些可能根據變體具有不同的含義（例如僵局）。

作為總敘，此篇文章將介紹所有的你會在Pychess上看的的棋類術語。


# 「國際象棋變體」

首先最重要是「**國際象棋變體**」是什麼?

像四狂象棋和雙狂象棋都是真正的國際象棋的變種，因為它們只是改變國際象棋的規則。然而，中國象棋、日本將棋、韓國將棋和泰國象棋都是各地的傳統棋類，為何也被稱為「國際象棋變體」?

通常在西方，「國際象棋變體」是指所有源自古印度怡圖蘭卡 Chatturanga 的回合制策略遊戲。每個棋子具有不同的走法，且目標皆是“將死”對手的王。儘管東方的棋種並非源自國際象棋，卻都來自於古印度。

最大的國際象棋變體庫 chessvariants.com 有一整篇文章專門討論 [“什麼是國際象棋變體？”](https://www.chessvariants.com/what.html)

# 仙靈棋子

「仙靈」一詞在英文中表示「發明」，「仙靈棋子」指的是那些傳統西洋棋中沒有的棋子。但是，這個術語並不用於流傳已久的棋種，像中國象棋的「炮」就不算是「仙靈棋子」。然而，當「炮」出現在新的變體中（例如Shako），就會被視為是「仙靈棋子」。


## 棋子分類

仙靈棋子可以簡單的分為五種：

* **長距離型**: 可無限地沿一個方向移動，直到被另一個棋子擋住或碰到棋盤邊緣，例如中國象棋中的車。

* **跳躍型**: 棋子具有一定走法且無法阻礙其到達目的地。國際象棋中的騎士就是一個典型的例子。中國象棋和韓國將棋中的馬因為有「拐馬腳」的規則，便不算是跳躍型。

* **類炮型**: 必須先跳過另一子才能移動或吃子的棋子。例如中國象棋中的炮（先跳過另一棋子才能吃子）以及韓國將棋的「炮」（移動和吃子皆需跳過另一棋子）。

* **複合型**: 結合其他兩種棋子走法的棋子，例如西洋棋中的后即是城堡和主教的結合。

* **分化型**: 攻擊與移動走法不同的棋子，例如西洋棋中的兵向前移動但向斜前方攻擊。分化型在可汗象棋、帝國象棋和跳跳西洋棋中尤為突出。

# 時間限制

**時間限制**限定雙方棋手的走棋時間。通常棋局都會設定在10~60分鐘，雙方玩家各自有計時器，分別計時。

計時器主要分為三種：

1. **加時制(Fischer)** - 每當棋手動子時，他都會獲得額外的加時。例如在Pychess中，標記為“10+15”的棋局帶表開始時，雙方計時器上各有「10分鐘，每動一步加15秒」。大部分的棋局使用此制。

2. **Byo-yomi** - (秒読み，日語讀秒），一旦棋手的計時器時間到了之後，每步就只剩下一定的時間可以移動，通常用於日本將棋和國將棋。

byo-yomi還可以有外加。例如，如果有 3 段(period)外加，那玩家最多可以在耗完某一手的byo-yomi時，使用3段外加byo-yomi繼續讀秒(當然整場遊戲只有那3段，用完就沒了)。例如標記為“10+3x30(b)”的棋局帶表開始時，計時器各有「10 分鐘，byo-yomi 30秒，最多可以額外用3段」。這讓棋手可以在關鍵的一步，一段byo-yomi不夠用時，有更多的時間可以思考。

3. **驟死制** - 沒有額外的時間，計時器時間到即輸棋。

# 基本概念

**將軍** - 用一個棋子威脅國王，如果沒有應將，下一回合可以殺將。

**將死** - 幾乎所有象棋的遊戲目標，若國王無法逃脫將軍，則被將死輸棋。

**逼和** - 在有些棋種中(例如西洋棋)，當國王無處可逃時，視為平局，

**重複** - 當棋盤狀態重複時，通常至少重複 3 次，代表局面無法進一步變化。不同的變體對重複有不同的勝負判決。

**長將** - 類似於重複，但一名玩家不斷將軍並重複相同動作。長將的勝負判定在各種變體中也不同。

**行** - 棋盤上的縱向的線。

**列** - 棋盤上橫向的線。

**棋譜** - 對局中使用棋譜來代表棋子在棋盤上的位置，及每回合的動作。

**標準代數記法 (SAN)** - 國際象棋中使用的記法。每一步都使用棋子名稱（兵除外）來描述，然後是其目的地。附加字母用於消除歧義。

**回合** - 西洋棋中的回合是指雙方各動一步。然而在其他棋中(例如將棋)，一回合只代表一方動了一步。例如在國際象棋中，「三合何將死」是五步。但在將棋中則是三步。

**打入** - 將吃掉的棋子作為自己的棋子放到場上上。這是將棋和雙狂象棋的主要特色。Pychess中可打入的變體通帶有「狂」字。

**升變** - 棋子到達特定區域後升級為更強的棋子，因棋而異。在國際象棋中，只有兵可以在到達底線後升變。日本將棋中，幾乎所有棋子都可升變。

# 戰術

**捉雙** - 同時攻擊兩子。在所有變體中，馬最常用來捉雙。在有「打入」規則的變體中，車和主教、角行也能捉雙，尤其是主教。

![捉雙示例](https://github.com/gbtami/pychess-variants/blob/master/static/images/CVariantsGuide/Fork.png)

**牽制** - 攻擊一個不能移動的棋子，否則它會暴露它後面更高價值的棋子（通常是國王）。

![牽制示例](https://github.com/gbtami/pychess-variants/blob/master/static/images/CVariantsGuide/Pin.png)

**串打** - 類似於牽制，但受攻擊的兩子並排在一條直線上。受攻擊的一方只能選擇一子逃離。

![串打示例](https://github.com/gbtami/pychess-variants/blob/master/static/images/CVariantsGuide/Skewer.png)

**閃擊** - 閃開一子使其後原本被阻擋的棋子可以發動攻擊，同時閃開的棋子又可以攻擊到另一棋子，稱為「閃擊」。閃擊在西洋棋中尤為長見。

![閃擊](https://github.com/gbtami/pychess-variants/blob/master/static/images/CVariantsGuide/Discovery.png)

在此情況下，移動騎士讓城堡攻擊國王，同時騎士也威脅到黑后。由於黑方必須移動王，因此白方可以吃掉皇后。

**犧牲** - 為了得到更好的盤勢而做出犧牲。

![犧牲示例](https://github.com/gbtami/pychess-variants/blob/master/static/images/CVariantsGuide/Sacrifice.png)

在這個例子中，如果白方后吃了黑方的馬，它也會被兵吃掉。但這就讓騎士可以跳進去將死國王（紅色箭頭）。

<iframe width="560" height="315" src="https://www.youtube.com/embed/e4jYQ0UMmGk" frameborder="0" allowfullscreen></iframe>