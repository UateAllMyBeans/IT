# IT Infrastruktuuri projekt

# Disainiotsused ja põhjendused

## Operatsioonisüsteem – Linux server (Ubuntu)
Valisime Ubuntu linux serveri, kuna see on avatud lähtekoodiga ja tasuta, mistõttu puuduvad litsentsikulud. Lisaks on see ressursisäästlik ning sobib hästi serverikeskkonda. 

---

Õpilaste tööjaamad – Windows 11

Õpilaste arvutites kasutame Windows 11 operatsioonisüsteemi, kuna see on laialdaselt kasutatav ja kasutajasõbralik. Windows 11 pakub head ühilduvust erinevate õppetööks vajalike programmide ja rakendustega ning võimaldab lihtsat ühendamist kooli võrgu ja failiserveriga. Lisaks on õpilastel süsteem tuttav, mis muudab igapäevase kasutamise lihtsamaks ja vähendab tehniliste probleemide tekkimist.

---

## Staatiline IP-aadress
Staatiline IP-aadressi valisime, kuna server peab olema alati kättesaadav sama aadressi kaudu. See tagab stabiilse ligipääsu teenustele, nagu failijagamine ja veebiserver, ning lihtsustab seadistamist ja vigade tuvastamist. 

---

## Sisemine võrk
Sisemine võrgu valisime, kuna see eraldab süsteemi välisest internetist ning vähendab turvariske. Õpilased saavad VPN-ida sisse kui vaja väljast poolt kooli ligipääsu teenustele või failiserverile. 

---

## Failijagamise teenus
Failijagamise teenuse valisime, kuna see võimaldab õpilastel faile lihtsalt jagada ja kasutada. Kõik failid paiknevad keskserveris, mis teeb haldamise administraatori jaoks lihtsamaks ja aitab hoida süsteemi korrastatuna. Failijagamise teenuseks kasutame Sambat.

---

## Veebiserver
Veebiserveri lisamise valimise, kuna see võimaldab majutada sisemist infot, näiteks kooliga seotud teavet. 

---

## Kasutajarollid (admin ja student)
Kasutusele võtame rollipõhise ligipääsu, kus admin kasutajal on täielikud õigused ning student kasutajal piiratud ligipääs. 

---

## Turvameetmed
Turvalisuse tagamiseks rakendame mitmeid meetmeid. Kasutame tugevaid paroole, et vältida volitamata ligipääsu. Tulemüür (UFW) lubab ainult vajalikud ühendused. Root kasutaja otsene sisselogimine on keelatud, mis vähendab rünnakute riski. Lisaks on aktiivsed ainult vajalikud teenused, mis vähendab võimalikke ründevektoreid.

---

## Dockeri kasutamine 
Dockerit kasutame, kuna see lihtsustab teenuste paigaldamist ja haldamist. See tagab ühtlase keskkonna erinevates süsteemides, vähendab konfiguratsioonivigu ning muudab süsteemi lihtsamini hallatavaks ja laiendatavaks.

---
