# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


# Quel est le nombre total d'objets Album contenus dans la base (sans regarder les id bien sûr) ?
Album.count

# Qui est l'auteur de la chanson "White Room" ?
Track.find_by(title: "White Room").artist

# Quelle chanson dure exactement 188133 milliseconds ?
Track.find_by(duration: 188133).title

# Quel groupe a sorti l'album "Use Your Illusion II" ?
Album.find_by(title: "Use Your Illusion II").artist

# Combien y a t'il d'albums dont le titre contient "Great" ?
Album.where("title LIKE ?", "%Great%")

# Supprime tous les albums dont le nom contient "music".
Album.where("title LIKE ?", "%music%").destroy_all

# Combien y a t'il d'albums écrits par AC/DC ?
Album.where(artist: "AC/DC").count

# Combien de chanson durent exactement 158589 millisecondes ?
Track.where(duration: 158589).count
