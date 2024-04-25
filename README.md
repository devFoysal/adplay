# AdPlay RTB Bidding System

This AdPlay project handles Real-Time Bidding (RTB) scenarios by processing bid requests and generating appropriate banner campaign responses.

## Objective

The objective of this project is to develop a PHP script to handle bid requests and generate suitable banner campaign responses for RTB scenarios.

## Requirements

- PHP >= 7.3
- Composer
- Laravel Framework

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/devFoysal/adplay.git
    ```

2. Navigate to the project directory:

    ```bash
    cd adplay
    ```

3. Install dependencies:

    ```bash
    composer install
    ```

4. Set up your environment variables by copying the `.env.example` file:

    ```bash
    cp .env.example .env
    ```

    Ensure you set up your database and other necessary configurations in the `.env` file.

5. Generate the application key:

    ```bash
    php artisan key:generate
    ```

## Usage

1. Start the Laravel development server:

    ```bash
    php artisan serve
    ```

2. Send a POST request to the `/api/bid` endpoint with a JSON payload representing a bid request. Example:

    ```bash
    curl -X POST http://localhost:8000/api/bid \
    -H "Content-Type: application/json" \
    -d '{"device": "mobile", "geo_location": "US", "ad_format": "image", "bid_floor": 0.5}'
    ```

    Replace the JSON payload with your bid request parameters.

## Structure

The project follows the MVC pattern with the following structure:

- `app/Http/Controllers`: Contains the controllers for handling HTTP requests.
- `app/Services`: Contains the services for processing bid requests and generating campaign responses.
- `routes/api.php`: Defines the API routes.
- `tests/Feature`: Contains feature tests for the application.

## Testing

To run tests, execute the following command:

```bash
php artisan test
