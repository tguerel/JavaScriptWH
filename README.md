# JavaScriptWH


# Primitive Datentypen
Mit primitiven Datentypen kann man Variablen erstellen, die **Zahlen**, einzelne **Zeichen** oder **logische Werte** aufnehmen.

Beispiele dafür sind:

**boolean**,

**string**

**int**
___

# Variablen
Variablen werden mit **let** oder **var** deklariert und sind ein Speicher oder Platzhalter für Daten wie Zahlen und Strings, deren Wert sich während der Ausführung des Scripts ändert. Javascript-Variablen haben einen Namen, einen Typ und einen Wert.
___
# Operatoren (artihmetisch, Vergleich, logisch)

Ein **arithmetischer Operator** nimmt numerische Werte (Literale oder Variablen) als Operanden entgegen und gibt einen einzelnen numerischen Wert zurück. Die arithmetischen Standardoperatoren sind Addition **(+)**, Subtraktion **(-)**, Multiplikation **(*)** und Division **(/)**.

**Vergleichsoperatoren** dienen zum Vergleichen zweier Werte. Solche Vergleiche werden vor allem für bedingte Anweisungen und Schleifen benutzt. Als Ergebnis liefern Vergleichsoperatoren immer einen sogenannten booleschen Wert (Wahrheitswert) vom Typ boolean, d.h. entweder true (wahr) oder false (falsch).

Mit den **logischen Operatoren** werden logische Verknüpfungen formuliert, z.B. für Abbruchbedingungen von Schleifen, bedingte Anweisungen bzw. Verzweigungen im Programmfluss. Beim Verknüpfen von booleschen Operanden (true/false) entsprechen die Ergebnisse denen der booleschen Algebra.JavaScript 1.0ChromeFirefoxIEOperaSafari
JavaScript ist bei den logischen Operatoren aber nicht nur auf die booleschen Werte false und true beschränkt. Statt dessen richten sie sich nach den Werte-Eigenschaften "truthy" und "falsy" (siehe Artikel zu Boolean) und behandeln truthy-Werte wie true und falsy-Werte wie false.

Mit dem logischen Operator **&&** verknüpfen Sie zwei oder mehrere Bedingungen durch "und", d.h. beide bzw. alle Bedingungen müssen erfüllt sein, damit die gesamte Bedingung erfüllt ist.

Mit dem logischen Operator **||** verknüpfen Sie zwei oder mehrere Bedingungen inklusiv durch "oder", d.h. es genügt, wenn eine der Bedingungen erfüllt ist, damit die gesamte Bedingung erfüllt ist.

Der logische Operator **!** (engl. not) prüft, ob ein Ausdruck unwahr ist. Der Ausdruck if (!name) trifft zu, wenn der Wert von name falsy ist, also ein Leerstring, null, undefiniert oder 0 ist.

___

# Kommentar
Kommentare können verwendet werden, um den Code zu erklären und leichter zu lesen.
Außerdem kann man damit alternativen Code testen, da auskommentierter Code nicht ausgeführt wird.

Einzeiliges Kommentar wird mit **"//"** gekennzeichnet. Alles in der Zeile wird nicht ausgeführt.

Mehrzeilige Kommentare werden mit **"/* ... */"** gekennzeichnet. 
Alles innerhalb der beiden Zeichen wird nicht ausgeführt.
___

# Ausgabe auf den Bildschirm
Zur Ausgabe auf den Bildschirm dienen alert, console und print. 
alert () ist die bekannteste Javascript-Methode zum Öffnen und Schließen von Fenstern – sie wird vor allem für die Fehlersuche in kleinen Scripten eingesetzt, ist aber heute der einfachen Ausgabe in die Console des Browsers gewichen.

Ausgaben mit dem Aufruf von Javascript console.log () erscheinen in der Browserkonsole.

print () druckt ein Fenster oder einen Frame, so als hätte der Benutzer den Befehl Drucken verwendet.
___

# Verzweigungen

