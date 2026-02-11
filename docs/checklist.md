# API Testing Checklist

## Smoke checks
- [ ] API health endpoint returns 201
- [ ] Auth token can be generated successfully
- [ ] Booking can be created
- [ ] Created booking can be retrieved by ID

## Regression checks
- [ ] Booking can be updated with valid token
- [ ] Updated booking data is saved
- [ ] Booking can be deleted
- [ ] Deleted booking returns 404
      
## Negative checks
- [ ] Creating booking without firstname returns error
- [ ] Creating booking without bookingdates returns error
- [ ] Creating booking with invalid date format is handled correctly
- [ ] Creating booking with wrong data types returns error
- [ ] Get booking with invalid ID returns 404
      
## Security checks
- [ ] Update booking without token is forbidden
- [ ] Update booking with invalid token is forbidden
- [ ] Delete booking with invalid token is forbidden
- [ ] Delete booking without token is forbidden

## Contract checks
- [ ] Get booking response contains all required fields
- [ ] Field types are correct (string, number, boolean)
- [ ] bookingdates object contains checkin and checkout




