---
layout: post
title: "Błąd w Adobe AIR 3.1 dla iOS"
date: 2011-12-09 10:35
comments: true
categories: adobe air ios
---
Jeśli po instalacji aplikacji Adobe AIR dla iOS nazwa aplikacji jest skopana to znaczy, że macie do czynienia z [błędem 3052344](https://bugbase.adobe.com/index.cfm?event=bug&id=3052344).  
Konkretnie chodzi o to, że nazwa aplikacji wyświetlana w menu brana jest z application-app.xml z pola:
    <filename>Filename</filename>
a nie z pola:
    <name>Appname</name>
    
Rozwiązaniem jest wypakowanie z pliku IPA konfiguracji w __info.plist__, zmiana pola:
    <key>CFBundleDisplayName</key>
    <string>Filename</string>
na:
    <key>CFBundleDisplayName</key>
    <string>Appname</string>
i wpakowanie tego pliku z powrotem do IPA.
