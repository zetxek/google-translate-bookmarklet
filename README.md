# google-translate-bookmarklet
Add a bookmarklet to add the google translate bar to any site

code:
```
// create it in your browser by copying the rest of the script - and appending the "address" with "javascript: ", and then paste the code
try {
  console.log("starting, inserting script");
  languages = "en,es,da";
  o = document.createElement("scri" + "pt");
  o.setAttribute(
    "src",
    "https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"
  );
  o.setAttribute("type", "text/javascript");
  document.body.appendChild(o);
  v = document.body.insertBefore(
    document.createElement("div"),
    document.body.firstChild
  );
  v.id = "google_translate_element";
  p = document.createElement("scri" + "pt");
  p.text =
    "function googleTranslateElementInit() { new google.translate.TranslateElement({ pageLanguage: 'auto', includedLanguages: '"+languages+"', autoDisplay: true, layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');}";
  p.setAttribute("type", "text/javascript");
  document.body.appendChild(p);
  console.log("script inserted");
} catch (e) {
  console.log(e);
}
```
