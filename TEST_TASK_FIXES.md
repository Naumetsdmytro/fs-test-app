# Test Task Fixes

## Issues Fixed

### 1. Authentication Fixes
- **Problem**: Login/Registration returned 200 OK instead of 401 Unauthorized
- **Fix**: Changed `res.json()` to `res.status(401).json()` in userController.js

### 2. Image Hover Effect
- **Problem**: Need zoom-in effect on menu images
- **Fix**: Added CSS hover effect to `.food-item-image`

### 3. Minus Button Position
- **Problem**: Minus button moved when quantity changed (especially with large numbers)
- **Fix**: Used flexbox with `flex-shrink: 0` to prevent button shrinking, `justify-content: space-between` for consistent spacing, and `min-width: 40px` for quantity text

## Files Changed
- `backend/controllers/userController.js`
- `frontend/src/components/FoodItem/FoodItem.css` 