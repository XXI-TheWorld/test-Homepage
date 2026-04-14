## 1. Guest ID Initialization

- [x] 1.1 Add function to generate random 4-digit guest ID (1000-9999)
- [x] 1.2 Add function to get or create guest ID from localStorage
- [x] 1.3 Call guest ID initialization on page load

## 2. UI Changes

- [x] 2.1 Replace nickname input field with readonly display "当前身份：XXXX"
- [x] 2.2 Style the identity display to match existing design

## 3. Comment Submission Logic

- [x] 3.1 Modify submitComment function to use guest_id instead of nickname field
- [x] 3.2 Remove nickname validation since it's auto-generated
- [x] 3.3 Ensure message validation still works

## 4. Testing

- [x] 4.1 Test new visitor sees generated guest ID
- [x] 4.2 Test returning visitor sees same guest ID
- [x] 4.3 Test comment submission uses correct guest ID
