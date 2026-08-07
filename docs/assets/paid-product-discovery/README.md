# Paid product discovery — 候选库与落地附件

配套主文档：`docs/beyond-toolify-paid-product-discovery-2026-08-07.md`

## 文件

| 文件 | 用途 |
|------|------|
| `candidates-template.csv` | 候选库表头 + **种子样本**（可直接导入 Sheet/Notion） |
| `quick-check-15min.md` | 单品 15 分钟快核勾选 |
| `SEED-RUN-2026-08-07.md` | 首轮四源试跑记录与局限 |

## 字段说明（与主文档附录 A 对齐）

- `evidence_level`: S / A / B / C  
- `source_method`: stripe_story | latka_sacra | appsumo_ltd | product_hunt | g2_capterra | traffic | builtwith | app_store | funding | indie_mrr_post | mrr_roundup | ai_directory | other  
- `decision`: track | competitor_card | watch | kill  
- 主键优先用 `domain`；未知域名先填 name，核验后补 domain  

## 导入 Notion / Google Sheet

1. 新建 Database / Sheet  
2. 导入 CSV（UTF-8）  
3. 给 `evidence_level`、`decision` 做成 Select  
4. 视图建议：  
   - **A+ only**（evidence in S,A）  
   - **本周新增**（updated_at）  
   - **待杀死复查**（decision=watch）  
   - **按 cluster**  

## 使用纪律

- 每周至少杀死 5 条并写 `kill_reason`  
- C 级不得进入竞品深写，只能当线索  
- 任何第三方 MRR 数字默认 **B**，结账/多源交叉后才升 **A/S**  

*来自hueshadow*
