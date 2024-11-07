Sélection des composants AWS pour le déploiement de notre application

Pour le déploiement de notre application, nous avons sélectionné les composants AWS suivants, qui garantissent une infrastructure fiable, sécurisée et facile à gérer. Ces choix visent à fournir une performance optimale tout en assurant une haute disponibilité et une scalabilité flexible en fonction de la demande.

Elastic Load Balancer (ELB)
Le Load Balancer répartit le trafic entre les services frontend et backend, assurant ainsi une haute disponibilité sur plusieurs zones de disponibilité. En cas de défaillance de l'un des services, l'ELB redirige le trafic vers des instances saines, garantissant ainsi la continuité de service et une expérience utilisateur sans interruption.
ECS Fargate (Elastic Container Service)
Avec ECS Fargate, nous pouvons déployer nos conteneurs Docker sans gérer l'infrastructure sous-jacente. Ce service serverless nous permet de nous concentrer sur le développement et la gestion de l’application, car les ressources sont allouées automatiquement en fonction des besoins. Cela offre une solution scalable et rentable, idéale pour une application générale.
Amazon S3 (Simple Storage Service)
Amazon S3 est notre choix pour stocker et gérer les fichiers statiques (comme les images, documents, et autres ressources). S3 est scalable et durable, offrant un accès rapide et fiable à partir de n'importe où, ce qui assure la bonne disponibilité des assets pour notre application.
Amazon CloudWatch
Nous utilisons CloudWatch pour surveiller les performances et les logs de notre application. Ce service permet de détecter les anomalies et de configurer des alertes en temps réel, nous offrant la possibilité de répondre rapidement aux incidents et d'assurer une expérience utilisateur optimale.
Amazon VPC (Virtual Private Cloud)
Un réseau privé sécurisé (VPC) est mis en place pour isoler les ressources de l'application et permettre une communication sécurisée entre elles. Le VPC garantit la sécurité des données et limite les accès externes, tout en autorisant une communication contrôlée entre les services.

Schéma de l'infrastructure AWS

![Schema de l'infrastructure](/schema.png)

Justification des choix techniques
Ces composants AWS ont été sélectionnés pour leur capacité à offrir une infrastructure performante, scalable et sécurisée. Le Load Balancer et ECS Fargate garantissent une haute disponibilité et une gestion serverless, ce qui simplifie l’administration et réduit les coûts. S3 assure un stockage fiable et accessible pour les fichiers statiques, tandis que CloudWatch fournit une surveillance continue et en temps réel. Enfin, VPC renforce la sécurité globale de l’application, protégeant les ressources critiques.

Bonus : Déploiement d’images Docker
Nous avons utilisé Amazon Elastic Container Registry (ECR) pour stocker nos images Docker et les rendre facilement disponibles pour ECS Fargate. ECR offre une gestion centralisée et sécurisée des conteneurs Docker, simplifiant ainsi notre processus de déploiement.