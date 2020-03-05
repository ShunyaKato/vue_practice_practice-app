<template>
  <div class="house">
    <h1>家庭内</h1>
    <Checklist
      :checklists="checklists[index]"
      v-for="(checklist, index) in checklists"
      :key="index"
    />
  </div>
</template>

<script>
import Checklist from "../components/house/Checklist";

export default {
  name: "house",
  components: {
    Checklist
  },
  data() {
    return {
      checklists: [
        {
          item: "健康管理と早期発見",
          lists: [
            {
              item:
                "自分の健康状態を把握している（平常時の体温、血圧、脈拍、排泄回数、排泄物の性状、食事量等）",
              isChecked: false
            },
            {
              item: "体調が悪いときは、受診している",
              isChecked: false
            }
          ]
        },
        {
          title: "手洗い",
          lists: [
            {
              item:
                "帰宅後、調理前、配膳前、食事前、排泄後、排泄のお世話後には手洗いを実施している",
              isChecked: false
            },
            {
              item: "爪は短く切り、時計や指輪を外している",
              isChecked: false
            },
            {
              item: "石鹸を使い、流水で 15～30 秒以上こすり洗いをしている",
              isChecked: false
            },
            {
              item:
                "汚れが残りやすい、指先や爪の間、指の間、親指の周り、手首、手のしわも注意して洗っている",
              isChecked: false
            },
            {
              item:
                "手洗い後の手拭用タオルは共用せず、ペーパータオルや個人用タオルを利用している",
              isChecked: false
            },
            {
              item:
                "水道の蛇口は手と一緒に洗うか、ペーパータオルを利用して、蛇口を締めている",
              isChecked: false
            }
          ]
        },
        {
          title: "排泄に関する対策",
          lists: [
            {
              item: "使用前に便座を消毒している",
              isChecked: false
            },
            {
              item: "排便後お尻を拭いた後、何も触らずすぐに手を洗っている",
              isChecked: false
            },
            {
              item: "可能であれば、排便後の手洗いはトイレの中で行っている",
              isChecked: false
            },
            {
              item:
                "ポンプ式石鹸や水道の蛇口、トイレのドアノブ、水洗レバーはペーパータオルを使うなどして、手洗い前に直接触らないようにしている",
              isChecked: false
            },
            {
              item: "蛇口は清潔に保ち、必要に応じて消毒している",
              isChecked: false
            }
          ]
        },
        {
          title: "食事に関する対策",
          lists: [
            {
              item: "調理前の手洗いは洗面台でしている",
              isChecked: false
            },
            {
              item: "高齢者や乳幼児へは、貝類の生食を避けている",
              isChecked: false
            },
            {
              item: "加熱できるものは中までしっかり加熱している",
              isChecked: false
            },
            {
              item: "作った食事はできるだけ早く食べている",
              isChecked: false
            },
            {
              item:
                "食器、調理器具は熱湯又は消毒液で消毒後、水洗いして乾燥させている",
              isChecked: false
            },
            {
              item: "冷蔵庫の中を掃除している",
              isChecked: false
            }
          ]
        },
        {
          title: "入浴時の対策",
          lists: [
            {
              item: "浴槽に入る前に、お尻をよく洗っている",
              isChecked: false
            },
            {
              item: "風呂の水は毎日かえている",
              isChecked: false
            },
            {
              item: "タオルやバスタオルは共用していない",
              isChecked: false
            },
            {
              item: " 下痢をしている患者の入浴は一番最後にしている",
              isChecked: false
            }
          ]
        },
        {
          title: "掃除",
          lists: [
            {
              title: "トイレ",
              items: [
                {
                  item: "専用の手袋を用いている",
                  isChecked: false
                },
                {
                  item: "日ごろからこまめに掃除をしている",
                  isChecked: false
                },
                {
                  item:
                    "消毒する場合は、汚れをあらかじめ落としてから、消毒液を含ませた布等で拭いている（噴霧の場合、消毒液がすぐ乾燥しないように十分な量を噴霧し、拭き取っている）",
                  isChecked: false
                },
                {
                  item: " 清掃後、手袋を外した後も手洗いをしている",
                  isChecked: false
                }
              ]
            },
            {
              title: "お風呂",
              items: [
                {
                  item: "浴槽は流水と石鹸で十分洗い流している",
                  isChecked: false
                },
                {
                  item: "浴槽の他、風呂の床、洗面器、椅子なども掃除している",
                  isChecked: false
                }
              ]
            }
          ]
        },
        {
          title: "感染症予防のための環境整備",
          lists: [
            {
              item: "洗面所、トイレに石鹸を置いている",
              isChecked: false
            },
            {
              item:
                "階段の手すり、水道の蛇口等頻繁に触れる場所を定期的に清掃（消毒）している",
              isChecked: false
            },
            {
              item: "おう吐物等を処理するための物品を準備している",
              isChecked: false
            },
            {
              item: " 訪問者に手洗いを勧めている",
              isChecked: false
            }
          ]
        }
      ]
    };
  }
};
</script>