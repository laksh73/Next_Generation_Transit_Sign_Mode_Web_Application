# Next Generation Sign Mode

A modern, standalone web application built with SvelteKit for displaying real-time transit information on public screens.

## Overview

Next Generation Sign Mode is a web application that lets transit agencies and businesses easily create public transit information displays. Building on the legacy of the original OneBusAway Sign Mode, this application provides a modernized, standalone solution for displaying real-time arrival information on large public screens.

## Features

- **Real-time arrival information** for public transit
- **Multi-stop support** for complex displays
- **Configurable through URL parameters** for easy setup
- **Responsive design** for various screen sizes
- **Theme customization** with light and dark modes
- **Advanced filtering** by route, time window, and more
- **Automatic refresh** at configurable intervals
- **Offline mode** for unstable network environments
- **Accessibility compliant** design
- **Configuration interface** for easy setup

## Quick Start

### Basic Usage

To display arrivals for a specific stop:
For example:
```
https://transit-display.example.org/sign/sign?stopIds=MTS_10772
```



### URL Parameters

| Parameter | Description | Example |
|-----------|-------------|---------|
| `stopIds` | Comma-separated list of stop IDs | `MTS_10772,MTS_11903` |
| `title` | Custom title for the display | `Downtown Transit Center` |
| `showTitle` | Show or hide the title section | `false` |
| `route` | Filter to specific route(s), can be repeated | `MTS_7` |
| `minutesBefore` | Hide departures older than N minutes | `5` |
| `minutesAfter` | Hide arrivals more than N minutes away | `60` |
| `refresh` | Auto-refresh interval in seconds | `30` |
| `darkMode` | Enable dark theme | `true` |
| `fontSize` | Base font size for display | `large` |


## Configuration Interface

This interface allows you to:
- Select stops from a map
- Choose routes to display
- Set display options
- Generate a URL for your sign
- Create a QR code for easy deployment

## Technical Architecture

Next Generation Sign Mode is built with:

- **SvelteKit** - A modern framework for building web applications
- **TypeScript** - For type safety and code clarity
- **OneBusAway API** - For real-time transit data
- **Vite** - For fast builds and development
- **Vitest** - For comprehensive testing

### Project Structure

```
src/
├── lib/
│   ├── components/      # UI components
│   ├── stores/          # Svelte stores for state management
│   ├── api/             # API client for OneBusAway
│   ├── utils/           # Utility functions
│   └── types/           # TypeScript type definitions
├── routes/              # SvelteKit routes
├── static/              # Static assets
└── app.html             # HTML template
```


## Acknowledgments

This project is part of the Open Transit Software Foundation ecosystem and builds upon the work of OneBusAway and other transit information systems.