Kontrollstrukturen sind Anweisungen, die wiederum Anweisungsblöcke enthalten. Dadurch ist es möglich, die Ausführung der in den Blöcken enthaltenen Anweisungen entsprechend bestimmter Regeln zu kontrollieren.

Man unterscheidet grundsätzlich zwei Arten von Kontrollstrukturen: Verzweigungen und Schleifen. Mittels Verzweigungen ist es möglich, die Ausführung einer oder mehrerer Anweisungs-Blöcke von Bedingungen abhängig zu machen (Fallunterscheidung). Schleifen ermöglichen, einen Anweisungs-Block wiederholt ausführen zu lassen.

**Wenn-Dann-Bedingungen mit "if"**

Sie können die Ausführung von Anweisungen von Bedingungen abhängig machen. In einer Verzweigung (bedingte Anweisung) wird ein Anweisungsblock nur durchlaufen, wenn eine Bedingung erfüllt ist. Alternativ kann beim Nichterfüllen der Bedingung ein zweiter Anweisungsblock durchlaufen werden.


Beispiel: allgemeines Schema
    if (Ausdruck) {
        //Anweisungsblock des True-Zweigs (wird ausgeführt, wenn Bedingung erfüllt ist)
        Anweisung;
        Anweisung;
    } else {
        //Anweisungsblock des False-Zweigs (wird ausgeführt, wenn Bedingung nicht erfüllt ist)
        Anweisung;
        Anweisung;
    }


Mit if leiten Sie eine Wenn-Dann-Bedingung ein (if = wenn). Dahinter folgt, in Klammern stehend, die Formulierung der Bedingung. Um solche Bedingungen zu formulieren, brauchen Sie Vergleichsoperatoren und in den meisten Fällen auch Variablen. Für Fälle, in denen die Bedingung nicht erfüllt ist, können Sie einen "andernfalls"-Zweig definieren. Dies geschieht durch else (else = sonst). Der Else-Zweig ist nicht zwingend erforderlich.

**Einfache Entweder-Oder-Abfrage**

Für einfache Entweder-Oder-Bedingungen gibt es mit dem bedingten (ternären) Operator eine spezielle Syntax, die Sie alternativ zur if/else-Anweisung verwenden können.



document.addEventListener('DOMContentLoaded', function () {

  document.querySelector('#check').addEventListener('click', Antwort);

function Antwort () {

      var Ergebnis = (document.Formular.Eingabe.value == '42') ? 'RICHTIG!' : 'FALSCH!';
      var text = 'Die Antwort ist ' + Ergebnis;
	  document.querySelector('output').innerText = text;
    }
	
});

Das Beispiel enthält eine JavaScript Funktion namens Antwort().

Wenn das Dokument geladen wird, wird mit addEventListener ein EventHandler hinzugefügt, der aufgerufen wird, wenn der Anwender in dem Formular auf den Klick-Button mit der Aufschrift OK und der id="check" klickt, und zwar mit dem click-Event.

Die Funktion prüft, ob der Wert des Eingabefeldes im Formular (document.Formular.Eingabe.value) den Wert 42 hat. Abhängig davon wird der Variablen Ergebnis entweder der Wert RICHTIG! oder FALSCH! zugewiesen. 

Anschließend wird ein entsprechender Satz zusammengesetzt (siehe dazu auch Operator für Zeichenkettenverknüpfung) und im output-Element ausgegeben.
Eine einfache Entweder-Oder-Abfrage wird mit einer Bedingung eingeleitet.

 Die Bedingung muss in Klammern stehen, im Beispiel (document.Formular.Eingabe.value == "42"). 
Dahinter wird ein Fragezeichen notiert.

 Hinter dem Fragezeichen wird ein Wert angegeben, der aktuell ist, wenn die Bedingung erfüllt ist. 
Dahinter folgt ein Doppelpunkt, und dahinter ein Wert für den Fall, dass die Bedingung nicht erfüllt ist. 

