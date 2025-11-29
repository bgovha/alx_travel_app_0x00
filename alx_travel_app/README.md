# ALX Travel App

A Django-based travel booking application.

## Models

### Listing
- Represents properties available for booking
- Fields: title, description, address, city, country, price_per_night, max_guests, bedrooms, bathrooms, property_type, amenities, is_available, host

### Booking
- Represents guest bookings
- Fields: listing, guest, check_in, check_out, total_price, guests_count, status, special_requests

### Review
- Represents guest reviews for listings
- Fields: listing, guest, rating, comment

## Serializers

### ListingSerializer
- Serializes Listing model with nested host and reviews data

### BookingSerializer
- Serializes Booking model with nested listing and guest data
- Includes validation for booking dates and guest count

## Seeding the Database

To populate the database with sample data:

```bash
python manage.py seed