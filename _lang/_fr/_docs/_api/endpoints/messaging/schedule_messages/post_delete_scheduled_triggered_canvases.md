---
nav_title: "POST: Supprimer les Canevas programmées déclenchées par l'API"
article_title: "POST: Supprimer les Canevas programmées déclenchées par l'API"
search_tag: Endpoint
page_order: 4
layout: api_page
page_type: Référence
description: "Cet article décrit les détails sur le point de terminaison de Suppression programmée des Canvases Déclenchées par l’API."
---

{% api %}
# Supprimer les toiles programmées déclenchées par l'API
{% apimethod post core_endpoint|https://www.braze.com/docs/core_endpoints %}
/fr/canvas/trigger/schedule/delete
{% endapimethod %}

Le point de terminaison de l'horaire de suppression vous permet d'annuler un message que vous avez préalablement programmé les Canvases déclenchées par l'API avant qu'il n'ait été envoyé.

{% apiref postman %}https://documenter.getpostman.com/view/4689407/SVYrsdsG?version=latest#7d34037f-4bf2-4fab-bc9c-c972988051a7 {% endapiref %}

## Corps de la requête

Les messages planifiés ou les déclencheurs qui sont supprimés très près ou pendant la période où ils étaient censés être envoyés seront mis à jour avec le maximum d'efforts, de sorte que les suppressions de dernière seconde puissent être appliquées à tous, à certains ou à aucun de vos utilisateurs ciblés.

```
Type de contenu : application/json
Autorisation : Bearer YOUR-REST-API-KEY
```

```json
{
  "canvas_id": (requis, chaîne) l'identifiant Canvas
  "schedule_id": (requis, chaîne) le `schedule_id` à supprimer (obtenu à partir de la réponse pour créer un planning)
}
```

## Paramètres de la requête

| Paramètre        | Requis | Type de données      | Libellé                                                                  |
| ---------------- | ------ | -------------------- | ------------------------------------------------------------------------ |
| `id_toile`       | Requis | Chaîne de caractères | Voir l'identifiant [Canvas]({{site.baseurl}}/api/identifier_types/).     |
| `Id du planning` | Requis | Chaîne de caractères | Le `schedule_id` à supprimer (obtenu de la réponse à créer un planning). |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}


## Exemple de demande
```
curl --location --request POST 'https://rest.iad-01.braze. om/canvas/trigger/schedule/delete' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-REST-API-KEY' \
--data-raw '{
  "canvas_id": "canvas_identifier",
  "schedule_id": "schedule_identifier"
}
'
```

{% endapi %}