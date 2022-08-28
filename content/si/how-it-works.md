---
title: එය වැඩ කරන්නේ කෙසේද
linkTitle: ලෙට්'ස් එන්ක්‍රිප්ට් වැඩ කරන්නේ කෙසේද
slug: how-it-works
top_graphic: 3
lastmod: 2019-10-18
show_lastmod: 1
---


ලෙට්'ස්&nbsp; එන්ක්‍රිප්ට් සහ [ACME කෙටුම්පතෙහි](https://tools.ietf.org/html/rfc8555) පරමාර්ථය වන්නේ HTTPS සේවාදායකයක් පිහිටුවීමට සහ එය ස්වයංක්‍රීයව කිසිදු මානව මැදිහත්වීමකින් තොරව අතිරික්සු-විශ්වසනීය සහතිකයක් අත් කර ගැනීමට සැලැස්වීමයි.  මෙය වියමන සේවාදායකයෙහි සහතික කළමණාකරණ නියෝතයක් ධාවනය කිරීමෙන් ඉටු කර ගැනේ.

තාක්ෂණය ක්‍රියා කරන ආකාරය තේරුම් ගැනීමට, ලෙට්'ස්&nbsp; එන්ක්‍රිප්ට් සඳහා සහාය දක්වන සහතික කළමණාකරණ නියෝතයක් සමඟින් `https://උදාහරණය.ලංකා/` පිහිටුවීමේ ක්‍රියාවලිය හරහා ගමන් කරමු.

මෙම ක්‍රියාවලිය සඳහා පියවර දෙකක් ඇත.  පළමුව, වියමන සේවාදායකය වසමක් පාලනය කරන බව නියෝතය ස.අධි. (CA) වෙත ඔප්පු කරයි.  එවිට, නියෝතයට එම වසම සඳහා සහතික ඉල්ලීමට, අලුත් කිරීමට සහ අහෝසි කිරීමට හැකිය.

## වසම වලංගුකරණය

ලෙට්'ස්&nbsp; එන්ක්‍රිප්ට් ප්‍රසිද්ධ යතුර මගින් සේවාදායක පරිපාලක හඳුනා ගනියි.  නියෝත මෘදුකාංගය ලෙට්'ස්&nbsp;එන්ක්‍රිප්ට් සමඟ අන්තර්ක්‍රියා කරන පළමු වතාවේදී, එය නව යතුරු යුගලයක් ජනනය කරන අතර සේවාදායකය වසම් එකක් හෝ කිහිපයක් පාලනය කරන බව ලෙට්'ස්&nbsp;එන්ක්‍රිප්ට් ස.අධි. වෙත ඔප්පු කරයි.  මෙය ගිණුමක් සෑදීමේ සහ එම ගිණුමට වසම් එකතු කිරීමේ සම්ප්‍රදායික ස.අධි. (CA) ක්‍රියාවලියට සමාන වේ.

ක්‍රියාවලිය පටන් ගැනීමට, නියෝතය එය `උදාහරණය.ලංකා` පාලනය කරන බව ඔප්පු කිරීමට කුමක් කළ යුතු දැයි ලෙට්'ස් එන්ක්‍රිප්ට් ස.අධි. (CA) න් අසයි.  ලෙට්'ස් එන්ක්‍රිප්ට් ස.අධි. (CA) වෙතින් ඉල්ලා සිටින වසම් නාමය දෙස බලා අභියෝග මාලාවක් හෝ එකක් නිකුත් කරයි.   මේවා නියෝතයට වසම පාලනය කිරීම ඔප්පු කළ හැකි විවිධ මාර්ග වේ.  උදාහරණයක් ලෙස, ස.අධි. (CA) නියෝතයට වරණය කිරීමට පහත දෑ දිය හැකිය:

* `උදාහරණය.ලංකා` යටතේ ව.නා.ප. වාර්තාවක් සැකසීම, හෝ
* `http://උදාහරණය.ලංකා/` හි හොඳින්-දන්නා ඒ.ස.හැ. (URI) යටතේ HTTP සම්පතක් සැකසීම

අභියෝග සමඟින්, ලෙට්'ස් එන්ක්‍රිප්ට් ස.අධි. (CA) එය යතුරු යුගලය පාලනය කරන බව ඔප්පු කිරීම සඳහා නියෝතයට එහි පෞද්ගලික යතුරු යුගලය සමඟ අත්සන් කළ යුතු එක් වර අංකයක් (අභිමත අංකයක්) ද සපයයි.

<div class="howitworks-figure">
<img alt="උදාහරණය.ලංකා වලංගු කිරීමට අභියෝග ඉල්ලා සිටීම"
     src="/images/howitworks_challenge.png"/>
</div>

නියෝත මෘදුකාංගය සපයන ලද අභියෝග මාලාවන්ගෙන් එකක් සම්පූර්ණ කරයි.   ඉහත දෙවන කාර්යය ඉටු කිරීමට හැකි යැයි සිතමු: එය `http://උදාහරණය.ලංකා` අඩවියේ නිශ්චිත මාර්ගයක ගොනුවක් සාදයි.  නියෝතය එහි පෞද්ගලික යතුර සමඟ සැපයූ එක් වර අංකය (අභිමත අංකය) අත්සන් කරයි.  නියෝතය මෙම පියවර සම්පූර්ණ කළ පසු, එය වලංගු කිරීම සම්පූර්ණ කිරීමට සූදානම් බව ස.අධි. (CA) වෙත දැනුම් දෙයි.

