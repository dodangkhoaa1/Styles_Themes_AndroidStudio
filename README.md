
# Android Presentation: Styles and Themes Demo

## 1. Introduction to Styles and Themes

In Android, **Styles** and **Themes** are essential for maintaining a consistent and customizable design across your application.

- **Style**: A collection of properties that specify the look for a View (like color, text size, etc.).
- **Theme**: A Style applied to an Activity or the entire app, providing a consistent look and feel.

---

## 2. Demo Steps

### Step 1: Create a New Android Project
- Open Android Studio and create a new project.
- Select **Empty View Activity**.

### Step 2: Open `res/values/themes.xml`
- In recent Android Studio versions, styles and themes are defined in `themes.xml`.

### Step 3: Create a Custom Style
Add the following code to `themes.xml` to create a new button style:

```xml
<resources xmlns:tools="http://schemas.android.com/tools">
    <style name="MyCustomButtonStyle" parent="Widget.AppCompat.Button">
        <item name="android:background">#FF5722</item> <!-- Background color -->
        <item name="android:textColor">#FFFFFF</item> <!-- Text color -->
        <item name="android:textSize">18sp</item> <!-- Text size -->
    </style>
</resources>
```

### Step 4: Apply the Style to a Button
In the `activity_main.xml` layout file, apply the custom style to a Button:

```xml
<Button
    android:id="@+id/button"
    style="@style/MyCustomButtonStyle"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="My Button"
    android:layout_gravity="center" />
```

- **Run the app** to see the styled button.

---

## 3. Create and Apply a Theme

### Step 5: Create a Custom Theme
Add the following Theme in `themes.xml`:

```xml
<resources xmlns:tools="http://schemas.android.com/tools">
    <style name="MyCustomTheme" parent="Theme.MaterialComponents.DayNight.DarkActionBar">
        <item name="colorPrimary">#4CAF50</item> <!-- Primary color -->
        <item name="colorPrimaryDark">#388E3C</item> <!-- Primary dark color -->
        <item name="colorAccent">#FFC107</item> <!-- Accent color -->
    </style>
</resources>
```

### Step 6: Apply the Theme to the Application
Open `AndroidManifest.xml` and apply the theme to your Activity:

```xml
<application
    android:theme="@style/MyCustomTheme"
    ... >
    <activity android:name=".MainActivity">
        ...
    </activity>
</application>
```

- **Run the app** again to see the new theme applied to your entire Activity.

---

## 4. Using Theme Variables
- In `res/values/colors.xml`, define color variables:

```xml
<resources>
    <color name="colorPrimary">#4CAF50</color>
    <color name="colorPrimaryDark">#388E3C</color>
    <color name="colorAccent">#FFC107</color>
</resources>
```

- Reference these variables in `themes.xml`:

```xml
<item name="colorPrimary">@color/colorPrimary</item>
<item name="colorPrimaryDark">@color/colorPrimaryDark</item>
<item name="colorAccent">@color/colorAccent</item>
```

---

## 5. Conclusion
- **Styles** are used to define individual UI component properties, while **Themes** apply styles to entire Activities or apps.
- Customizing styles and themes helps maintain a consistent and flexible UI design across the application.

Feel free to ask questions!
