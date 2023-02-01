---
layout: default
title: About
members: [
  {
    name    : "Anusha",
    picture : "https://pbs.twimg.com/profile_images/1423444246971908096/HzpAoez7_400x400.jpg",
    link    : "https://twitter.com/0xh3110ca",
    role    : "President (Current)",
    order   : 0,
    current    : True,
  },
  {
    name    : "Nathan",
    picture : "https://media.licdn.com/dms/image/C5603AQFRw-xI5sLWYw/profile-displayphoto-shrink_800_800/0/1662006829381?e=1677110400&v=beta&t=nmV0nz_cf0lW3Yc2c6l4AP4kBhQ0e4UCN3sKKaMfJQU",
    link    : "https://github.com/nathanfarlow",
    role    : "Former President (FA 2022)",
    order   : 1,
    current    : False,
  },
  {
    name    : "Thomas",
    picture : "https://quig.dev/cdn/photos/glitch-crop.gif",
    link    : "https://quig.dev/",
    role    : "Former President (2020-2022)",
    order   : 2,
    current    : False,
  },
  {
    name    : "ravi",
    picture : "https://avatars.githubusercontent.com/u/36464332",
    link    : "https://github.com/jprx",
    role    : "Former President (2019-2020)",
    order   : 3,
    current    : False,
  },
  {
    name    : "Ian",
    picture : "https://klatz.co/images/arrow.png",
    link    : "https://klatz.co",
    role    : "Former President (2018-2019)",
    order   : 4,
    current    : False,
  },
  {
    name    : "Nicholas",
    picture : "https://nicholas.sh/profile.jpg",
    link    : "https://nicholas.sh",
    role    : "Officer",
    order   : 5,
    current    : True,
  },
  {
    name    : "kuilin",
    picture : "https://kuilin.net/profile_upscaled.png",
    link    : "https://kuilin.net",
    role    : "Infra Admin",
    order   : 6,
    current    : False,
  },
  {
    name    : "Husnain",
    picture : "https://avatars.githubusercontent.com/u/12467423",
    link    : "https://github.com/epistemologist",
    role    : "Officer",
    order   : 7,
    current    : True,
  }
]
---

<div class="container mb-5">
  <div class="row">
    <div class="col panel mt-5">
      <div class="embedded-image">
        <img src="{{ site.baseurl }}/images/logo.png" class="rounded" height="350" width="300"/>
      </div>

      <br>
      <hr/>

	  <p>
	  SIGPwny is a friendly, elite club from UIUC focused on cybersecurity.
	  We host weekly learning meetings, participate in CTFs as a group, and
	  do cutting-edge cybersecurity research.
	  </p>

      <p>
        SIGPwny is canonically spelled SIGPwny, but some alumni might remember it as SIGPony.
        The club was originally named SIGMil, which was founded around
		2002, and reborn as SIGPwny around 2011.
      </p>

    </div>
  </div>

  <div class="col panel mt-5">
    <h2 class="my-5 header"> Our Members </h2>
    <hr/>
    <div class="row d-flex justify-content-center">
    {% assign groups = page.members | group_by: "order" | sort: "name" %}
    {% for group in groups %}
      {% assign members = group.items | sort: "name" %}
      {% for member in members %}
        <div class="card m-3">
          <a href="{{ member.link }}">
            <div class="member-image">
              <img src="{{ member.picture }}" class="rounded-circle my-3" height="150" width="150"/>
              <h4 class="mx-3">{{ member.name }}</h4>
              <p class="mx-3">{{ member.role }}</p>
            </div>
          </a>
        </div>
      {% endfor %}
    {% endfor %}
    </div>
    <h2 class="my-5 header"> and 500+ more! </h2>
  </div>
</div>