එවිට, අභියෝග සන්තෘප්ත වී ඇත්දැයි පරීක්ෂා කිරීම ස.අධි. (CA)  යේ කාර්යයයි.  ස.අධි. එක් වර අංකයේ අත්සන සත්‍යාපනය කරයි, සහ එය වියමන සේවාදායකයෙන් ගොනුව බාගැනීමට තැත් කරන අතර එහි අපේක්ෂිත අන්තර්ගතය ඇති බවට සැක දුරු කර ගනියි.

<div class="howitworks-figure">
<img alt="උදාහරණය.ලංකා සඳහා බලය දීම වෙනුවෙන් ක්‍රියා කිරීමට ඉල්ලා සිටීම"
     src="/images/howitworks_authorization.png"/>
</div>

එක් වර අංකයෙහි අත්සන වලංගු නම් සහ අභියෝග පරීක්ෂා කර ඇත්නම්, `උදාහරණය.ලංකා` සඳහා සහතික කළමණාකරණය කිරීමට ප්‍රසිද්ධ යතුර මගින් හඳුනාගත් නියෝතයට බලය ලැබේ.  අපි නියෝතය භාවිතා කළ යතුරු යුගලය `උදාහරණය.ලංකා` සඳහා "බලයලත් යතුරු යුගලය" ලෙස හඳුන්වමු.


## සහතික නිකුත් කිරීම සහ අහෝසි කිරීම

නියෝතයට බලයලත් යතුරු යුගලයක් ඇති පසු, සහතික ඉල්ලීම, අලුත් කිරීම සහ අහෝසි කිරීම සරලයි--- සහතික කළමණාකරණ පණිවිඩ යවා ඒවා බලයලත් යතුරු යුගලයෙන් අත්සන් කරන්න.

වසම සඳහා සහතිකයක් අත් කර ගැනීමට, නියෝතය විසින් `උදාහරණය.ලංකා` සඳහා නිශ්චිත ප්‍රසිද්ධ යතුරක් සමඟ සහතිකයක් නිකුත් කිරීමට ලෙට්'ස්&nbsp;එන්ක්‍රිප්ට් ස.අධි. (CA) න් අසන PKCS#10 [සහතික අත්සන් කිරීමේ ඉල්ලීමක්](https://tools.ietf.org/html/rfc2986) ගොඩනඟයි.  සාමාන්‍ය පරිදි, ස.අ.ඉ. හි ප්‍රසිද්ධ යතුරට අනුරූප පෞද්ගලික යතුරෙහි අත්සනක් ස.අ.ඉ (CSR) දී ඇතුළත් කෙරේ.  නියෝතය ද `උදාහරණය.ලංකා` සඳහා බලය ලත් යතුර සමඟ සමස්ථ ස.අ.ඉ. (CSR) අත්සන් කරයි, එවිට එය බලයලත් බව ලෙට්'ස්&nbsp;එන්ක්‍රිප්ට් ස.අධි. දැන ගනී.

ලෙට්'ස්&nbsp;එන්ක්‍රිප්ට් ස.අධි. වෙත ඉල්ලීම ලැබුණු විට, එය අත්සන් දෙකම සත්‍යාපනය කරයි.  සෑම දෙයක්ම හොඳින් බව පෙනෙන්නේ නම්, එය `උදාහරණය.ලංකා` සඳහා ස.අ.ඉ (CSR) වෙතින් ප්‍රසිද්ධ යතුර ද සමඟ සහතිකයක් නිකුත් කර එය නියෝතය වෙත ආපසු එවයි.

<div class="howitworks-figure">
<img alt="උදාහරණය.ලංකා සඳහා සහතිකයක් ඉල්ලීම"
     src="/images/howitworks_certificate.png"/>
</div>

අහෝසි කිරීම ද සමාන අන්දමකින් සිදු කෙරේ.  නියෝතය `උදාහරණය.ලංකා` සඳහා බලයලත් යතුරු යුගලය සමඟ අහෝසි කිරීමේ ඉල්ලීමක් අත්සන් කරයි, සහ ලෙට්'ස්&nbsp;එන්ක්‍රිප්ට් ස.අධි. ඉල්ලීම බලයලත් බව සත්‍යාපනය කරයි.  එසේ නම්, එය අහෝසි කිරීමේ තොරතුරු සාමාන්‍ය අහෝසි කිරීමේ නාලිකා (එනම් මා.ස.ත.කෙ. / OCSP) වෙත ප්‍රකාශයට පත් කරයි, එවිට අතිරික්සු වැනි විශ්වාස කරන පාර්ශ්වයන්ට ඔවුන් අහෝසි කළ සහතිකය පිළි නොගත යුතු බව දැන ගත හැකිය.

<div class="howitworks-figure">
<img alt="උදාහරණය.ලංකා සඳහා සහතිකයක් අහෝසි කිරීමට ඉල්ලීම"
     src="/images/howitworks_revocation.png"/>
</div>


