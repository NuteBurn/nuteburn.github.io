---
layout: page
title: Resources
custom_class: wide-layout
---

* Do not remove this line (it will not be displayed)
{:toc}

{% assign resources = site.data.resources %}
{% assign rating-icon = "fa-solid fa-fire" %}
{% assign rating-icon-sub = "fa-solid fa-fire" %}

## <i class="fa-solid fa-book" aria-hidden="true"></i> Books
{: #books}

  <section class="resourceSection">
    <div class="resourceGrid">
      {% assign books = resources | where: "type", "book" %}
      {% for resource in books %}
        <article class="resourceCard {% if resource.rating == 5 %}card-featured{% endif %} {% if resource.notes.size > 100 %}card-wide{% endif %}">
          <div class="resourceHeader">
            <h3 class="resourceName">
              {% if resource.url != "" %}
                <a href="{{ resource.url }}">{{ resource.name }}</a>
              {% else %}
                {{ resource.name }}
              {% endif %}
            </h3>
            {% if resource.rating > 0 %}
              <div class="resourceRating" aria-label="Rating: {{ resource.rating }} out of 5">
                {% for i in (1..5) %}
                  {% if i <= resource.rating %}
                    <i class="{{ rating-icon }}"></i>
                  {% else %}
                    <i style="color: var(--gray-600) " class="{{ rating-icon-sub }}"></i>
                  {% endif %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if resource.status %}
            <span class="resourceStatus status-{{ resource.status }}">{{ resource.status }}</span>
          {% endif %}
          {% if resource.notes != "" %}
            <p class="resourceNotes">{{ resource.notes }}</p>
          {% endif %}
          {% if resource.tags %}
            <div class="resourceTags">
              {% for tag in resource.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  </section>

## <i class="fa-solid fa-globe" aria-hidden="true"></i> Websites
{: #websites}

  <section class="resourceSection">
    <div class="resourceGrid">
      {% assign websites = resources | where: "type", "website" %}
      {% for resource in websites %}
        <article class="resourceCard {% if resource.rating == 5 %}card-featured{% endif %}">
          <div class="resourceHeader">
            <h3 class="resourceName">
              <a href="{{ resource.url }}">{{ resource.name }}</a>
            </h3>
            {% if resource.rating > 0 %}
              <div class="resourceRating" aria-label="Rating: {{ resource.rating }} out of 5">
                {% for i in (1..5) %}
                  {% if i <= resource.rating %}
                    <i class="{{ rating-icon }}"></i>
                  {% else %}
                    <i style="color: var(--gray-600) " class="{{ rating-icon-sub }}"></i>
                  {% endif %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if resource.status %}
            <span class="resourceStatus status-{{ resource.status }}">{{ resource.status }}</span>
          {% endif %}
          {% if resource.notes != "" %}
            <p class="resourceNotes">{{ resource.notes }}</p>
          {% endif %}
          {% if resource.tags %}
            <div class="resourceTags">
              {% for tag in resource.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  </section>

## <i class="fa-brands fa-youtube" aria-hidden="true"></i> YouTube Channels
{: #youtube}

  <section class="resourceSection">
    <div class="resourceGrid">
      {% assign youtube = resources | where: "type", "youtube" %}
      {% for resource in youtube %}
        <article class="resourceCard {% if resource.rating == 5 %}card-featured{% endif %} {% if resource.favoriteContent %}card-wide{% endif %}">
          <div class="resourceHeader">
            <h3 class="resourceName">
              <a href="{{ resource.url }}">{{ resource.name }}</a>
            </h3>
            {% if resource.rating > 0 %}
              <div class="resourceRating" aria-label="Rating: {{ resource.rating }} out of 5">
                {% for i in (1..5) %}
                  {% if i <= resource.rating %}
                    <i class="{{ rating-icon }}"></i>
                  {% else %}
                    <i style="color: --var(gray-600_" class="{{ rating-icon-sub }}"></i>
                  {% endif %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if resource.status %}
            <span class="resourceStatus status-{{ resource.status }}">{{ resource.status }}</span>
          {% endif %}
          {% if resource.notes != "" %}
            <p class="resourceNotes">{{ resource.notes }}</p>
          {% endif %}
          {% if resource.favoriteContent %}
            <p class="resourceFavorite"><strong>Favorites:</strong> {{ resource.favoriteContent }}</p>
          {% endif %}
          {% if resource.tags %}
            <div class="resourceTags">
              {% for tag in resource.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  </section>

## <i class="fa-brands fa-reddit" aria-hidden="true"></i> Subreddits
{: #reddit}

  <section class="resourceSection">
    <div class="resourceGrid resourceGrid-compact">
      {% assign reddit = resources | where: "type", "reddit" %}
      {% for resource in reddit %}
        <article class="resourceCard">
          <div class="resourceHeader">
            <h3 class="resourceName">
              <a href="{{ resource.url }}">{{ resource.name }}</a>
            </h3>
            {% if resource.rating > 0 %}
              <div class="resourceRating" aria-label="Rating: {{ resource.rating }} out of 5">
                {% for i in (1..5) %}
                  {% if i <= resource.rating %}
                    <i class="{{ rating-icon }}"></i>
                  {% else %}
                    <i style="color: var(--gray-600) " class="{{ rating-icon-sub }}"></i>
                  {% endif %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if resource.status %}
            <span class="resourceStatus status-{{ resource.status }}">{{ resource.status }}</span>
          {% endif %}
          {% if resource.notes != "" %}
            <p class="resourceNotes">{{ resource.notes }}</p>
          {% endif %}
          {% if resource.tags %}
            <div class="resourceTags">
              {% for tag in resource.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  </section>

## <i class="fa-solid fa-users" aria-hidden="true"></i> Lemmy Communities
{: #lemmy}

  <section class="resourceSection">
    <div class="resourceGrid resourceGrid-compact">
      {% assign lemmy = resources | where: "type", "lemmy" %}
      {% for resource in lemmy %}
        <article class="resourceCard">
          <div class="resourceHeader">
            <h3 class="resourceName">
              <a href="{{ resource.url }}">{{ resource.name }}</a>
            </h3>
            {% if resource.rating > 0 %}
              <div class="resourceRating" aria-label="Rating: {{ resource.rating }} out of 5">
                {% for i in (1..5) %}
                  {% if i <= resource.rating %}
                    <i class="{{ rating-icon }}"></i>
                  {% else %}
                    <i style="color: var(--gray-600) " class="{{ rating-icon-sub }}"></i>
                  {% endif %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if resource.status %}
            <span class="resourceStatus status-{{ resource.status }}">{{ resource.status }}</span>
          {% endif %}
          {% if resource.notes != "" %}
            <p class="resourceNotes">{{ resource.notes }}</p>
          {% endif %}
          {% if resource.tags %}
            <div class="resourceTags">
              {% for tag in resource.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  </section>

## <i class="fa-solid fa-seedling" aria-hidden="true"></i> Seed Banks
{: #seed-banks}

  <section class="resourceSection">
    <div class="resourceGrid">
      {% assign seedbanks = resources | where: "type", "seed-bank" %}
      {% for resource in seedbanks %}
        <article class="resourceCard {% if resource.rating == 5 %}card-featured{% endif %}">
          <div class="resourceHeader">
            <h3 class="resourceName">
              <a href="{{ resource.url }}">{{ resource.name }}</a>
            </h3>
            {% if resource.rating > 0 %}
              <div class="resourceRating" aria-label="Rating: {{ resource.rating }} out of 5">
                {% for i in (1..5) %}
                  {% if i <= resource.rating %}
                    <i class="{{ rating-icon }}"></i>
                  {% else %}
                    <i style="color: var(--gray-600) " class="{{ rating-icon-sub }}"></i>
                  {% endif %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if resource.status %}
            <span class="resourceStatus status-{{ resource.status }}">{{ resource.status }}</span>
          {% endif %}
          {% if resource.location %}
            <p class="resourceLocation"><i class="fa-solid fa-location-dot"></i> {{ resource.location }}</p>
          {% endif %}
          {% if resource.notes != "" %}
            <p class="resourceNotes">{{ resource.notes }}</p>
          {% endif %}
          {% if resource.tags %}
            <div class="resourceTags">
              {% for tag in resource.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  </section>

## <i class="fa-solid fa-dna" aria-hidden="true"></i> Breeders
{: #breeders}

  <section class="resourceSection">
    <div class="resourceGrid">
      {% assign breeders = resources | where: "type", "breeder" %}
      {% for resource in breeders %}
        <article class="resourceCard {% if resource.rating == 5 %}card-featured{% endif %}">
          <div class="resourceHeader">
            <h3 class="resourceName">
              <a href="{{ resource.url }}">{{ resource.name }}</a>
            </h3>
            {% if resource.rating > 0 %}
              <div class="resourceRating" aria-label="Rating: {{ resource.rating }} out of 5">
                {% for i in (1..5) %}
                  {% if i <= resource.rating %}
                    <i class="{{ rating-icon }}"></i>
                  {% else %}
                    <i style="color: var(--gray-600) " class="{{ rating-icon-sub }}"></i>
                  {% endif %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if resource.status %}
            <span class="resourceStatus status-{{ resource.status }}">{{ resource.status }}</span>
          {% endif %}
          {% if resource.notes != "" %}
            <p class="resourceNotes">{{ resource.notes }}</p>
          {% endif %}
          {% if resource.tags %}
            <div class="resourceTags">
              {% for tag in resource.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  </section>

## <i class="fa-solid fa-store" aria-hidden="true"></i> Chicago Grow Stores
{: #chicago-stores}

  <section class="resourceSection">
    <div class="resourceGrid">
      {% assign stores = resources | where: "type", "local-store" %}
      {% for resource in stores %}
        <article class="resourceCard {% if resource.status == 'closed' %}card-closed{% endif %}">
          <div class="resourceHeader">
            <h3 class="resourceName">
              {% if resource.url != "" %}
                <a href="{{ resource.url }}">{{ resource.name }}</a>
              {% else %}
                {{ resource.name }}
              {% endif %}
            </h3>
            {% if resource.rating > 0 %}
              <div class="resourceRating" aria-label="Rating: {{ resource.rating }} out of 5">
                {% for i in (1..5) %}
                  {% if i <= resource.rating %}
                    <i class="{{ rating-icon }}"></i>
                  {% else %}
                    <i style="color: var(--gray-600) " class="{{ rating-icon-sub }}"></i>
                  {% endif %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if resource.status %}
            <span class="resourceStatus status-{{ resource.status }}">{{ resource.status }}</span>
          {% endif %}
          {% if resource.location %}
            <p class="resourceLocation"><i class="fa-solid fa-location-dot"></i> {{ resource.location }}</p>
          {% endif %}
          {% if resource.notes != "" %}
            <p class="resourceNotes">{{ resource.notes }}</p>
          {% endif %}
          {% if resource.tags %}
            <div class="resourceTags">
              {% for tag in resource.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  </section>
