![Logo](admin/vis-2-widgets-jaeger-design.png)
# Special Jaeger Design widgets for ioBroker.vis 2.0

![Number of Installations](http://iobroker.live/badges/vis-2-widgets-jaeger-design-installed.svg) ![Number of Installations](http://iobroker.live/badges/vis-2-widgets-jaeger-design-stable.svg) [![NPM version](http://img.shields.io/npm/v/iobroker.vis-2-widgets-jaeger-design.svg)](https://www.npmjs.com/package/iobroker.vis-2-widgets-jaeger-design)
[![Downloads](https://img.shields.io/npm/dm/iobroker.vis-2-widgets-jaeger-design.svg)](https://www.npmjs.com/package/iobroker.vis-2-widgets-jaeger-design)

[![NPM](https://nodei.co/npm/iobroker.vis-2-widgets-jaeger-design.png?downloads=true)](https://nodei.co/npm/iobroker.vis-2-widgets-jaeger-design/)

### English:

## ioBroker.vis-2-widgets-jaeger-design Adapter

With the new visualization of the `ioBroker.vis-2-widgets-jaeger-design` adapter, anyone can easily and simply create a beautiful and user-friendly interface for their Smart Home in ioBroker. Here's a brief guide to get you started.

### Getting Started

1. **Install the Adapter**:
   - Open your ioBroker admin UI.
   - Go to the "Adapters" section.
   - Search for `ioBroker.vis-2-widgets-jaeger-design`.
   - Click on the install button to add the adapter to your system.

2. **Using the Adapter in VIS 2**:
   - After installation, open the VIS 2 editor.
   - You will find new widgets associated with the `jaeger-design` adapter in the widget library.
   - Drag and drop these widgets as needed to create your desired dashboard interface.

### Learning Resources

To assist you in using these new features, we have compiled a series of YouTube videos. The videos are divided into:
1. **Demonstrations**: Showcasing what is possible with the adapter.
2. **Tutorials**: Step-by-step guides on how to use the adapter.

The video list is continuously updated, so make sure to check back for new content. 

[Link zur YouTube-Playlist](https://www.youtube.com/playlist?list=PLddhldeLVrtl5Bhj6AAbkLabuIuyV0bVe)

### Deutsch:

## ioBroker.vis-2-widgets-jaeger-design Adapter

Mit der neuen Visualisierung des `ioBroker.vis-2-widgets-jaeger-design` Adapters, kann jeder einfach und unkompliziert eine schön aussehende Oberfläche mit einer hohen Benutzerfreundlichkeit für sein Smart Home in ioBroker umsetzen. Hier ist eine kurze Anleitung, um loszulegen.

### Erste Schritte

1. **Adapter installieren**:
   - Öffnen Sie Ihr ioBroker-Admin-UI.
   - Gehen Sie zum Bereich "Adapter".
   - Suchen Sie nach `ioBroker.vis-2-widgets-jaeger-design`.
   - Klicken Sie auf die Installationsschaltfläche, um den Adapter in Ihrem System hinzuzufügen.

2. **Den Adapter in VIS 2 verwenden**:
   - Nach der Installation öffnen Sie den VIS 2-Editor.
   - In der Widget-Bibliothek finden Sie die neuen Widgets des `jaeger-design` Adapters.
   - Ziehen Sie diese Widgets nach Bedarf in Ihre Oberfläche, um Ihr gewünschtes Dashboard zu erstellen.

### Lernressourcen

Um Ihnen die Nutzung der neuen Funktionen zu erleichtern, haben wir eine Reihe von YouTube-Videos zusammengestellt. Die Videos sind unterteilt in:
1. **Demonstrationen**: Zeigt, was mit dem Adapter möglich ist.
2. **Tutorials**: Schritt-für-Schritt-Anleitungen zur Verwendung des Adapters.

Die Videoliste wird kontinuierlich erweitert, schauen Sie daher regelmäßig vorbei, um neue Inhalte zu entdecken.

[Link zur YouTube-Playlist](https://www.youtube.com/playlist?list=PLddhldeLVrtl5Bhj6AAbkLabuIuyV0bVe)



![youtube](img/youtube.png)

You can find the video how to use the widgets [here](https://www.youtube.com/watch?v=4bctUvfpPuQ) (in german).

Das Video wie man die Widgets benutzt kann man [hier](https://www.youtube.com/watch?v=4bctUvfpPuQ) finden.

## Widgets
### Buttons and switches

### Actual news
![Actual news ](img/news.png)

To use this widget, you need to create a small script in Javascript adapter:
```
const axios = require('axios');

function readRss() {
    axios('https://www.n-tv.de/rss')
        .then(resp => setState('javascript.0.rss', resp.data.toString(), true));
}

createState('javascript.0.rss', {type: 'string'}, () => {
    setInterval(() => readRss(), 60000 * 60 * 2); // update rss every 2 hours
    readRss();
});
```

And then use `javascript.0.rss` object in this widget.

<!--
    Placeholder for the next version (at the beginning of the line):
    ### **WORK IN PROGRESS**
-->
## Changelog
### 1.2.4 (2024-07-10)
* (bluefox) Added possibility to control other IDs with memory buttons (Dimmer, Shutter)
* (bluefox) Added the power option for thermostat
* (bluefox) Implemented the writing of specific values for state widget

### 1.2.1 (2024-07-07)
* (bluefox) Removed withStyles usage
* (bluefox) Added confirmation dialog

### 1.1.27 (2024-05-27)
* (bluefox) Added descriptions

### 1.1.26 (2024-05-23)
* (bluefox) Corrected font-size of thermostat

### 1.1.22 (2024-05-14)
* (bluefox) Added possibility to show a simple state without a border
* (bluefox) Added possibility to add a caption for some widgets

### 1.1.21 (2024-05-01)
* (bluefox) Changed layout for mobile view

### 1.1.20 (2024-04-09)
* (bluefox) Allowed changing font size for thermostat

### 1.1.19 (2024-03-12)
* (bluefox) Allowed changing the palette for every widget

### 1.1.15 (2024-03-06)
* (bluefox) Improved dimmer widget

### 1.1.14 (2024-02-21)
* (bluefox) Added top info in the mobile view

### 1.1.12 (2024-02-20)
* (bluefox) Corrected some layout issues

### 1.1.10 (2024-01-19)
* (bluefox) Small changes on layout and added new distance settings

### 1.1.8 (2024-01-18)
* (bluefox) Corrected info button in mobile view

### 1.1.5 (2023-12-05)
* (bluefox) Added an option to start action or scene from new line

### 1.1.0 (2023-11-29)
* (bluefox) Corrected license check
* (bluefox) Added class names to all important layout components

### 1.0.12 (2023-11-22)
* (bluefox) Allowed reordering of the actions and scenes
* (bluefox) Added a new option to show scenes before actions
* (bluefox) Added option to show value in dimmer
* (bluefox) Added option for adjustable width of the right view on the home page
* (bluefox) Added option to provide icons for scenes and actions
* (bluefox) Added option set the distance between menu items
* (bluefox) Added possibility to set control value for scenes
* (bluefox) Added possibility to adjust font size for scenes and actions

### 1.0.11 (2023-11-10)
* (bluefox) Corrected error local variables and controls

### 1.0.10 (2023-11-08)
* (bluefox) Corrected error with scenes
* (bluefox) Improved state widget with custom icons

### 1.0.9 (2023-11-07)
* (bluefox) Allowed setting distance between actions and scenes on the home page

### 1.0.8 (2023-11-06)
* (bluefox) Corrected the cameras widget

### 1.0.7 (2023-10-31)
* (bluefox) Added possibility to reorder info on status bar

### 1.0.5 (2023-10-17)
* (bluefox) Corrected error with fakeView

### 1.0.4 (2023-10-10)
* (bluefox) Corrected layout of thermostat

### 1.0.3 (2023-10-10)
* (bluefox) Corrected error if shutter was inverted

### 1.0.2 (2023-09-28)
* (bluefox) Corrected touch behavior for dimmer and shutter

### 1.0.1 (2023-09-26)
* (bluefox) Corrected small issues

### 1.0.0 (2023-08-11)
* (bluefox) Changed style of shutter and state widgets

### 0.6.5 (2023-08-09)
* (bluefox) Corrected view selector and empty menu item

### 0.6.4 (2023-07-31)
* (bluefox) Set constant width and height of thermostat icons

### 0.6.3 (2023-07-25)
* (bluefox) Added many new features

### 0.6.1 (2023-07-21)
* (bluefox) Added max height/width for floors

### 0.6.0 (2023-07-19)
* (bluefox) Corrected some errors with information

### 0.5.2 (2023-07-02)
* (bluefox) Support of false for scenes

### 0.5.0 (2023-06-28)
* (bluefox) Added support for the new vis
* (bluefox) Added page configurable margins

### 0.4.6 (2023-06-19)
* (bluefox) Corrected sub menu

### 0.4.5 (2023-06-13)
* (bluefox) Corrected visualization of view

### 0.4.0 (2023-05-31)
* (bluefox) Added exclusions
* (bluefox) Added possibility to show information on the very top of layout

### 0.3.2 (2023-04-05)
* (bluefox) Corrected license problem

### 0.3.1 (2023-03-22)
* (bluefox) Corrected build process

### 0.3.0 (2023-03-21)
* (bluefox) Implemented dark mode

### 0.2.3 (2023-03-09)
* (bluefox) update packages

### 0.2.2 (2023-03-06)
* (bluefox) Updated thermostat widget

### 0.2.1 (2023-02-03)
* (bluefox) Mobile views tuned

### 0.2.0 (2023-02-01)
* (bluefox) implemented mobile view

### 0.1.3 (2023-01-30)
* (bluefox) initial commit

## License
Copyright (c) 2022-2024 bluefox <dogafox@gmail.com>
All rights reserved.
