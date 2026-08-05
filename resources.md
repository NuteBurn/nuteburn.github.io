---
layout: page
title: Resources
custom_class: wide-layout
---

* Do not remove this line (it will not be displayed)
{:toc}

{% assign resources = site.data.resources %}
{% assign rating_icon = "fa-solid fa-fire" %}

## <i class="fa-solid fa-book" aria-hidden="true"></i> Books
{: #books}

<section class="resourceSection">
  <div class="resourceGrid">
    {% assign books = resources | where: "type", "book" %}
    {% for resource in books %}
      {% capture card_classes %}{% if resource.rating == 5 %} card-featured{% endif %}{% if resource.notes.size > 100 %} card-wide{% endif %}{% endcapture %}
      {% include resource-card.html resource=resource card_classes=card_classes rating_icon=rating_icon %}
    {% endfor %}
  </div>
</section>

## <i class="fa-solid fa-globe" aria-hidden="true"></i> Websites
{: #websites}

<section class="resourceSection">
  <div class="resourceGrid">
    {% assign websites = resources | where: "type", "website" %}
    {% for resource in websites %}
      {% capture card_classes %}{% if resource.rating == 5 %} card-featured{% endif %}{% endcapture %}
      {% include resource-card.html resource=resource card_classes=card_classes rating_icon=rating_icon %}
    {% endfor %}
  </div>
</section>

## <i class="fa-brands fa-youtube" aria-hidden="true"></i> YouTube Channels
{: #youtube}

<section class="resourceSection">
  <div class="resourceGrid">
    {% assign youtube = resources | where: "type", "youtube" %}
    {% for resource in youtube %}
      {% capture card_classes %}{% if resource.rating == 5 %} card-featured{% endif %}{% if resource.favoriteContent %} card-wide{% endif %}{% endcapture %}
      {% include resource-card.html resource=resource card_classes=card_classes rating_icon=rating_icon %}
    {% endfor %}
  </div>
</section>

## <i class="fa-brands fa-reddit" aria-hidden="true"></i> Subreddits
{: #reddit}

<section class="resourceSection">
  <div class="resourceGrid resourceGrid-compact">
    {% assign reddit = resources | where: "type", "reddit" %}
    {% for resource in reddit %}
      {% include resource-card.html resource=resource rating_icon=rating_icon %}
    {% endfor %}
  </div>
</section>

## <i class="fa-solid fa-users" aria-hidden="true"></i> Lemmy Communities
{: #lemmy}

<section class="resourceSection">
  <div class="resourceGrid resourceGrid-compact">
    {% assign lemmy = resources | where: "type", "lemmy" %}
    {% for resource in lemmy %}
      {% include resource-card.html resource=resource rating_icon=rating_icon %}
    {% endfor %}
  </div>
</section>

## <i class="fa-solid fa-seedling" aria-hidden="true"></i> Seed Banks
{: #seed-banks}

<section class="resourceSection">
  <div class="resourceGrid">
    {% assign seedbanks = resources | where: "type", "seed-bank" %}
    {% for resource in seedbanks %}
      {% capture card_classes %}{% if resource.rating == 5 %} card-featured{% endif %}{% endcapture %}
      {% include resource-card.html resource=resource card_classes=card_classes rating_icon=rating_icon %}
    {% endfor %}
  </div>
</section>

## <i class="fa-solid fa-dna" aria-hidden="true"></i> Breeders
{: #breeders}

<section class="resourceSection">
  <div class="resourceGrid">
    {% assign breeders = resources | where: "type", "breeder" %}
    {% for resource in breeders %}
      {% capture card_classes %}{% if resource.rating == 5 %} card-featured{% endif %}{% endcapture %}
      {% include resource-card.html resource=resource card_classes=card_classes rating_icon=rating_icon %}
    {% endfor %}
  </div>
</section>

## <i class="fa-solid fa-store" aria-hidden="true"></i> Chicago Grow Stores
{: #chicago-stores}

<section class="resourceSection">
  <div class="resourceGrid">
    {% assign stores = resources | where: "type", "local-store" %}
    {% for resource in stores %}
      {% capture card_classes %}{% if resource.status == 'closed' %} card-closed{% endif %}{% endcapture %}
      {% include resource-card.html resource=resource card_classes=card_classes rating_icon=rating_icon %}
    {% endfor %}
  </div>
</section>
