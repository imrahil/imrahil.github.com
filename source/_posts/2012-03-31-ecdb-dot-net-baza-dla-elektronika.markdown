---
layout: post
title: "ecdb.net - baza dla elektronika"
date: 2012-03-31 02:51
comments: true
categories: hardware DIY
---
<script type="text/javascript" src="{{ root_url }}/javascripts/jquery.js"></script>
<script type="text/javascript" src="{{ root_url }}/javascripts/jquery.lightbox.js"></script>

<link rel="stylesheet" type="text/css" href="/stylesheets/jquery.lightbox-0.5.css" media="screen" />

<script type="text/javascript">
jQuery.noConflict();

jQuery(function() {
    jQuery('a.lightbox').lightBox({
	imageLoading: '/images/lightbox-ico-loading.gif',
	imageBtnPrev: '/images/lightbox-btn-prev.gif',
	imageBtnNext: '/images/lightbox-btn-next.gif',
	imageBtnClose: '/images/lightbox-btn-close.gif',
	imageBlank: '/images/lightbox-blank.gif'
	});
});
</script>

Odkrycie ostatnich dni - serwis [ecdb.net](http://ecdb.net/login.php).

Wyśmienita baza danych dla posiadanych komponentów elektronicznych (które jak wiadomo lubią się przewalać byle gdzie i trudno je znaleźć :)

<a href="http://dl.dropbox.com/u/70162/ecdb/ecdb01.jpg" class="lightbox">{% img center http://dl.dropbox.com/u/70162/ecdb/ecdb01_small.jpg %}</a>

Dla każdego komponentu można podać: nazwę, komentarz, producenta, położenie w naszym biurku czy szafce, masę, link do noty katalogowej, zdjęcia, typ obudowy, cenę, wymiary, posiadaną ilość i ilość wymaganą do zamówienia.

<a href="http://dl.dropbox.com/u/70162/ecdb/ecdb02.jpg" class="lightbox">{% img center http://dl.dropbox.com/u/70162/ecdb/ecdb02_small.jpg %}</a>

Serwis umożliwia tworzenie projektów i dodawanie do nich komponentów z posiadanych zbiorów oraz list zakupowych (tzw BOM - Bill Of Material).

<a href="http://dl.dropbox.com/u/70162/ecdb/ecdb03.jpg" class="lightbox">{% img center http://dl.dropbox.com/u/70162/ecdb/ecdb03_small.jpg %}</a>

<a href="http://dl.dropbox.com/u/70162/ecdb/ecdb04.jpg" class="lightbox">{% img center http://dl.dropbox.com/u/70162/ecdb/ecdb04_small.jpg %}</a>

Dla niecierpliwych (takich jak ja) przygotowałem szybki skrypcik [Greasemonkey](http://www.greasespot.net/) pokazujący na czerwono brakują komponenty w wybranym projekcie - [link](https://gist.github.com/2043287) (widoczny powyżej)

Przydałby się też ewentualny import/export do zjadliwych formatów lub porządne API - nie ma nic lepszego niż aplikacja mobilna dla takiego serwisu :)

