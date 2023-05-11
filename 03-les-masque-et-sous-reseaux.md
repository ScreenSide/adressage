# III. Les masques de sous-réseau

## A. Définition des masques de sous-réseau

- Un masque de sous-réseau est une combinaison de bits utilisée pour diviser un réseau en sous-réseaux plus petits.
- Les masques de sous-réseau permettent d'augmenter l'efficacité et la sécurité des réseaux.

## B. Utilisation des masques de sous-réseau pour diviser un réseau en sous-réseaux

- Pour diviser un réseau en sous-réseaux, un masque de sous-réseau est appliqué à l'adresse IP du réseau.
- Les bits correspondant au masque de sous-réseau indiquent quelle partie de l'adresse IP est réservée pour l'identification du sous-réseau et quelle partie est réservée pour l'identification de l'hôte.

## C. Calcul du nombre de sous-réseaux et d'hôtes dans un réseau donné

- Le nombre de sous-réseaux et d'hôtes disponibles dans un réseau dépend du nombre de bits alloués pour l'identification du sous-réseau et du nombre de bits alloués pour l'identification de l'hôte.
- Le nombre de sous-réseaux et d'hôtes peut être calculé en utilisant des formules mathématiques spécifiques.

## D. Exemples de calculs de réseaux (adresse de réseau, adresse de diffusion, plage d'adresses valides)

- En utilisant un masque de sous-réseau, il est possible de déterminer l'adresse de réseau, l'adresse de diffusion et la plage d'adresses valides pour chaque sous-réseau.
- Ces calculs sont importants pour configurer correctement les appareils connectés au réseau.

# Exercices

1. Calculez le nombre de sous-réseaux et d'hôtes disponibles pour l'adresse IP suivante : 192.168.0.0/24.

2. Divisez le réseau 172.16.0.0/16 en 8 sous-réseaux égaux. Quel est le masque de sous-réseau nécessaire pour cela ?

3. Un administrateur réseau souhaite diviser le réseau 10.0.0.0/8 en sous-réseaux pour trois départements différents. Le département A nécessite 50 sous-réseaux, le département B nécessite 100 sous-réseaux, et le département C nécessite 200 sous-réseaux. Calculez le masque de sous-réseau nécessaire pour cette configuration.

4. Calculez l'adresse de réseau, l'adresse de diffusion et la plage d'adresses valides pour un sous-réseau avec l'adresse IP 192.168.10.0/24.

5. Un réseau a été divisé en 6 sous-réseaux égaux avec le masque de sous-réseau 255.255.255.224. Quelles sont les adresses de réseau, les adresses de diffusion et les plages d'adresses valides pour chacun des sous-réseaux ?

## Solutions

1. Pour l'adresse IP 192.168.0.0/24, le masque de sous-réseau est 255.255.255.0. Cela signifie qu'il y a 8 bits réservés au masque de sous-réseau, ce qui permet de créer 2^8 (256) sous-réseaux et de 2^(32-24-8) (256) hôtes par sous-réseau. Ainsi, il y a 256 sous-réseaux disponibles et chacun d'eux peut accueillir jusqu'à 256 hôtes.

2. Pour diviser le réseau 172.16.0.0/16 en 8 sous-réseaux égaux, nous avons besoin de 3 bits supplémentaires pour les masques de sous-réseau (2^3=8). Ainsi, le masque de sous-réseau approprié est 255.255.248.0 (ou /21 en notation CIDR). Chaque sous-réseau contient 2^(32-21)-2 (2046) adresses.

3. Pour diviser le réseau 10.0.0.0/8 en sous-réseaux pour les départements A, B et C, nous avons besoin de calculer le nombre de bits nécessaires pour chaque département. Pour le département A, 50 sous-réseaux nécessitent 6 bits supplémentaires pour le masque de sous-réseau. Pour le département B, 100 sous-réseaux nécessitent 7 bits supplémentaires, et pour le département C, 200 sous-réseaux nécessitent 8 bits supplémentaires. Ainsi, le masque de sous-réseau approprié pour chaque département est le suivant :

- Département A : 255.255.252.0 (ou /22 en notation CIDR)
- Département B : 255.255.254.0 (ou /23 en notation CIDR)
- Département C : 255.255.255.128 (ou /25 en notation CIDR)

4. Pour l'adresse IP 192.168.10.0/24, le masque de sous-réseau est 255.255.255.0. La plage d'adresses valides pour le sous-réseau est donc de 192.168.10.1 à 192.168.10.254. L'adresse de réseau est 192.168.10.0 et l'adresse de diffusion est 192.168.10.255.

5. Le masque de sous-réseau 255.255.255.224 (ou /27 en notation CIDR) permet de diviser un réseau en 8 sous-réseaux égaux. Les adresses de réseau et de diffusion pour chaque sous-réseau sont les suivantes :

- Sous-réseau 1 : Adresse réseau = 192.168.10.0, Adresse diffusion = 192.168.10.31
- Sous-réseau 2 : Adresse réseau = 192.168.10.32, Adresse diffusion = 192.168.10.63
- Sous-réseau 3 : Adresse réseau = 192.168.10.64, Adresse diffusion = 192.168.10.95
- Sous-réseau 4 : Adresse réseau = 192.168.10.96, Adresse diffusion = 192.168.10.127
