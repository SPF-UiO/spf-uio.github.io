---
permalink: /
excerpt: |
  Vi er arbeidsgiveren for frivillige ved studentkjellerne tilknyttet Universitet i Oslo,
  og håndterer lønn, forsikringer og fakturering av personalkostnader. <br />
  
layout: splash
header:
  #overlay_color: lightgray
  overlay_color: '#CE2029'
  cta_label: <i class='fa fa-at'></i> &nbsp; Kontakt oss
  cta_url: mailto:&#115;&#112;&#102;&#045;&#115;&#116;&#121;&#114;&#101;&#116;&#064;&#115;&#116;&#117;&#100;&#111;&#114;&#103;&#046;&#117;&#105;&#111;&#046;&#110;&#111;

intro:
  - excerpt: Hva burde stå her?

feature_row:
  - title: Arbeidere
    url: /medlemmer/
    btn_label: Kontakt lokal utlånsansvarlig &nbsp; <i class="fas fa-fw fa-arrow-circle-right"></i>
    btn_class: btn--success
    excerpt: |
      For deg som jobber hos oss, for en av medlemsforeningene, og som

      * Ønsker lønnsinformasjon
      * Har lønnsspørsmål
      * Opplevd yrkesskade


  - title: Medlemsforeninger
    url: https://spf.cyb.no
    btn_label: Åpne SPBM &nbsp; <i class="fas fa-fw fa-user-lock"></i>
    btn_class: btn--info
    excerpt: |
      For deg som er representant på SPFs styre, og som ønsker ting som

      * Ønsker oversikt over registrerte jobber
      * Liste over arbeidere
      * Oppfølging av faktura

  - title: Styremedlemmer
    url: https://wiki.cyb.no/display/SPF
    btn_label: |
      Åpne viteboken &nbsp;
      <span class="fa-layers fa-fw">
       <i class="fas fa-user-lock"></i>
       <i class="fas fa-external-link-alt fa-inverse" data-fa-transform="shrink-8 right-8 up-8"></i>
      </span>
    btn_class: btn--danger
    excerpt: |
      For du som er representant på SPFs styre, og leter etter ting som

      * Kundeforhold
      * Arbeidsgiveransvar
      * Økonomi og rutiner

---

{% assign members = site.data.members | sort: 'org' %}

Studentkjellernes personalforening er en samarbeids- og personalforening mellom
{% for member in members -%}
	{% if forloop.last %} og 
	{% elsif forloop.first == false %}, {% endif -%}
<a href="{{ member.url }}" title="Gå til {{ member.org }} sin hjemmeside" rel="external">
	{{ member.org }}</a> 
{%- endfor -%}
.


# Hva kan SPF hjelpe deg med?

{% include feature_row %}




Har du noen spørsmål som ikke er svart på her? Ta kontakt med [SPF sitt styre][epost].


[Cybernetisk Selskab]: http://cyb.no
[Kjellerutvalget]: https://www.facebook.com/TraugotsKjeller/
[Realistforeningen]: https://foreninger.uio.no/rf/
[RF-regi]: https://foreninger.uio.no/rf/regi/
[Medicinerforeningen]: https://foreninger.uio.no/medicinerforeningen/
[Samfunnsvitenskapelig fakultetsforening]: http://svff.no/
[Uglebo]: https://foreninger.uio.no/filologisk-forening/

[epost]: mailto:&#115;&#112;&#102;&#045;&#115;&#116;&#121;&#114;&#101;&#116;&#064;&#115;&#116;&#117;&#100;&#111;&#114;&#103;&#046;&#117;&#105;&#111;&#046;&#110;&#111;
