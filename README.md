# ShoppingListApp

A feature-rich **Shopping List** app built with **Kotlin**, **Jetpack Compose**, **MVVM architecture**, **Navigation**, **Retrofit** for network calls, and **Location Services** for enhanced shopping experiences. The app allows users to manage their shopping list, track items, get location, and more!

## ✨ Features

- **Modern UI**: Beautifully designed with Jetpack Compose for a smooth and intuitive experience.
- **MVVM Architecture**: Separates concerns for easier maintenance and testing.
- **Navigation**: Seamless in-app navigation using Jetpack Navigation Component.
- **Location Services**: Get location-based suggestions or notifications for items nearby.
- **Network Integration**: Fetch data from external APIs using Retrofit.
- **Add, Edit, and Delete Items**: Manage your shopping list with ease.
- **Mark Items as Purchased**: Visual indicators for purchased and pending items.
- **Persistent Data**: Uses Room Database to persist shopping list data locally.

## ⚙️ Technologies Used

- **Kotlin**: The primary language for Android development.
- **Jetpack Compose**: For building modern UI with declarative syntax.
- **MVVM Architecture**: Separation of concerns for easier development and testing.
- **Navigation**: Jetpack Navigation for navigating between different screens.
- **Retrofit**: A type-safe HTTP client for making API calls.
- **Location Services**: To track the user’s location and provide personalized shopping suggestions.
- **LiveData & ViewModel**: For managing UI-related data in a lifecycle-conscious way.

## 📦 Installation

To get the app up and running on your local machine, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/Shivanshs673/ShoppingListApp.git
    ```

2. Open the project in [Android Studio](https://developer.android.com/studio).

3. Build and run the app on an emulator or physical device.

4. Make sure to add your API key in the `strings.xml` if you're using Retrofit for network requests.

## 📱 Features Overview

### 1. **MVVM Architecture**:
The app is built using the **Model-View-ViewModel (MVVM)** architecture. The **ViewModel** handles UI-related data, and the **Model** layer is responsible for data handling, including fetching from local databases and remote APIs.

### 2. **Navigation**:
We use **Jetpack Navigation** to navigate between various screens like the Home Screen, Item Details Screen, and Add Item Screen. This allows for easy back-stack management and deep-linking.

```kotlin
navController.navigate("itemDetails/{itemId}")
```

### 3. **Location Services**:
The app uses **Location Services** to track the user’s current location. It uses the FusedLocationProviderClient to get the most accurate location, and the app can provide recommendations or notifications based on the user’s proximity to certain places.

```kotlin
val fusedLocationClient = LocationServices.getFusedLocationProviderClient(context)
fusedLocationClient.lastLocation.addOnSuccessListener { location: Location? ->
    // Use location data for personalized suggestions
}
```

### 4. **Retrofit Integration**:
**Retrofit** is used for fetching data from remote APIs. For example, you can fetch shopping-related data from an external API to provide recommendations, item prices, or other relevant data.

```kotlin
interface ApiService {
    @GET("shoppingItems")
    suspend fun getShoppingItems(): List<ShoppingItem>
}
```

## 🎮 Usage

1. **Add an Item**: Tap the "Add Item" button to add new shopping list entries.
2. **Edit or Delete an Item**: Long-press on an item to either edit or remove it.
3. **Mark Items as Purchased**: Tap an item to mark it as purchased, with a smooth UI transition showing its status.
4. **Track Your Progress**: View a summary of all your items, showing both pending and completed tasks.

## 🧑‍💻 Contributing

I welcome contributions! If you’d like to improve the app or suggest new features, feel free to fork the repository and submit a pull request.

Steps to contribute:
- Fork the repo.
- Create your feature branch (`git checkout -b feature/your-feature`).
- Commit your changes (`git commit -am 'Add new feature'`).
- Push to the branch (`git push origin feature/your-feature`).
- Create a new Pull Request.

## 📝 License

This project is licensed under the MIT License.

---

### 🌈 Acknowledgments

Special thanks to:
- The Android Developer community.
- [Jetpack Compose](https://developer.android.com/jetpack/compose) for an amazing UI framework.

---

### 📧 Contact

If you have any questions or feedback, feel free to reach out!

- **GitHub**: [shivanshs673](https://github.com/Shivanshs673)  
- **LinkedIn**: [Shivansh Shukla](https://www.linkedin.com/in/shivansh-shukla-2a9552257/)  
- **Email**: [shivansh Shukla](mailto:shivanshs673@gmail.com)

---

**⭐ If you like this project, don't forget to give it a star! ⭐**


