<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CreasiteDZ</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
    }
    header {
      background-color: #002244;
      color: white;
      padding: 20px;
      text-align: center;
    }
    header h1 {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      font-size: 36px;
      margin: 0;
    }
    .description {
      border: 2px solid #002244;
      padding: 20px;
      margin: 20px;
      background-color: white;
    }
    form {
      background-color: white;
      padding: 20px;
      margin: 20px;
    }
    label {
      display: block;
      margin: 10px 0 5px;
      background-color: #f5f0e6;
      padding: 5px;
    }
    input, textarea, select {
      width: 100%;
      padding: 8px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .footer {
      background-color: #002244;
      color: white;
      text-align: center;
      padding: 10px;
      margin-top: 20px;
    }
    .remarque {
      margin: 20px;
      padding: 10px;
      background-color: #e0f7fa;
      border-left: 4px solid #00796b;
      font-style: italic;
    }
    .gallery {
      display: flex;
      justify-content: space-around;
      padding: 20px;
      background-color: #fff;
    }
    .gallery img {
      width: 30%;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
  </style>
</head>
<body>
  <header>
    <h1>CreasiteDZ</h1>
  </header>
  <div class="gallery">
    <img src="/mnt/data/web-design-3411373_1280.webp" alt="Web Design" />
    <img src="/mnt/data/code-1076536_1280.jpg" alt="Code HTML" />
    <img src="/mnt/data/https-3344700_1280.webp" alt="HTTPS Secure" />
  </div>
  <div class="description">
    <p>Bienvenue sur CreasiteDZ ! Nous créons des sites web simples, professionnels et adaptés aux petites boutiques et projets e-commerce. Remplissez ce formulaire pour commander votre site. Vous recevrez une confirmation par email.</p>
  </div>
  <form id="commandeForm">
    <label>1 - Nom et prénom :</label>
    <input type="text" name="nom_projet" required />
    <label>2 - Description du projet :</label>
    <textarea name="description_projet"></textarea>
    <label>3 - Avez-vous un logo ?</label>
    <select name="avez_logo">
      <option>Oui</option>
      <option>Non</option>
    </select>
    <label>Si Oui, ajoutez le logo :</label>
    <input type="file" name="logo_file" />
    <label>4 - Couleurs préférées :</label>
    <input type="text" name="couleurs_pref" value="bleu foncé, blanc, beige chaud" />
    <label>5 - Email professionnel à afficher (facultatif) :</label>
    <input type="email" name="email_pro" required />
    <label>6 - Type de site souhaité :</label>
    <select name="type_site">
      <option>Site vitrine</option>
      <option>Site e-commerce simple</option>
    </select>
    <label>Autre besoin (précisez) :</label>
    <input type="text" name="autre_type_site" />
    <label>7 - Design souhaité :</label>
    <input type="text" name="design_pref" placeholder="simple et élégant..." />
    <label>8 - Nom de domaine déjà existant ?</label>
    <select name="domaine_exist">
      <option>Oui</option>
      <option>Non</option>
    </select>
    <label>Si Oui, précisez :</label>
    <input type="text" name="domaine_info" />
    <label>9 - Hébergement déjà disponible ?</label>
    <select name="hebergement">
      <option>Oui</option>
      <option>Non</option>
    </select>
    <label>Si Oui, précisez :</label>
    <input type="text" name="hebergement_info" />
    <label>10 - Langues à inclure sur le site :</label>
    <select multiple name="langues">
      <option>Français</option>
      <option>Anglais</option>
      <option>Arabe</option>
    </select>
    <label>Autres langues (précisez) :</label>
    <input type="text" name="autres_langues" />
    <label>11 - Réseaux sociaux à afficher (facultatif) :</label>
    <input type="text" name="social_facebook" placeholder="Lien Facebook" />
    <input type="text" name="social_instagram" placeholder="Lien Instagram" />
    <input type="text" name="social_autre" placeholder="Autres liens" />
    <label>12 - Informations supplémentaires :</label>
    <textarea name="infos_sup"></textarea>
    <label>13 - Souhaitez-vous une version mobile optimisée ?</label>
    <select name="version_mobile">
      <option>Oui</option>
      <option>Non</option>
    </select>
    <input type="submit" value="Envoyer la commande" />
  </form>
  <div class="remarque">
    Remarque : Vous serez contacté par email pour confirmer votre commande. Merci pour votre confiance !
  </div>
  <div class="footer">
    <p>Email : creasitedz@gmail.com | Facebook : CreasiteDZ | Instagram : CreasiteDZ</p>
    <p>Téléphone : +213 6 00 00 00 00</p>
  </div>
<script>
document.getElementById("commandeForm").addEventListener("submit", function(e) {
  e.preventDefault();
  const formData = new FormData(this);
  const jsonData = {};
  formData.forEach((value, key) => {
    if (jsonData[key]) {
      if (!Array.isArray(jsonData[key])) {
        jsonData[key] = [jsonData[key]];
      }
      jsonData[key].push(value);
    } else {
      jsonData[key] = value;
    }
  });
  fetch("https://script.google.com/macros/s/AKfycbyugYkQAhF1v1r4mnNiFJGjDKImSI1yLxVgCO96CcFdLIb_05fsROVb1N2IRl-ljjyR/exec", {
    method: "POST",
    mode: "no-cors",
    body: JSON.stringify(jsonData)
  })
  .then(() => {
    alert("✅ Commande envoyée avec succès ! Vous recevrez un email de confirmation.");
    document.getElementById("commandeForm").reset();
  })
  .catch(error => {
    alert("❌ Erreur lors de l'envoi : " + error.message);
  });
});
</script>
</body>
</html>
