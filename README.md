# CanvasRecorder

Record a canvas to webm video without effecting rendering performance.

## How to use

Create a recorder

```javascript
const canvas = document.getElementById('animation');
const recorder = new CanvasRecorder(canvas);
```

```javascript
// optional: bits per second for video quality, defaults to 2.5Mbps
const recorder = new CanvasRecorder(canvas, 4500000);
```

Start recording
```javascript
recorder.start();
```

Stop recording
```javascript
recorder.stop();
```

Save/download recording
```javascript
recorder.save();

// Save with given file name
recorder.save('busy_motion.webm');
```

## How it works

It is based on this [WebRTC sample](https://webrtc.github.io/samples/src/content/capture/canvas-record/). Captures [`MediaStream`](https://developer.mozilla.org/en-US/docs/Web/API/MediaStream_Recording_API) from a canvas element and records it with [`MediaRecorder`](https://developer.mozilla.org/en-US/docs/Web/API/MediaRecorder).
