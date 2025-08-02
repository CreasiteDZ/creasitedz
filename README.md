<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Commande de site web - CreasiteDZ</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #ffffff;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #0D1B2A;
            color: white;
            text-align: center;
            padding: 20px 10px;
        }
        header h1 {
            font-size: 2.2em;
            font-family: 'Trebuchet MS', sans-serif;
        }
        .description {
            background-color: #0D1B2A;
            color: white;
            padding: 20px;
            margin: 20px;
            border-radius: 10px;
        }
        .description h2 {
            margin-top: 0;
        }
        form {
            max-width: 800px;
            margin: 0 auto;
            background-color: #f9f9f9;
            padding: 20px;
            border-radius: 10px;
        }
        label {
            display: block;
            margin: 15px 0 5px;
            background-color: #F5F5DC;
            padding: 10px;
            border-radius: 5px;
        }
        input[type="text"],
        input[type="email"],
        input[type="tel"],
        textarea,
        select {
            width: 100%;
            padding: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .question-oui-non {
            margin-bottom: 10px;
        }
        .remarque {
            margin: 30px 0;
            background-color: #eee;
            padding: 15px;
            border-left: 5px solid #0D1B2A;
        }
        footer {
            background-color: #0D1B2A;
            color: white;
            text-align: center;
            padding: 15px 10px;
            margin-top: 40px;
        }
        img {
            max-width: 100%;
            height: auto;
            margin-bottom: 20px;
            border-radius: 8px;
        }
    </style>
</head>
<body>

<header>
    <h1>CreasiteDZ</h1>
</header>

<div class="description">
    <h2>Bienvenue chez CreasiteDZ</h2>
    <p>Nous créons des sites web vitrines et e-commerce pour les petites boutiques et entreprises en Algérie. Veuillez remplir ce formulaire pour passer votre commande.</p>
</div>

<form>
    <label>1. Nom complet :</label>
    <input type="text" name="nom">

    <label>2. Adresse e-mail :</label>
    <input type="email" name="email">

    <label>3. Numéro de téléphone :</label>
    <input type="tel" name="telephone">

    <label>4. Nom de votre boutique ou entreprise :</label>
    <input type="text" name="nom_boutique">

    <label>5. Adresse de votre boutique ou zone d'activité :</label>
    <input type="text" name="adresse_boutique">

    <label>6. Type de site web souhaité :</label>
    <select name="type_site">
        <option value="vitrine">Site vitrine</option>
        <option value="ecommerce">Site e-commerce</option>
        <option value="autre">Autre (précisez ci-dessous)</option>
    </select>
    <textarea placeholder="Autres besoins..." name="precisions_type"></textarea>

    <label>7. Souhaitez-vous intégrer des moyens de paiement ?</label>
    <div class="question-oui-non">
        <input type="radio" name="paiement" value="oui"> Oui
        <input type="radio" name="paiement" value="non"> Non
    </div>
    <textarea placeholder="Si oui, précisez les moyens souhaités..." name="details_paiement"></textarea>

    <label>8. Avez-vous un logo ?</label>
    <div class="question-oui-non">
        <input type="radio" name="logo" value="oui"> Oui
        <input type="radio" name="logo" value="non"> Non
    </div>
    <textarea placeholder="Vous pouvez ajouter un lien ou description..." name="logo_details"></textarea>

    <label>9. Avez-vous un nom de domaine ?</label>
    <div class="question-oui-non">
        <input type="radio" name="domaine" value="oui"> Oui
        <input type="radio" name="domaine" value="non"> Non
    </div>
    <textarea placeholder="Si oui, indiquez-le ici..." name="domaine_details"></textarea>

    <label>10. Langues souhaitées pour votre site :</label>
    <select multiple name="langues">
        <option value="fr">Français</option>
        <option value="ar">Arabe</option>
        <option value="en">Anglais</option>
        <option value="autre">Autres (précisez ci-dessous)</option>
    </select>
    <textarea placeholder="Autres langues ou remarques..." name="langues_details"></textarea>

    <label>11. Couleurs préférées pour le site :</label>
    <input type="text" name="couleurs" placeholder="Exemple : bleu foncé, blanc, beige chaud">

    <label>12. Souhaitez-vous que nous intégrions des images fournies par vous ?</label>
    <div class="question-oui-non">
        <input type="radio" name="images" value="oui"> Oui
        <input type="radio" name="images" value="non"> Non
    </div>
    <textarea placeholder="Ajoutez les liens ou noms de fichiers si disponible..." name="details_images"></textarea>

    <label>13. Liens de vos réseaux sociaux (facultatif) :</label>
    <textarea name="reseaux" placeholder="Exemple : Facebook: facebook.com/votrepage, Instagram: instagram.com/votreprofil..."></textarea>

    <div class="remarque">
        ⚠️ Une fois votre commande envoyée, elle sera **confirmée par e-mail** par notre équipe à l'adresse que vous avez fournie.
    </div>
</form>

<footer>
    <p>Contact : creasitedz@example.com | Facebook : facebook.com/creasitedz | Instagram : @creasitedz | Tél : +213 123 456 789</p>
</footer>

</body>
</html>
