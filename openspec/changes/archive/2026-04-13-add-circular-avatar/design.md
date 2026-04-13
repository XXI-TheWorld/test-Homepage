## Context

The webpage needs a profile avatar displayed in circular format. The image is located at `./images/touxiang.jpg`. CSS will be used to style the image as a circle.

## Goals / Non-Goals

**Goals:**
- Display the avatar image in a perfect circle using CSS border-radius
- Ensure the avatar is properly sized (typically 100-150px diameter)
- Use relative path for image source portability

**Non-Goals:**
- Not implementing user upload functionality
- Not adding border, shadow, or other decorative effects (unless needed for circular masking)

## Decisions

- **CSS `border-radius: 50%`**: Makes the image a perfect circle regardless of original dimensions.
  - Alternative: `border-radius: 50px` - requires knowing exact dimensions, less flexible
  - Chosen: `border-radius: 50%` scales perfectly with any image size

- **Fixed dimensions**: Set explicit width and height (e.g., 120px) to ensure consistent sizing.
  - Alternative: `max-width/max-height` - could result in different sizes on different screens
  - Chosen: Fixed 120px diameter for consistent appearance

- **Image source path**: Use `./images/touxiang.jpg` relative path for portability.

## Risks / Trade-offs

- **Risk**: Non-square image may appear distorted when forced into circle.
  - **Mitigation**: If the source image is not square, use `object-fit: cover` to crop to square before applying border-radius, or recommend using a square image.
