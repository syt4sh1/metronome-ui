# metronome-ui
## Installation
To install the package, use npm:

`npm install metronome-ui tone`
## Usage
### Basic Usage
You can use the metronome UI in your HTML and JavaScript files as follows:

Include the required HTML elements:
```
<!-- Add these elements to your HTML -->
<div id="metronome-ui">
  <button id="start-button">Start</button>
  <input type="number" id="tempo-input" value="120" />
  <select id="beat-dropdown">
    <option value="4">4/4</option>
    <option value="3">3/4</option>
    <option value="6">6/8</option>
  </select>
  <div id="tick-indicator"></div>
</div>
```
Import and set up the metronome UI in your JavaScript:

```
import Metronome from 'your-metronome-package';
import Tone from 'tone';
const metronome = new Metronome();
Tone.Transport.start();
// Rest of your code (event listeners, metronome hooks, etc.)
```
## Advanced Configuration
You can customize the behavior of the metronome UI further by exploring the API and event hooks. Refer to the API Reference section for more details.

## API Reference
`Metronome Class`
The Metronome class provides methods to control and customize the metronome UI.

`new Metronome()`
Creates a new instance of the metronome.

`metronome.start(tempo, beatsPerBar)`
Starts the metronome with the specified tempo (beats per minute) and beatsPerBar.

`metronome.stop()`
Stops the metronome.

`metronome.setTempo(tempo)`
Changes the tempo of the metronome.

`metronome.setBeatsPerBar(beatsPerBar)`
Changes the number of beats per bar.

## Events
The metronome emits various events that you can hook into.  
`tick` Event
Emitted on each metronome tick.
```
metronome.on('tick', (currentTick) => {
  // Your code here
});
```
