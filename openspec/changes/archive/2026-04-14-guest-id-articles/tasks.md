## 1. Article Form - Auto Guest ID

- [x] 1.1 Remove nickname input field from article publish form in index.html
- [x] 1.2 Use getGuestId() as author when saving new articles

## 2. Guest ID Modify Feature

- [x] 2.1 Add "修改身份" button next to identity display
- [x] 2.2 Implement modifyGuestId() function with prompt
- [x] 2.3 Update localStorage and UI when ID changes

## 3. Delete Without Nickname Verification

- [x] 3.1 Remove nickname input from delete confirmation modal
- [x] 3.2 Use getGuestId() directly for ownership verification in delete logic
- [x] 3.3 Update modal UI to remove nickname field

## 4. Delete Button Visibility

- [x] 4.1 Show delete button on article if guestId matches article.nickname
- [x] 4.2 Show delete button on comment if guestId matches comment.nickname
