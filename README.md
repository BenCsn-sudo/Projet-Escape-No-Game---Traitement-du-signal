# ==============================================
#  Projet : Chaîne de Transmission Numérique
#  Auteur : [Ton Nom]
#  Description :
#    Ce projet simule le fonctionnement complet
#    d'une chaîne de communication numérique :
#      - Écriture d’un message texte
#      - Conversion en binaire (ASCII)
#      - Codage Manchester
#      - Modulation FSK (Frequency Shift Keying)
#      - Démodulation, décodage et restitution
#
#  Objectif :
#    Illustrer le traitement du signal numérique
#    à travers un notebook Python interactif.
# ==============================================

# Nom du notebook
NOTEBOOK = livrable.ipynb

# Nom du rapport exporté
OUTPUT = rapport.html

# Commande pour exécuter le notebook
run:
	jupyter nbconvert --to notebook --execute $(NOTEBOOK) --output $(NOTEBOOK)

# Commande pour générer une version HTML lisible
export:
	jupyter nbconvert --to html $(NOTEBOOK) --output $(OUTPUT)

# Nettoyage des fichiers générés
clean:
	rm -f $(OUTPUT)
	rm -rf __pycache__

# Commande d’aide
help:
	@echo "Commandes disponibles :"
	@echo "  make run     -> Exécute le notebook"
	@echo "  make export  -> Génère une version HTML du rapport"
	@echo "  make clean   -> Supprime les fichiers générés"