Da es sich um Werte handelt, die für die Weiterverarbeitung nur sinnvoll sind, wenn sie in einer Variablen gespeichert werden, wird einer solchen Entweder-Oder-Abfrage in der Regel eine Variable vorangestellt, im Beispiel die Variable Ergebnis. Der Variablen wird durch diese Art von Anweisung das Ergebnis der Entweder-Oder-Abfrage zugewiesen.


**Fallunterscheidung mit "switch"**

Mit if und else können Sie genau zwei Fälle unterscheiden. Wenn Sie feiner differenzieren, also zwischen mehreren Fällen unterscheiden wollen, können Sie zwar mehrere if-Abfragen hintereinander notieren, aber es gibt noch eine elegantere Möglichkeit: die Fallunterscheidung mit "switch".

var Eingabe = window.prompt('Geben Sie eine Zahl zwischen 1 und 4 ein:', ''),
    text = '';

switch (Eingabe) {

    case "1":
        text = 'Sie sind sehr bescheiden!';
        break;
    case "2":
        text = 'Sie sind ein aufrichtiger Zweibeiner!';
        break;
    case "3":
        text = 'Sie haben ein Dreirad gewonnen!';
        break;
    case "4":
        text = 'Gehen Sie auf allen Vieren und werden Sie bescheidener!';
        break;
    default:
        text = 'Sie bleiben leider dumm!';
        break;
}

var ausgabe = document.getElementById('ausgabe');

ausgabe.innerHTML = text;


Mit switch leiten Sie eine Fallunterscheidung ein (switch = Schalter). Dahinter folgt, in runde Klammern eingeschlossen, eine Variable oder ein Ausdruck, für dessen aktuellen Wert Sie die Fallunterscheidung durchführen. Im Beispiel ist das die Variable mit dem Namen Eingabe. Diese Variable wird vor der Fallunterscheidung mit einem Wert versorgt, denn ein Dialogfenster (window.prompt()) mit einem Eingabefeld fordert den Anwender auf, eine Zahl zwischen 1 und 4 einzugeben. Der eingegebene Wert wird in Eingabe gespeichert.

Die einzelnen Fälle, die Sie abfragen möchten, werden innerhalb geschweifter Klammern notiert. Jeden einzelnen Fall leiten Sie mit case ein (case = Fall). Dahinter folgt die Angabe des Wertes, auf den Sie prüfen wollen. Die Anweisung case "1": im obigen Beispiel bedeutet dann so viel wie: 'wenn die Variable Eingabe den Wert "1" hat'. Im Beispiel wird für jeden Fall eine individuelle Meldung ausgegeben.

Wichtig ist dabei auch das Wort break am Ende jedes Falls (break = abbrechen). Wenn Sie das Wort weglassen, werden nämlich alle nachfolgenden Fälle auch ausgeführt, aber das wollen Sie ja in der Regel nicht.

Für den Fall, dass keiner der definierten Fälle zutrifft, können Sie am Ende der Fallunterscheidung den Fall default: definieren. Die darunter stehenden Anweisungen werden ausgeführt, wenn keiner der anderen Fälle zutrifft.

___

# Schleifen

**Schleifen mit "while"**

Mit Hilfe von while-Schleifen können Sie Programmanweisungen solange wiederholen, wie die Bedingung, die in der Schleife formuliert wird, erfüllt ist. Solche Schleifen eignen sich dann, wenn Sie nicht wissen, wie oft die Schleife durchlaufen werden soll.

    var eingabe = "",
	text    = "",
        zaehler = 1;
    while (eingabe != "how to make love" && zaehler <= 3) {
      eingabe = window.prompt(zaehler + ". Versuch: Was bedeutet 'HTML'?", "");
      zaehler++;
    }

    if (eingabe != "how to make love") {
      text = "Lernen Sie erst mal HTML! ...";
    } else {
      text = "Fein, Sie haben verstanden worum es geht! ...";
    }

  document.querySelector('output').innerText = text;

Das Beispiel bittet den Anwender in einer while-Schleife bis zu drei mal in einem Dialogfenster (window.prompt()), die Bedeutung der Abkürzung 'HTML' einzugeben.

