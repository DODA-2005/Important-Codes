1. "Playback Speed On Youtube" -  
  document.getElementsByTagName("video")[0].playbackRate =x
2. "Fix Sound on a video" - 

var videoElement = document.querySelector("video")
var audioCtx = new AudioContext()
var source = audioCtx.createMediaElementSource(videoElement)
var gainNode = audioCtx.createGain()
gainNode.gain.value = 2 // double the volume
source.connect(gainNode)
gainNode.connect(audioCtx.destination)

gainNode.gain.value = x
