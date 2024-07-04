# Monitoring des Services Web avec Prometheus, Grafana, Alertmanager et Slack

Ce dépôt contient une configuration pour surveiller et gérer les alertes des services web à l'aide de Prometheus, Grafana, Alertmanager et Slack.

## Fonctionnalités

- **Prometheus** : Collecte et stocke les métriques des services web.
- **Grafana** : Interface de visualisation pour les métriques collectées.
- **Alertmanager** : Gère et envoie des notifications d'alertes à Slack.
- **Blackbox Exporter** : Sonde les endpoints HTTP des services web pour les vérifications.
- **Node Exporter** : Collecte les métriques système des hôtes.

## Utilisation

1. **Démarrage rapide** : Utilisez Docker Compose pour démarrer tous les services.
2. **Accès aux services** :
    - Accédez à Prometheus pour surveiller les métriques : `http://localhost:9090`
    - Utilisez Grafana pour visualiser les tableaux de bord : `http://localhost:3000`
    - Gérez les alertes avec Alertmanager : `http://localhost:9093`
3. **Notifications** : Recevez des notifications dans Slack pour les alertes détectées.

## Recommandation

Utilisez le dashboard Grafana avec l'ID **13659** pour surveiller les probes HTTP du Blackbox Exporter : [Dashboard Grafana 13659](https://grafana.com/grafana/dashboards/13659-blackbox-exporter-http-prober/).

## Contribuer

Les contributions sont les bienvenues ! Soumettez une pull request pour toute amélioration ou correction.