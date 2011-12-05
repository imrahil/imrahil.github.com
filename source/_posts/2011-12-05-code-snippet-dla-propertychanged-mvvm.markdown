---
layout: post
title: "Code snippet dla PropertyChanged (MVVM)"
date: 2011-12-05 00:58
comments: true
categories: wp7 mvvm code_snippets
---
Zajmuję się ostatnio poznawaniem programowania dla [Windows Phone 7.5](http://msdn.microsoft.com/pl-pl/ff380145). Dość poważnym problemem było dla mnie zrozumienie jak działa bindowanie (bardzo prosta rzecz we Flexie) i jak włączyć aktualizację danych z modelu w widoku.  
Po chwili googlania znalazłem bardzo dobry tutorial na stronach [bazy wiedzy Codeguru](http://www.codeguru.pl/baza-wiedzy/wp7-dla-programistow-czesc-3---data-binding-i-mvvm,1836).  
Można się z niego dowiedzieć, że rozwiązaniem tego problemu jest implementacja interfejsu __INotifyPropertyChanged__ dla każdego modelu (lub ViewModelu - ale to kwestia na osobny post).  
Wspomniana implementacja wygląda mniej więcej tak:
    public event PropertyChangedEventHandler PropertyChanged;

    protected void OnPropertyChanged(string propertyName)
    {
        if (PropertyChanged != null)
        {
            PropertyChanged(this,
                new PropertyChangedEventArgs(propertyName));
        }
    }

W efekcie czego wystarczy dla każdej zmiennej w obiekcie dać takie gettery i settery:
    private int myField;

    public int MyProperty
    {
        get
        {
            return this.myField;
        }

        set
        {
            if (this.myField != value)
            {
                this.myField = value;
                this.OnPropertyChanged("MyProperty");
            }
        }
    }

Problem pojawia się w momencie gdy trzeba stworzyć dużo zmiennych do modelu, albo skonwertować obiekt z AS3 (tak jak w moim przypadku). Wtedy z pomocą przychodzą snippety stworzone przez [Mariano Omar Rodriguez](http://weblogs.asp.net/marianor/archive/2009/08/17/c-code-snippets-for-properties-raising-propertychanged-event.aspx). Tworzą one kod identyczny z tym podanym wcześniej.  
Na wszelki wypadek lokalna kopia do ściągnięcia [tutaj](/upload/PropertyChangedSnippets.zip).

W Visual Studio 2010 snippety dostępne są pod skrótami: __propnpc__ oraz __onpc__.
(czyli wpisujemy __propnpc__, naciskamy Tab dwa razy i wpisujemy nazwę zmiennej :)