Die Schleife kann aus zwei Gründen beendet werden: entweder der Anwender gibt die richtige Bedeutung der Abkürzung ein, oder die Variable zaehler, die die Anzahl der Versuche mitzählt, hat einen Wert größer als 3. Wenn die Schleife beendet ist, steht also nicht fest, aus welchen der beiden möglichen Ursachen sie beendet wurde. Um das zu entscheiden, wird im Beispiel deshalb anschließend mit Hilfe einer if-Abfrage nochmals überprüft, ob die Schleife deshalb beendet wurde, weil die Eingabe falsch war. 

Je nachdem, ob sie falsch oder richtig war, wird mit document.querySelector('output').innerText ein entsprechender Satz in das output-Element der Webseite eingefügt.

Eine while-Schleife beginnt mit dem Wort while (while = solange). Dahinter folgt, in Klammern stehend, die Bedingung. Um eine Bedingung zu formulieren, brauchen Sie Vergleichsoperatoren. Der Inhalt der Schleife wird solange wiederholt, wie die Schleifenbedingung wahr ist.

In der Regel enthält eine while-Schleife mehrere Anweisungen, die innerhalb der Schleife stehen. Notieren Sie alle Anweisungen innerhalb geschweifter Klammern { und }, so wie im Beispiel (siehe auch den Abschnitt über Anweisungsblöcke).

**Schleifen mit "for"**

Der Schleifenkopf einer for-Schleife enthält eine Zählvariable, eine Fortführungsbedingung sowie eine Anweisung zur Änderung der Zählvariable.


  var text = "";

  for (var i = 10; i <= 36; i++) {

    text = text + '<span style="font-size:' + i + 'px">Schrift mit ' + i + ' Pixel Größe<\/span><br>';
    document.querySelector('output').innerHTML = text;
  }

Das Beispiel definiert eine Variable namens text, die im Verlauf einer for-Schleife immer mehr Inhalt erhält und am Ende mit document.querySelector('output').innerHTML ihren ganzen Inhalt ins Browser-Fenster schreibt.

Die for-Schleife wird insgesamt 27 mal durchlaufen, nämlich so oft, wie der Zähler, der in der Variablen i definiert und mit dem Wert 10 initialisiert wird, kleiner oder gleich 36 ist, wobei er bei jedem Schleifendurchlauf um 1 erhöht wird (i++).

Mit jedem Schleifendurchgang wird die Variable Ausgabe mit ihrem jeweils bisherigen Wert um etwas HTML-Code mit der CSS-Angabe font-size (Schriftgröße) erweitert. Der Wert, der font-size dabei zugewiesen wird, ist jeweils der Wert von i. So entsteht der Effekt, dass CSS-Angaben von font-size:10px bis font-size:36px erzeugt werden. Das Ergebnis wird am Ende ausgegeben.

 Zum Verständnis der zusammengesetzten Teile bei Ausgabe siehe auch Operator für Zeichenkettenverknüpfung).

Eine for-Schleife beginnt mit dem Wort for. Dahinter wird, in Klammern stehend, die Schleifenbedingung formuliert. Bei der for-Schleife gilt dabei eine feste Syntax. Innerhalb der Schleifenbedingung werden drei Anweisungen notiert. In der ersten Anweisung wird ein Schleifenzähler definiert und initialisiert. Im Beispiel wird ein Zähler i definiert und mit dem Wert 10 initialisiert. 

Die zweite Anweisung enthält die Bedingung für den Schleifenablauf; die Schleife wird ausgeführt, wenn und solange diese zutrifft. Dazu brauchen Sie Vergleichsoperatoren. In der dritten Anweisung wird der Schleifenzähler so verändert, dass er irgendwann die in der zweiten Anweisung notierte Bedingung erfüllt. 

Im Beispiel wird der Zähler mit i++ bei jedem Schleifendurchgang um 1 erhöht. An dieser Stelle könnte aber auch so etwas stehen wie i=i+10 (bei jedem Schleifendurchgang um 10 erhöhen).

