Le code de la méthode main utilise principalement le Builder Pattern pour créer les réservations d'hôtel. Une fois les réservations construites, il applique différentes stratégies de tarification en utilisant le Strategy Pattern. Le Abstract Factory Pattern est utilisé en coulisse pour créer différents types de chambres.

Voici comment chaque design pattern est utilisé dans le projet :

Builder Pattern
Le Builder Pattern est utilisé pour construire des objets de réservation d'hôtel complexes, permettant de définir étape par étape les différents attributs d'une réservation (type de chambre, services inclus, etc.).

Classes impliquées :

ReservationBuilder (abstract)
ReservationLuxeBuilder (concrete)
ReservationEconomiqueBuilder (concrete)
ReservationDirector
Strategy Pattern
Le Strategy Pattern permet de changer dynamiquement la stratégie de tarification appliquée à une réservation sans modifier la classe HotelReservation.

Classes impliquées :

StrategieTarification (interface)
TarificationSaisonniere (concrete)
TarificationOffreSpeciale (concrete)
Abstract Factory Pattern
Le Abstract Factory Pattern est utilisé pour créer des familles d'objets (dans ce cas, différents types de chambres) sans spécifier leurs classes concrètes.

Classes impliquées :

Chambre (abstract)
Suite (concrete)
ChambreStandard (concrete)
ChambreFactory (interface)
SuiteFactory (concrete)
ChambreStandardFactory (concrete)
