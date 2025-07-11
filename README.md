# Welcome to your Expo app 👋

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Add the environment variabled 
``` EXPO_PUBLIC_API_UR=   ```

3. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

## Get a fresh project

When you're ready, run:

```bash
npm run reset-project
```

This command will move the starter code to the **app-example** directory and create a blank **app** directory where you can start developing.

## Learn more

To learn more about developing your project with Expo, look at the following resources:

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals, or go into advanced topics with our [guides](https://docs.expo.dev/guides).
- [Learn Expo tutorial](https://docs.expo.dev/tutorial/introduction/): Follow a step-by-step tutorial where you'll create a project that runs on Android, iOS, and the web.

## Join the community

Join our community of developers creating universal apps.

- [Expo on GitHub](https://github.com/expo/expo): View our open source platform and contribute.
- [Discord community](https://chat.expo.dev): Chat with Expo users and ask questions.

---

## Solution Overview

This application is a simple React Native app built with the Expo managed workflow. It fetches a list of posts from the [JSONPlaceholder](https://jsonplaceholder.typicode.com/posts) public API and displays them in a scrollable list.

### Key Features:

- **Fixed Header**: A non-scrolling header containing the application title.
- **Scrollable Content**: A list of posts fetched from a remote API. Each list item displays a title and a body.
- **Fixed Footer**: A non-scrolling footer with a static copyright notice.
- **Loading & Error States**: The application displays a loading indicator while fetching data and shows a user-friendly error message if the API call fails.

### Project Structure:

- **`app/(tabs)/index.tsx`**: This is the main screen of the application. It contains all the UI and business logic for fetching, displaying, and handling the state of the posts list.
- **`types/post.ts`**: This file defines the TypeScript interface (`Post`) for the data objects fetched from the API, ensuring type safety.
- **`app/(tabs)/_layout.tsx`**: This file configures the tab navigator. The application is built into the existing tab-based structure that came with the project template.
- **`.env`**: This file (which must be created manually) stores the API endpoint URL.

## Assumptions and Limitations

### Assumptions

- The solution was implemented within the existing tab-based navigation structure provided by the initial Expo project template (`app/(tabs)`). The requirements did not specify removing this structure, so I built upon it.

### Limitations

- **No Pull-to-Refresh**: The list of posts is fetched only once when the component mounts. There is no functionality to manually refresh the data.
- **Basic Styling**: The styling is clean and functional, using React Native's built-in `StyleSheet`. No advanced design or theming has been applied.