**Schleifen mit "for...in"**

Eine spezielle Abart der for-Schleife ist die for..in-Schleife. Mit ihr kann über alle Eigenschaften eines Objekts iteriert werden.


 var Ausgabe = "";
 for (var Eigenschaft in document) {

   Ausgabe = Ausgabe + "document." + Eigenschaft + ": " + document[Eigenschaft] + "";

 }

 document.querySelector('output').innerHTML = Ausgabe;

Das Beispiel zeigt, wie Sie mit Hilfe einer for..in-Schleife einiges über die JavaScript-Fähigkeiten Ihres Browsers herausbekommen können. Im Beispiel werden die Eigenschaften des Objektes document ausgegeben. Mit jedem Schleifendurchgang wird die Variable Ausgabe um eine Objekteigenschaft erweitert. Den aktuellen Wert der Objekteigenschaft können Sie sich mit Objektname[Eigenschaft] ausgeben lassen. Die Schleife läuft so lange, wie es verfügbare Objekteigenschaften gibt - dies bedeutet das for .. in.

**Schleifen mit "for...of"**

Mit einer for...of-Schleife kann über alle Eigenschaften eines Objekts iteriert (schrittweise durchgegangen) werden. Anders als bei der for...in-Schleife werden nicht der Index, sondern die im Array gespeicherten Werte ausgegeben.[2][3]

Beispiel: Vergleich der klassischen for-in- mit der for-of-Schleife
const numbers = [2, 3, 5, 7, 11, 13, 17, 19];
numbers.name = 'Primzahlen';

//for-in-Schleife
for (let i in numbers) {
  console.log(i);   // 0, 1, 2, 3, 4, 5, 6, 7, name
}

//for-of-Schleife
for (let i of numbers) {
  console.log(i);   // 2, 3, 5, 7, 11, 13, 17, 19
}
Die for...of-Schleifen eignen sich für Strings, Arrays und Maps sowie für NodeLists, nicht jedoch für Objekte, da diese keine iterierbaren Eigenschaften besitzen.

**Schleifen mit "do-while"**

Die do-while-Schleife ist eine Variante der normalen while-Schleife. Der Unterschied zwischen beiden ist, dass bei der normalen while-Schleife vor dem Ausführen des Codes die Schleifenbedingung überprüft wird, während bei der do-while-Schleife zuerst der Code ausgeführt und erst danach die Schleifenbedingung überprüft wird. Auf diese Weise können Sie erzwingen, dass Anweisungen innerhalb der Schleife auf jeden Fall mindestens einmal ausgeführt werden, auch wenn sich die Schleifenbedingung gleich am Anfang als unwahr herausstellt.

 var x = 10;
 do {
   document.querySelector('output').innerHTML = "x × x = " + (x * x);
   x = x + 1;
 } while (x < 10);

Und einmal so:


 var x = 10;
 while (x < 10) {
   document.querySelector('output').innerHTML = "x * x = " + (x * x);
   x = x + 1;
 }

  </script>

In den Beispielen werden jeweils ein kleiner JavaScript-Bereich definiert. In beiden Bereichen wird eine Variable x definiert und mit dem Wert 10 vorbelegt.

Im ersten Bereich wird solange das Quadrat von x (das bei jedem Schleifendurchlauf um 1 erhöht wird) geschrieben, wie x kleiner als 10 ist. Da x ja schon am Beginn den Wert 10 hat, ist die Abbruchbedingung eigentlich schon von vorne herein erfüllt. Trotzdem wird einmal das Quadrat von x ausgegeben, da die Überprüfung der Schleifenbedingung erst nach dem Ausführen der Anweisungen innerhalb der Schleife erfolgt.

Im zweiten Script-Bereich herrschen die gleichen Bedingungen, jedoch wird dort eine normale while-Schleife notiert. Da x von vorne herein nicht kleiner als 10 ist, werden die Anweisungen der while-Schleife kein einziges Mal ausgeführt. Die Überprüfung der Schleifenbedingung, die am Anfang stattfindet, verhindert dies.
