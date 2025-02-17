<!DOCTYPE html>
<html>
<head>
<title>Exact Slider Replicas</title>
<style>
  .slider-container {
    width: 400px; /* Increased width */
    position: relative;
    margin: 30px auto; /* Centered and increased spacing */
  }

  .slider-track {
    height: 4px; /* Reduced height */
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    left: 0;
    right: 0;
    border-radius: 2px;
  }

  .slider-thumb {
    width: 16px; /* Reduced size */
    height: 16px; /* Reduced size */
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    cursor: grab;
    z-index: 2;
    border: none;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.2);
  }

  .slider-thumb:active {
    cursor: grabbing;
  }

  .slider-value {
    position: absolute;
    top: -20px; /* Adjusted position */
    left: 50%;
    transform: translateX(-50%);
    font-size: 11px; /* Reduced size */
    color: #555;
  }

  .slider-ticks {
    position: absolute;
    top: 15px;
    left: 0;
    right: 0;
    display: flex;
    justify-content: space-between;
    pointer-events: none;
  }

  .slider-tick {
    width: 1px;
    height: 6px; /* Reduced height */
    background-color: #bbb;
  }

  /* Track 1: Green to Pink */
  .slider-container:nth-child(1) .slider-track {
    background: linear-gradient(to right,
      green 50%, /* Green up to 50% */
      lightgreen 50% 70%,  /* Light green from 50% to 70% */
      pink 70%
    );  /* Pink from 70% onwards */
  }

  .slider-container:nth-child(1) .slider-thumb {
    background-color: green;
  }

  /* Track 2: Divisor Style */
  .slider-container:nth-child(2) .slider-track {
    background: linear-gradient(to right,
      #336699 20%,  /* Solid blue up to 20% */
      rgba(51, 102, 153, 0.3) 20%
    );  /* Faded blue afterwards */
  }

  .slider-container:nth-child(2) .slider-thumb {
    background-color: #336699;
  }

  .slider-container:nth-child(2) .slider-ticks {
    top: 5px;
  }

  .slider-container:nth-child(2) .slider-ticks .slider-tick {
    width: 3px;
    height: 3px;
    background-color: #336699;
    border-radius: 50%;
  }

  /* Track 3: Thumb Style */
  .slider-container:nth-child(3) .slider-track {
    background: linear-gradient(to right,
      #cc6666 80%, /* Solid red up to 80% */
      rgba(204, 102, 102, 0.3) 80%
    );
  }

  .slider-container:nth-child(3) .slider-thumb {
      width: 0;
      height: 0;
      border-left: 8px solid transparent;
      border-right: 8px solid transparent;
      border-bottom: 16px solid #cc6666; /* Darker red */
      border-radius: 0; /* Remove circle */
      transform: translateX(-50%) translateY(-75%); /* Adjust position */
  }

  .slider-container:nth-child(3) .slider-ticks {
    top: 5px;
  }

  .slider-container:nth-child(3) .slider-ticks .slider-tick {
    width: 3px;
    height: 3px;
    border-radius: 50%;
    background-color: #cc6666;
  }

  /* Track 4: Tick Style */
  .slider-container:nth-child(4) .slider-track {
    background-color: #66b3ff;
  }

  .slider-container:nth-child(4) .slider-thumb {
    background-color: #3385ff;
  }

  /* Labels */
  .slider-label {
    position: absolute;
    top: -25px;
    left: 0;
    font-size: 12px;
    color: #777;
    font-weight: bold;
  }

  .slider-container:nth-child(1) .slider-label {color: green;}
  .slider-container:nth-child(2) .slider-label {color: #336699;}
  .slider-container:nth-child(3) .slider-label {color: #cc6666;}
  .slider-container:nth-child(4) .slider-label {color: #3385ff;}

</style>
</head>
<body>

<div class="slider-container">
  <span class="slider-label">Track</span>
  <div class="slider-track"></div>
  <div class="slider-thumb">
    <div class="slider-value">60</div>
  </div>
</div>

<div class="slider-container">
  <span class="slider-label"></span>
  <div class="slider-track"></div>
  <div class="slider-thumb">
    <div class="slider-value">60</div>
  </div>
  <div class="slider-ticks"></div>
</div>

<div class="slider-container">
  <span class="slider-label"></span>
  <div class="slider-track"></div>
  <div class="slider-thumb">
    <div class="slider-value">60</div>
  </div>
  <div class="slider-ticks"></div>
</div>

<div class="slider-container">
  <span class="slider-label"></span>
  <div class="slider-track"></div>
  <div class="slider-thumb">
    <div class="slider-value">60</div>
  </div>
  <div class="slider-ticks"></div>
</div>


<script>
  const sliderContainers = document.querySelectorAll('.slider-container');

  sliderContainers.forEach((sliderContainer, index) => {
    const sliderTrack = sliderContainer.querySelector('.slider-track');
    const sliderThumb = sliderContainer.querySelector('.slider-thumb');
    const sliderValue = sliderContainer.querySelector('.slider-value');
    const sliderTicksContainer = sliderContainer.querySelector('.slider-ticks');

    const minValue = 0;
    const maxValue = 100;
    let currentValue = 60; /* Changed to 60 initial value */
    let isDragging = false;

    // Initialize Ticks (if the container has them)
    if (sliderTicksContainer) {
      const numTicks = 20;
      for (let i = 0; i < numTicks; i++) {
        const tick = document.createElement('div');
        tick.classList.add('slider-tick');
        sliderTicksContainer.appendChild(tick);
      }
    }

    // Set initial thumb position
    updateThumbPosition();

    sliderThumb.addEventListener('mousedown', (e) => {
      isDragging = true;
      document.addEventListener('mousemove', handleMouseMove);
      document.addEventListener('mouseup', handleMouseUp);
      e.preventDefault(); // Prevent text selection while dragging
    });

    function handleMouseMove(e) {
      if (!isDragging) return;

      const trackRect = sliderTrack.getBoundingClientRect();
      let x = e.clientX - trackRect.left;

      // Clamp the x position to the track bounds
      x = Math.max(0, Math.min(x, trackRect.width));

      // Calculate the new value based on the position
      currentValue = (x / trackRect.width) * (maxValue - minValue) + minValue;
      currentValue = Math.round(currentValue); // Round to nearest integer

      // Update the thumb position and value display
      updateThumbPosition();
    }

    function handleMouseUp() {
      isDragging = false;
      document.removeEventListener('mousemove', handleMouseMove);
      document.removeEventListener('mouseup', handleMouseUp);
    }

    function updateThumbPosition() {
      const percentage = (currentValue - minValue) / (maxValue - minValue);
      const trackWidth = sliderTrack.offsetWidth;
      const thumbPosition = percentage * trackWidth;

      sliderThumb.style.left = `${thumbPosition}px`;
      sliderValue.textContent = currentValue;
    }

    // Touch Support (Optional)
    sliderThumb.addEventListener('touchstart', (e) => {
      isDragging = true;
      document.addEventListener('touchmove', handleTouchMove);
      document.addEventListener('touchend', handleMouseUp);
      e.preventDefault();
    });

    function handleTouchMove(e) {
      if (!isDragging) return;

      const trackRect = sliderTrack.getBoundingClientRect();
      let x = e.touches[0].clientX - trackRect.left;

      // Clamp the x position to the track bounds
      x = Math.max(0, Math.min(x, trackRect.width));

      // Calculate the new value based on the position
      currentValue = (x / trackRect.width) * (maxValue - minValue) + minValue;
      currentValue = Math.round(currentValue); // Round to nearest integer

      // Update the thumb position and value display
      updateThumbPosition();
    }
  });


</script>

</body>
</html>
