### APIs HTTP públicas para integração com dados do Free Fire

> Documentação dos endpoints HTTP públicos para Free Fire, criada para facilitar a integração com aplicações, bots e sistemas próprios. Consulte endpoints, parâmetros, exemplos de requisições, respostas em JSON e mensagens retornadas pela API.
---

## Regiões suportadas

Atualmente, as APIs possuem suporte para **16 regiões** do Free Fire:

- `BR • SAC • US • NA • IND • BD • ID • ME • VN • TH • CIS • RU • PK • SG • EU • TW`
---

## 1. Info do jogador

Consulta informações públicas de uma conta do Free Fire através do UID e da região.

```http
GET https://freefireapis.lat/info-player?uid=228159683&region=BR
```

### Parâmetros

| Parâmetro | Tipo | Obrigatório | Descrição |
| --- | --- | --- | --- |
| `uid` | `string` | Sim | UID da conta do jogador |
| `region` | `string` | Sim | Região da conta |

### Resposta de sucesso

```json
{
  "success": true,
  "result": {
    "basicInfo": {
      "accountId": "1986238923",
      "accountType": 1,
      "nickname": "Mαnynhα ",
      "primeLevel": 6,
      "region": "BR",
      "language": "LANGUAGEEN",
      "level": 72,
      "exp": "3.648.738",
      "bannerId": 901026021,
      "headPic": 902000290,
      "rank": "Diamante I",
      "rankingPoints": "2.850",
      "badgeCnt": "34",
      "badgeId": 1001000100,
      "seasonId": 53,
      "liked": "41.968",
      "showRank": true,
      "lastLoginAt": "15/09/2026 às 20:02:48",
      "csRank": "Mestre",
      "csRankingPoints": "88",
      "maxRank": "Diamante I",
      "csMaxRank": "Mestre",
      "createAt": "07/05/2020 às 07:14:08",
      "title": 904090014,
      "releaseVersion": "OB54",
      "showBrRank": true,
      "showCsRank": true,
      "hippoRank": 15,
      "hippoRankingPoints": "19",
      "brPointsToNextRank": 50,
      "csPointsToNextRank": 3712,
      "brPointsRate": "77.8",
      "csPointsRate": "0.0",
      "xpInfo": {
        "levelText": "Conta level 72",
        "currentInLevel": "276.454",
        "totalInLevel": "327.171",
        "toNextLevel": "50.717",
        "rate": "84.5"
      }
    },
    "petInfo": {
      "id": 1300000051,
      "name": "JUBILEU",
      "level": 7,
      "exp": "6.013",
      "isSelected": true,
      "skinId": 1310000054,
      "selectedSkillId": 1315000010
    },
    "socialInfo": {
      "accountId": "1986238923",
      "language": "LANGUAGEARABIC",
      "timeOnline": "TIMEONLINEWEEKEND",
      "timeActive": "TIMEACTIVENIGHT",
      "signature": "Irmão da Lua, amigo das Estrelas  ♫\nModão é claroo",
      "rankShow": "RANKSHOWCS"
    },
    "creditScoreInfo": {
      "creditScore": 100,
      "rewardState": "REWARDSTATEUNCLAIMED",
      "periodicSummaryEndTime": "15/09/2026 às 20:02:50",
      "periodicSummaryLevel": 1789772570
    }
  }
}
```

---

## 2. Info Guest

Consulta informações de uma conta Guest através do UID e da senha, incluindo informações de banimento e carteira.

```http
GET https://freefireapis.lat/info-guest?uid=UID_GUEST&password=PASSWORD_GUEST
```

### Parâmetros

| Parâmetro | Tipo | Obrigatório | Descrição |
| --- | --- | --- | --- |
| `uid` | `string` | Sim | UID da conta Guest |
| `password` | `string` | Sim | Senha da conta Guest |

### Resposta de sucesso

```json
{
  "success": true,
  "result": {
    "accountInfo": {
      "accountId": "14499598574",
      "accountName": "M4S-GVDJYbPG",
      "region": "BR",
      "level": 20,
      "exp": "20.968"
    },
    "rankInfo": {
      "brRank": "Bronze I",
      "csRank": "Bronze I"
    },
    "activityInfo": {
      "createAt": "21/01/2026 às 16:14:29",
      "lastLoginAt": "16/09/2026 às 02:27:06",
      "server": "154.223.134.35 : 39698"
    },
    "walletInfo": {
      "coins": "21.916",
      "gems": "50",
      "gopGems": "0",
      "totalTopup": "0",
      "lastTopupTime": "0"
    }
  }
}
```
