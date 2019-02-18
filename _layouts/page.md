<!DOCTYPE html>
<html lang="{{ site.lang | default: "en-US" }}">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    {% comment %}Favicons{% endcomment %}
    <link
      href="{{ "/assets/img/favicon-apple-touch-114.png" | relative_url }}"
      rel="apple-touch-icon-precomposed"
      sizes="114x114" href="favicon-apple-touch-114.png">
    <link
      href="{{ "/assets/img/favicon-apple-touch-144.png" | relative_url }}"
      rel="apple-touch-icon-precomposed"
      sizes="144x144" href="favicon-apple-touch-144.png">
    <link
      href="/favicon.ico"
      rel="icon"
      sizes="32x32 48x48"
      type="image/vnd.microsoft.icon">
    <link href="/favicon.icns" rel="icon" sizes="128x128">
    <link href="/favicon.png" rel="icon" type="image/x-icon">

    {% seo %}

    <link rel="stylesheet" href="{{ "/assets/css/style.css?v=" | append: site.time | relative_url }}">

    {% comment %} Font Awesome for Social Media Icons {% endcomment %}
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.1/css/all.css" integrity="sha384-fnmOCqbTlWIlj8LyTjo7mOUStjsKC4pOpQbqyi7RrhN7udi9RwhKkMHpvLbHG9Sr" crossorigin="anonymous">

    <!--[if lt IE 9]>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv.min.js"></script>
    <![endif]-->
  </head>
  <body>
    <div class="wrapper">
      <header>
        <strong><a href="{{ "/" | absolute_url }}">{{ site.title }}</a></strong>

        {% if site.logo %}
          <img src="{{site.logo | relative_url}}" alt="Logo" />
        {% endif %}

        <p>{{ site.description }}</p>

        <div class="social-links">
          {% if site.facebook_username %}
            <a href="https://www.facebook.com/{{ site.facebook_username }}" title="Facebook">
              <i class="fab fa-facebook-square"></i>
            </a>
          {% endif %}
          {% if site.github_username %}
            <a href="https://github.com/{{ site.github_username }}" title="GitHub">
              <i class="fab fa-github"></i>
            </a>
          {% endif %}
          {% if site.linked_username %}
            <a href="https://linkedin.com/in/{{ site.linked_username }}" title="LinkedIn">
              <i class="fab fa-linkedin"></i>
            </a>
          {% endif %}
          {% if site.twitter_username %}
            <a href="https://twitter.com/{{ site.twitter_username }}" title="Twitter">
              <i class="fab fa-twitter-square"></i>
            </a>
          {% endif %}
          {% if site.angellist_username %}
            <a href="https://angel.co/{{ site.angellist_username }}" title="Angel List">
              <i class="fab fa-angellist"></i>
            </a>
          {% endif %}
        </div>
      </header>
      <div class="content">
        <section>
          {{ content }}
        </section>
        <footer>
          <small>&copy; 2019 David Dripps. All rights reserved.</small>
        </footer>
      </div>
    </div>
    <script src="{{ "/assets/js/scale.fix.js" | relative_url }}"></script>
    {% if site.google_analytics %}
    <script>
      (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
      (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
      m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
      })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');
      ga('create', '{{ site.google_analytics }}', 'auto');
      ga('send', 'pageview');
    </script>
    {% endif %}
  </body>
</html>
