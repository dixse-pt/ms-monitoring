# Gestion des Alertes avec Prometheus, Alertmanager et Slack

Ce dépôt contient une configuration pour surveiller et gérer les alertes de services web à l'aide de Prometheus, Alertmanager et Slack. Les alertes sont déclenchées en fonction des réponses HTTP obtenues par le blackbox exporter.

## Configuration

### Prometheus

Prometheus est configuré pour scruter les endpoints des services web à intervalles réguliers et collecter des métriques comme le statut HTTP.

### Alertmanager

Alertmanager est utilisé pour agréger et gérer les alertes générées par Prometheus. Il envoie des notifications à Slack lorsque des alertes sont déclenchées et résolues.

### Slack

Les notifications Slack sont configurées pour être envoyées dans le canal `#services-web`. L'URL d'API Slack est géré en tant que variable d'environnement sécurisée pour éviter toute exposition de secrets dans ce dépôt public.

## Utilisation

Pour utiliser cette configuration localement :

1. **Prérequis** : Assurez-vous que Docker et Docker Compose sont installés sur votre machine.
2. **Configuration des variables d'environnement** :
    - Créez un fichier `.env` à la racine du projet avec les variables d'environnement nécessaires, y compris `SLACK_API_URL`.
3. **Démarrage** :
    - Lancez l'ensemble du système avec Docker Compose :
        
        ```
        Copier le code
        docker-compose up -d
        
        ```
        
4. **Surveillance** :
    - Accédez à Prometheus via `http://localhost:9090` pour surveiller les métriques collectées.
5. **Gestion des alertes** :
    - Accédez à Alertmanager via `http://localhost:9093` pour voir et gérer les alertes actives.
6. **Notifications** :
    - Recevez des notifications dans le canal Slack défini dans le fichier alertmanager.yml, ici "#services-web" lorsque des alertes sont déclenchées ou résolues.

## Contribuer

Les contributions sont les bienvenues ! Pour toute amélioration ou correction, veuillez soumettre une pull request et nous examinerons votre proposition.

---