# Livrables

Ce dossier contient tout ce que Jarvis (Claude) produit pour Mohamed.

---

## Regle d'or

| Sens | Dossier |
|------|---------|
| **Inputs** — documents que tu fournis a Claude (PDFs, exports, notes, briefs) | `context/import/` |
| **Outputs** — tout ce que Claude produit pour toi | `livrables/` |

Ne jamais melanger les deux. Si tu apportes un document a analyser, il va dans `context/import/`. Si Claude te livre quelque chose, ca va dans le bon sous-dossier ici.

---

## Organisation des sous-dossiers

| Dossier | Contenu |
|---------|---------|
| `sites-web/` | Sites internet, landing pages, maquettes, copies web |
| `applications/` | Outils, scripts, automatisations, prototypes |
| `youtube/` | Briefs videos, scripts, hooks, calendriers editoriaux |
| `cabinet/` | Livrables pour le cabinet de conseil Chatflow |
| `ecole/` | Livrables pour IApreneur Academie |

---

## Convention de nommage

Format : `AAAA-MM-JJ_nom-du-projet_type-livrable`

Exemples :
- `2026-06-26_medkit_landing-page-copy.md`
- `2026-07-01_chatflow_proposition-commerciale.pdf`
- `2026-07-15_youtube_script-ep12-prompting.md`
- `2026-08-01_iapreneur_module-3-contenu.md`

Regles :
- Toujours commencer par la date au format ISO (AAAA-MM-JJ)
- Nom du projet en minuscules avec des tirets
- Type de livrable a la fin, aussi en minuscules
- Pas d'espaces, pas d'accents, pas de caracteres speciaux

---

## Comment travailler

1. Tu fournis un brief ou un document dans `context/import/`
2. Claude produit le livrable et le depose dans le bon sous-dossier ici
3. Tu retrouves tous tes livrables ici, organises par theme et dates
