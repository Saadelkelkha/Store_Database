# Store_Database
This is a MySQL database named entreprise with tables clients, produits, and commandes. The commandes table has a foreign key id_client that references clients, a check constraint on statut, and a default value for statut.

# More Details :

- `clients` table: Stores client information. Each client has a unique `id_client`, `nom` (name), `prenom` (surname), `email`, `adresse` (address), and `telephone`.

- `produits` table: Contains product details. Each product has a unique `id_produit`, `nom_produit` (product name), `description`, `prix` (price), and `stock`.

- `commandes` table: Records orders. Each order has a unique `id_commande`, `id_client` (link to the client who made the order), `date_commande` (order date), `statut` (status of the order), and `total` (total price).

The `commandes` table is linked to the `clients` table via the `id_client` foreign key. This means each order is associated with a client in the `clients` table. The `statut` field in the `commandes` table has a check constraint to ensure its value is either 'en cours', 'livree', or 'annulee', and its default value is 'en cours'. This database design allows efficient management of clients, products, and orders. 😊
