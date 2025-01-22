# Audix 🎶

**Audix** is a powerful and flexible audio management library for the web. Built with **Web Audio API** and **TypeScript**, `Audix` gives you full control over audio playback, multi-track management, and audio effects. Perfect for modern web applications that need precise and efficient audio handling. 🚀

---

## Key Features 🌟

- **Play, Pause, and Resume**: Full control over audio playback with seamless pause and resume.
- **Multi-Track Management**: Play and manage multiple audio files simultaneously.
- **Seek to Position**: Jump to any specific point in the audio.
- **Volume Control**: Dynamically adjust the volume of any audio.
- **Event Handling**: Listen to play, pause, end, and error events.
- **Optimized Performance**: Built on **Web Audio API** for high performance and low resource usage.

---

## Installation 📦

Install `Audix` via **npm**:

```bash
npm install audix
```

Or include it directly in your web project via **CDN**:

```html
<script src="https://cdn.jsdelivr.net/npm/audix/dist/audix.min.js"></script>
```

---

## Quick Start 🚀

### 1. Create an Instance of `Audix`

```typescript
import Audix from 'audix';

const audix = new Audix();
```

### 2. Load and Play Audio

```typescript
// Load an audio file
await audix.load('background', 'path/to/background.mp3');

// Play the audio
audix.play('background', true); // Loop the audio
```

### 3. Control Audio Playback

```typescript
// Pause the audio
audix.pause('background');

// Resume playback from where it left off
audix.play('background');

// Seek to a specific position
audix.seek('background', 30); // Jump to 30 seconds

// Adjust volume
audix.setVolume('background', 0.5); // Set volume to 50%
```

### 4. Handle Events

```typescript
// Add an event listener
audix.on('play', 'background', () => {
  console.log('Audio playback started!');
});

// Remove an event listener
audix.off('play', 'background', callbackFunction);
```

---

## Documentation 📚

### Methods

- **`load(name: string, url: string): Promise<void>`**: Load an audio file.
- **`play(name: string, loop?: boolean, startTime?: number): void`**: Play the audio.
- **`pause(name: string): void`**: Pause the audio.
- **`stop(name: string): void`**: Stop the audio completely.
- **`seek(name: string, time: number): void`**: Seek to a specific time in the audio.
- **`setVolume(name: string, volume: number): void`**: Adjust the volume of the audio.
- **`getCurrentTime(name: string): number`**: Get the current playback time.
- **`on(event: AudioEvent, name: string, listener: () => void): void`**: Add an event listener.
- **`off(event: AudioEvent, name: string, listener: () => void): void`**: Remove an event listener.
- **`dispose(): void`**: Clean up resources and stop all audio.

---

## Examples 🎨

### Playing Multiple Audio Files Simultaneously

```typescript
await audix.load('background', 'path/to/background.mp3');
await audix.load('effect', 'path/to/effect.mp3');

audix.play('background', true); // Loop background music
audix.play('effect'); // Play sound effect
```

### Handling Events

```typescript
audix.on('play', 'background', () => {
  console.log('Background music started playing!');
});

audix.on('end', 'effect', () => {
  console.log('Sound effect finished playing!');
});
```

---

## Contributing 🤝

We welcome contributions! Here's how you can get started:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/YourFeatureName`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature/YourFeatureName`.
5. Open a Pull Request.

---

## License 📜

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## Support ❤️

If you love `Audix`, show your support by giving us a star (⭐) on GitHub!

---

Crafted with ❤️ by [Your Name](https://github.com/peymanprd)  
**Audix** - Audio management for the web, made simple and powerful! 🎧

---

This README is designed to make your project stand out and provide all the necessary information for users and contributors. Let me know if you need further tweaks! 😊
