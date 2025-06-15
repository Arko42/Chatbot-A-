Markdown

# 🤖 AAHIR Chatbot

AAHIR Chatbot is a simple, web-based chatbot built using Python Flask. It provides a user-friendly interface to access various utilities like weather information, current time, unit conversions, and capital lookups for specific countries.

## ✨ Features

* **Weather Lookup**: Get current weather conditions for a few predefined cities (e.g., Kolkata, Mumbai, Delhi).
* **Current Time**: Display the current time in Indian Standard Time (IST).
* **Unit Conversion**: Convert values between common units, including:
    * Kilograms (kg) to Pounds (lb) and vice-versa.
    * Centimeters (cm) to Inches and vice-versa.
    * Celsius (C) to Fahrenheit (F) and vice-versa.
* **Capital Lookup**: Find the capital city for a predefined list of countries (e.g., India, USA, UK).
* **Simple Web Interface**: An intuitive HTML/CSS/JavaScript frontend for easy interaction.

## 🛠️ Technologies Used

* **Backend**: Python, Flask
* **Frontend**: HTML, CSS, JavaScript (for API calls)

## 🚀 Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* Python 3.x installed on your system.
* `pip` (Python package installer).

### Installation

1.  **Save the `app.py` file**: Copy the provided `app.py` content into a file named `app.py` on your local machine.

2.  **Install Flask**: Open your terminal or command prompt and navigate to the directory where you saved `app.py`. Then, install Flask using pip:

    ```bash
    pip install Flask
    ```

### Running the Application

1.  **Run the Flask app**: In your terminal or command prompt, from the directory containing `app.py`, execute the following command:

    ```bash
    python app.py
    ```

    You should see output similar to this, indicating the server is running:

    ```
     * Serving Flask app 'app'
     * Debug mode: on
    WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
     * Running on [http://127.0.0.1:5000](http://127.0.0.1:5000)
    Press CTRL+C to quit
    ```

2.  **Access the Chatbot**: Open your web browser and go to `http://127.0.0.1:5000/`.

    You will see the AAHIR Chatbot interface, where you can interact with its features.

## ⚙️ API Endpoints

The Flask application exposes the following API endpoints, which are consumed by the frontend:

* **GET `/weather?city=<city_name>`**
    * **Description**: Retrieves weather information for the specified city.
    * **Parameters**: `city` (string, e.g., `kolkata`, `delhi`).
    * **Example Response**:
        ```json
        {
          "city": "Kolkata",
          "condition": "cloudy",
          "icon": "☁️"
        }
        ```

* **GET `/time`**
    * **Description**: Returns the current Indian Standard Time (IST).
    * **Parameters**: None.
    * **Example Response**:
        ```json
        {
          "Indian Time": "2025-06-15 18:27:04",
          "emoji": "🕒"
        }
        ```

* **GET `/convert?value=<number>&from=<unit1>&to=<unit2>`**
    * **Description**: Converts a given value from one unit to another.
    * **Parameters**:
        * `value` (float/integer, the value to convert).
        * `from` (string, the unit to convert from, e.g., `kg`, `cm`, `c`).
        * `to` (string, the unit to convert to, e.g., `lb`, `inch`, `f`).
    * **Supported Conversions**: `kg <-> lb`, `cm <-> inch`, `c <-> f`.
    * **Example Response**:
        ```json
        {
          "input": "10.0 kg",
          "output": "22.05 lb"
        }
        ```

* **GET `/capital?country=<country_name>`**
    * **Description**: Retrieves the capital city for the specified country.
    * **Parameters**: `country` (string, e.g., `india`, `usa`).
    * **Example Response**:
        ```json
        {
          "capital": "New Delhi",
          "country": "India"
        }
        ```

## 📄 License

This project is open-source and available under the MIT License.

---
**Note**: This chatbot uses predefined, sample data for weather, conversions, and capitals. It does not integrate with external APIs for real-time data.

Sources






