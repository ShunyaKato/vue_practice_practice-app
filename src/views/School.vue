<template>
  <div class="School">
    <h1>学校等</h1>
    <Checklist
      :checklists="checklists[index]"
      v-for="(checklist, index) in checklists"
      :key="index"
    />
  </div>
</template>

<script>
import Checklist from "../components/school/Checklist";

export default {
  name: "school",
  components: {
    Checklist
  },
  data() {
    return {
      checklists: [
        {
          title: "園児・児童・生徒の健康管理と早期発見",
          lists: [
            {
              item:
                "園児・児童・生徒が接種した予防接種について確認を行っている",
              isChecked: false
            },
            {
              item: "園児・児童・生徒の健康診断の結果を記録している",
              isChecked: false
            },
            {
              item: "園児・児童・生徒の毎日の健康観察を実施している",
              isChecked: false
            },
            {
              item:
                "園・学校全体の体調不良者・欠席者等の情報（人数や欠席理由等）が１日１回集約されている",
              isChecked: false
            },
            {
              item:
                "園児・児童・生徒の体調が悪い場合には、本人・保護者に受診を促している",
              isChecked: false
            }
          ]
        },
        {
          title: "教職員の健康管理と早期発見",
          lists: [
            {
              item:
                "教職員の健康診断を定期的に実施し、未受診者に受診を促している",
              isChecked: false
            },
            {
              item: "教職員の体調が悪い場合には、医療機関へ受診させている",
              isChecked: false
            },
            {
              item:
                "学校内に出入りするパート職員やボランティア等の健康状態を確認している",
              isChecked: false
            },
            {
              item:
                "実習生の予防接種歴・健康診断の結果を必要に応じて提出させている",
              isChecked: false
            },
            {
              item:
                "実習生の毎日の健康状態を確認している（発熱・咳・おう吐・下痢等の有無）",
              isChecked: false
            }
          ]
        },
        {
          title: "手洗いと標準予防策",
          lists: [
            {
              item: "園児・児童・生徒へ手洗いの指導を行っている",
              isChecked: false
            },
            {
              item: "手洗いは、石鹸と流水で、15秒～30秒以上行っている",
              isChecked: false
            },
            {
              item:
                "手拭きは使い捨てのペーパータオルか個人用のタオルを使用している(共用タオルは置いていない）",
              isChecked: false
            },
            {
              item: "来訪者に手洗いを勧めている",
              isChecked: false
            },
            {
              item:
                "使い捨て手袋を使用した場合、手袋をはずした後に手洗いをしている",
              isChecked: false
            },
            {
              item:
                "園児・児童・生徒・教職員に咳症状がある場合、周囲への飛散を防ぐためマスクの着用を促している",
              isChecked: false
            }
          ]
        },
        {
          title: "感染症予防のための環境整備",
          lists: [
            {
              item: "手洗い場・トイレに石鹸が整備されている",
              isChecked: false
            },
            {
              item:
                "階段の手すり・水道の蛇口等、園児・児童・生徒が頻繁に触れる場所を定期的に清掃（消毒）している",
              isChecked: false
            },
            {
              item:
                "感染症予防・発生時対応のための物品が準備されている（※使い捨て手袋・マスク・エプロン・拭き取りの布（ペーパータオル、新聞紙等）、塩素系消毒剤、ビニール袋、専用バケツなど）",
              isChecked: false
            }
          ]
        },
        {
          title: "研修",
          lists: [
            {
              item:
                "職員に対する感染症の研修を、年一回以上、学校内で実施（または施設外の研修へ派遣）している",
              isChecked: false
            },
            {
              item: "派遣研修の場合、研修の内容を職員会議等で共有している",
              isChecked: false
            },
            {
              item:
                "おう吐物処理の方法を教職員の間で確認している（特に冬季胃腸炎流行シーズン頃）",
              isChecked: false
            }
          ]
        }
      ]
    };
  }
};
</script>
