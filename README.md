# Christoffel's Menu App

Christoffel's Menu is a simple restaurant menu management app built using React Native. The app allows users to add dishes to a menu, display them on a home screen, and filter the menu (future functionality).

## Features

- **Add Menu Items**: Users can add dishes with name, description, course (Starters, Mains, Desserts), and price.
- **View Menu Items**: Display all the added menu items on the home screen.
- **Filter Menu**: Placeholder screen for filtering menu items (future implementation).

## Screens

### 1. Home Screen (`HomeScreen.tsx`)
Displays all the menu items added by the user. It also provides buttons to add a new dish or filter the existing menu.

- **Components**: 
  - `FlatList`: Displays the list of menu items.
  - `Button`: Navigation to `AddMenuScreen` and `FilterMenuScreen`.
  
- **State Management**: 
  - The list of menu items is managed using `useState` and `useEffect` to update the list whenever a new item is added.

### 2. Add Menu Screen (`AddMenuScreen.tsx`)
Users can add new dishes to the menu by entering a dish name, description, selecting a course (Starter, Main, Dessert), and entering the price.

- **Components**: 
  - `TextInput`: Allows users to enter dish details.
  - `Picker`: Allows users to select the course of the dish (Starter, Main, Dessert).
  - `Button`: Submits the form and navigates back to the home screen, passing the new item.

- **State Management**: 
  - `useState` hooks are used to handle the form inputs and manage the state of the dish being added.

### 3. Filter Menu Screen (`FilterMenuScreen.tsx`)
This is a placeholder screen for the filter functionality that will be implemented later. It includes a title and layout.

## Navigation

This project uses React Navigation to move between different screens.

- **Stack Navigation**: The app uses a stack navigator to navigate between the `Home`, `AddMenu`, and `FilterMenu` screens.

### Navigation Flow

- **Home Screen**: 
  - Add new menu items (`AddMenuScreen`)
  - Filter menu items (`FilterMenuScreen`)

- **Add Menu Screen**: 
  - Add a new dish to the menu and return to the home screen with the new item.
  
- **Filter Menu Screen**: 
  - Placeholder for future filter functionality.

## Project Structure

```plaintext
.
├── /screens/
│   ├── HomeScreen.tsx            # Main screen to display and manage menu items
│   ├── AddMenuScreen.tsx         # Form screen to add new menu items
│   ├── FilterMenuScreen.tsx      # Placeholder screen for menu filtering
├── /types/
│   └── RootStackParamList.ts     # Defines the type for navigation
└── App.tsx                       # Entry point for the app
