@tailwind base;
@tailwind components;
@tailwind utilities;

@keyframes float {
  0% {
    transform: translateY(0px) rotateY(0deg) scale(1);
  }
  50% {
    transform: translateY(-20px) rotateY(180deg) scale(1.05);
  }
  100% {
    transform: translateY(0px) rotateY(360deg) scale(1);
  }
}

.hero-text {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeUp 1.2s cubic-bezier(0.23, 1, 0.32, 1) forwards;
}

@keyframes fadeUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.parallax-section {
  transform-style: preserve-3d;
  perspective: 2000px;
}

.parallax-section::after {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(to bottom, transparent, rgba(0,0,0,0.8));
  pointer-events: none;
  transition: opacity 0.5s ease;
}

.product-card {
  transition: all 0.8s cubic-bezier(0.23, 1, 0.32, 1);
  transform-style: preserve-3d;
  perspective: 1000px;
}

.product-card:hover {
  transform: translateY(-20px) rotateX(10deg) rotateY(10deg);
  box-shadow: 
    0 25px 50px -12px rgba(0, 0, 0, 0.5),
    20px 20px 60px -20px rgba(255, 255, 255, 0.1);
}

.product-card img {
  transition: transform 0.8s cubic-bezier(0.23, 1, 0.32, 1);
}

.product-card:hover img {
  transform: scale(1.1) translateZ(30px);
}

.scroll-reveal {
  opacity: 0;
  transform: translateY(100px) rotateX(10deg);
  transition: all 1.2s cubic-bezier(0.23, 1, 0.32, 1);
  transform-style: preserve-3d;
}

.scroll-reveal.visible {
  opacity: 1;
  transform: translateY(0) rotateX(0);
}

.feature-icon {
  animation: float 8s cubic-bezier(0.23, 1, 0.32, 1) infinite;
  filter: drop-shadow(0 10px 15px rgba(255,255,255,0.1));
}

.glass-effect {
  backdrop-filter: blur(15px);
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.button-3d {
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  transform-style: preserve-3d;
  perspective: 1000px;
}

.button-3d:hover {
  transform: translateY(-5px) translateZ(20px);
  box-shadow: 
    0 15px 30px -10px rgba(0, 0, 0, 0.3),
    0 5px 15px rgba(255, 255, 255, 0.1);
}

@keyframes gradientBG {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
