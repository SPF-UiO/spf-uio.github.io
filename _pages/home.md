---
title: Hvem er SPF, og hva gjør vi?
permalink: /
excerpt: |
  Vi er arbeidsgiveren for frivillige ved studentkjellerne tilknyttet Universitet i Oslo,
  og håndterer lønn, forsikringer og fakturering av personalkostnader på vegne av våre 
  medlemmer.
  
layout: splash
header:
  #overlay_color: lightgray
  overlay_color: '#CE2029'
  cta_label: Kontakt våre utleiere &nbsp; <i class='fas fa-fw fa-users'></i>
  cta_url: '#utleie-og-medlemmer'

intro:
  - excerpt: Hva burde stå her?

feature_row:
  - title: Arbeidere
    url: '#utleie-og-medlemmer'
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
      * Deres plikter
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

Har du noen spørsmål som ikke er svart på her? Ta kontakt med [styret i Studentkjellernes personalforening][epost].

---

# Utleie og medlemmer

{:.notice--success}
**Leter du etter et lokale på Blindern eller Gaustad?** SPFs medlemmer tilbyr
*rimelig* utleie av deres lokaler til fester, presentasjoner, sammenkomster,
konserter, julebord, og mer.


## Studentkjellere

<table> 
  <thead> 
    <tr>
      <th>Forening</th>
      <th>Kjeller</th>
      <th>Kapasitet</th>
      <th class="thin"></th>
      <th class="thin"></th>
      <th class="thin"></th>
    </tr>
  </thead>
  <tbody>
  {% assign pubs = site.data.members | where:"type", "pub" | sort: "name" %}
  {% for member in pubs %}
  <tr>
    <td><a href="{{ member.url }}" rel="external">{{ member.org }}</a></td>
    <td><strong>{{ member.name }}</strong></td>
    <td>{% if member.capacity %}{{ member.capacity }} stk.{% else %}<i class="fas fa-fw fa-question"></i>{% endif %}</td>
    <td class="thin">
			{% include button.html text='Kontakt' member=member btn='info' icon='envelope' link=member.contact 
			title="Ta kontakt om du har ønsker å leie lokalet, har spørsmål om lyd, lys, servering, osv., eller om du har personalspørsmål" %}
		</td>
    <td class="thin">
			{% include button.html text='Kart' member=member btn='success' icon='map-marked-alt' link=member.map_url
			title="Åpne kart som viser hvor du finner lokalet" %}
		</td>
    <td class="thin">
			{% include button.html text='Bestillingskjema' member=member btn='primary' icon='file-alt' link=member.booking_url 
			title="Send inn bestillingsskjema for utlån direkte uten å måtte sende e-post til kjelleren" %}
		</td>
  </tr>
  {% endfor %}
</tbody>
</table>


## Lyd, lys og scene

<table> 
  <thead> 
    <tr>
      <th>Forening</th>
      <th class="thin"></th>
    </tr>
  </thead>
  <tbody>
  {% assign rentals = site.data.members | where:"type", "rental" | sort: "name" %}
  {% for member in rentals %}
  <tr>
    <td><strong><a href="{{ member.url }}" rel="external">{{ member.org }}</a></strong></td>
    <td class="thin">
			{% include button.html text='Kontakt' member=member btn='info' icon='envelope' link=member.contact 
			title="Ta kontakt om du har ønsker å leie lokalet, har spørsmål om lyd, lys, servering, osv., eller om du har personalspørsmål" %}
		</td>
  </tr>
  {% endfor %}
</tbody>
</table>

[epost]: mailto:&#115;&#112;&#102;&#045;&#115;&#116;&#121;&#114;&#101;&#116;&#064;&#115;&#116;&#117;&#100;&#111;&#114;&#103;&#046;&#117;&#105;&#111;&#046;&#110;&#111;
