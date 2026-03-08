---
name: animation-micro-interaction-pack
description: Adds animations, transitions, and micro-interactions to UI components. Use when a user wants to make an interface feel more polished or alive — hover effects, entrance animations, loading states, gesture feedback, or any motion that communicates state changes. Also trigger when a UI feels "flat" or "static" even if the user doesn't use the word "animation".
---

## Mission

Add motion that serves communication, not decoration — every animation should tell the user something: what changed, what's loading, what's interactive, what succeeded or failed. Default to subtle and fast. When in doubt, less is more. Always implement `prefers-reduced-motion` support — motion that can't be disabled is an accessibility failure.

## Animation Patterns

**Hover Effects**: Scale, lift (translateY), glow (box-shadow), color shifts
**Entrance**: Fade-in, slide-in, zoom-in with stagger for lists
**Exit**: Fade-out, slide-out, scale-out
**Loading**: Pulse, skeleton waves, progress bars
**Gestures**: Ripple on click, drag feedback, swipe indicators

## Tailwind Animations

```css
/* tailwind.config.js */
animation: {
  'fade-in': 'fadeIn 0.5s ease-out',
  'slide-up': 'slideUp 0.3s ease-out',
  'scale-in': 'scaleIn 0.2s ease-out',
}
```

## Framer Motion Examples

```tsx
<motion.div
  initial={{ opacity: 0, y: 20 }}
  animate={{ opacity: 1, y: 0 }}
  transition={{ duration: 0.3 }}
/>
```

## Best Practices

Use 200-300ms for micro-interactions, respect prefers-reduced-motion, animate transform/opacity for performance, add easing functions, stagger list items, provide hover/active states.
