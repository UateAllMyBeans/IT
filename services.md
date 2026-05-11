Operatsioonisüsteem – Ubuntu Server

Serveri operatsioonisüsteemina kasutati Ubuntu Server Linuxit. Ubuntu valiti, kuna tegemist on tasuta ja avatud lähtekoodiga operatsioonisüsteemiga, millel puuduvad litsentsikulud. Lisaks on Ubuntu Server ressursisäästlik, stabiilne ning sobib hästi serverikeskkondades kasutamiseks. Süsteem võimaldab hallata erinevaid teenuseid, kasutajaid ja võrguühendusi.

SSH teenus (OpenSSH)

SSH teenust kasutati serveri kaugelt haldamiseks. SSH võimaldab administraatoritel serverisse turvaliselt sisse logida ilma füüsilise ligipääsuta. Serveris keelati root kasutaja otsene sisselogimine ning ligipääs lubati ainult määratud kasutajatele. SSH võimaldab meeskonnaliikmetel serverit turvaliselt hallata ja seadistada.

Tulemüür (UFW)

Serveri turvalisuse tagamiseks kasutati UFW tulemüüri. Tulemüüri abil lubati ainult vajalikud ühendused ja teenused. Avatud pordid olid SSH jaoks port 22, veebiserveri jaoks port 80 ning Samba failijagamise jaoks pordid 139 ja 445. Tulemüür aitab vähendada turvariske ja piirata soovimatut ligipääsu serverile.

Samba failijagamise teenus

Failide jagamiseks kasutati Samba teenust. Samba võimaldab Linuxi ja Windowsi arvutite vahel failide jagamist ning ligipääsu ühistele kaustadele. Projekti käigus loodi jagatud kaust, millele määrati grupipõhised õigused. See võimaldab kasutajatel ühiselt faile kasutada ning lihtsustab failide haldamist.

Apache veebiserver

Veebiteenuse pakkumiseks paigaldati Apache veebiserver. Apache võimaldab majutada veebilehti ja sisemist infot serveris. Projekti käigus loodi lihtne veebileht, mille kaudu saab kontrollida veebiserveri toimimist. Apache on üks enim kasutatavaid veebiservereid ning sobib hästi väiksemate infosüsteemide majutamiseks.

Docker

Dockerit kasutati konteineripõhiste teenuste käitamiseks. Docker võimaldab teenuseid käivitada eraldatud konteinerites, mis muudab süsteemi lihtsamini hallatavaks ja paindlikumaks. Konteinerid aitavad vähendada konfiguratsioonivigu ning võimaldavad teenuseid kiiresti paigaldada ja eemaldada.

Nginx Docker konteineris

Dockeri abil käivitati Nginx veebiserver konteineris. Nginx töötas eraldi konteinerina ning sellele pääses ligi läbi serveri IP-aadressi ja pordi 8080. Konteineripõhine lahendus demonstreerib kaasaegset teenuste haldamist ning võimaldab teenuseid põhisüsteemist eraldada.

Kasutajate ja gruppide haldus

Serveris loodi eraldi kasutajakontod meeskonnaliikmetele ning kasutati grupipõhist õiguste haldust. Administraatoritele anti sudo õigused süsteemi haldamiseks, tavakasutajatele määrati piiratud ligipääs. Selline lahendus parandab süsteemi turvalisust ja lihtsustab kasutajate haldamist.
