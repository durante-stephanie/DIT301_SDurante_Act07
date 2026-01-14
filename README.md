## Reflection

### 1. What did you learn about using fragments and navigation components?
I learned that the Navigation Component simplifies managing app navigation by using a visual graph instead of manually handling fragment transactions with code. It makes switching between screens (like Home, Profile, and Settings) much cleaner and handles the "back stack" automatically. I also learned that `FragmentContainerView` acts as the host where different fragments are swapped in and out based on the user's selection in the Bottom Navigation bar.

### 2. How did you make your UI adaptive to screen size or orientation?
To ensure the app supports different screen sizes, I used `ConstraintLayout`, which allows UI elements to position themselves relative to the parent container rather than using hardcoded positions. For larger screens (like tablets), I created a specific resource folder named `layout-sw600dp`. This tells Android to automatically load a different layout file when the device screen is 600dp or wider, ensuring the UI looks good on both phones and tablets without changing the Kotlin code.

### 3. What challenges did you face when combining Bottom Navigation and Tabs?
The main challenge was managing nested navigation. Since the `ProfileFragment` (which is part of the Bottom Navigation) contains its own internal navigation (Tabs for "Info" and "Gallery"), I had to ensure the `ViewPager2` and `TabLayout` were set up correctly inside that fragment without interfering with the main bottom navigation. Another challenge was debugging a crash caused by missing `layout_width` attributes in the XML, which taught me the importance of reading Logcat errors (`InflateException`) to pinpoint layout issues.
