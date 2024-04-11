---
title: Test Android 2-1
layout: upj_design
permalink: /drafts/android-2-1/
---

#### Table Of Contents

- TOC
{:toc}

## Basic 1 - Layouts
{: #upj_1676528515775}

[App 1-AboutMe App](https://github.com/udacity/andfun-kotlin-about-me)

```kotlin
// Hide the keyboard.
val imm = getSystemService(Context.INPUT_METHOD_SERVICE) as InputMethodManager
imm.hideSoftInputFromWindow(view.windowToken, 0)
```

### dataBinding
{: #upj_1676528537087}

```groovy
buildFeatures {
  viewBinding = true
  dataBinding = true
}
```
wrap root tag with layout tag

```xml
<layout
  tools:context="kr.sungil.androidkotlin.game.GameFragment"
  xmlns:android="http://schemas.android.com/apk/res/android"
  xmlns:tools="http://schemas.android.com/tools"
  xmlns:app="http://schemas.android.com/apk/res-auto"
  >

  <data>
    ↓ 이부분 넣고 Build > Clean Project 해주어여 함
    <variable
      name="gameViewModel"
      type="kr.sungil.androidkotlin.game.GameViewModel"
      />
  </data>

  <androidx.constraintlayout.widget.ConstraintLayout
    android:id="@+id/game_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    >
    ...
  </androidx.constraintlayout.widget.ConstraintLayout>
</layout>
```

```kotlin
class SleepTrackerFragment : Fragment() {
  override fun onCreateView(inflater: LayoutInflater, container: ViewGroup?, savedInstanceState: Bundle?): View? {
    val binding: FragmentSleepTrackerBinding = DataBindingUtil.inflate(
      inflater, R.layout.fragment_sleep_tracker, container, false
    )
    return binding.root
  }
}
```

### viewBinding
{: #upj_1676528761343}

```groovy
buildFeatures {
  viewBinding = true
  dataBinding = true
}
```

```kotlin
class TitleFragment : Fragment() {
  private var binding: FragmentTitleBinding? = null

  override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
    super.onViewCreated(view, savedInstanceState)
    val _binding = FragmentTitleBinding.bind(view)
    binding = _binding

    binding!!.playGameButton.setOnClickListener {
      findNavController().navigate(TitleFragmentDirections.actionTitleToGame())
    }
  }
}
```

```kotlin
class MainActivity : AppCompatActivity() {
	private lateinit var binding: ActivityMainBinding
	override fun onCreate(savedInstanceState: Bundle?) {
		super.onCreate(savedInstanceState)
		binding = ActivityMainBinding.inflate(layoutInflater)
		setContentView(binding.root)

		val homeFragment = HomeFragment()
		val chatListFragment = ChatListFragment()
		val myPageFragment = MyPageFragment()

		replaceFragment(homeFragment)

		binding.btnvMenu.setOnItemSelectedListener {
			when (it.itemId) {
				R.id.home -> {
					replaceFragment(homeFragment)
				}
				R.id.chat_list -> {
					replaceFragment(chatListFragment)
				}
				R.id.my_page -> {
					replaceFragment(myPageFragment)
				}
			}
			true
		}
	}

	private fun replaceFragment(fragment: Fragment) {
		supportFragmentManager.beginTransaction()
			.replace(R.id.fl_container, fragment)
			.commit()
	}
}
```

### build.gradle 샘플
{: #upj_1676770940917}

```groovy
// Project
// Top-level build file where you can add configuration options common to all sub-projects/modules.
buildscript {
  dependencies {
    classpath "androidx.navigation:navigation-safe-args-gradle-plugin:2.5.3"
  }
}
plugins {
	id 'com.android.application' version '7.3.1' apply false
	id 'com.android.library' version '7.3.1' apply false
	id 'org.jetbrains.kotlin.android' version '1.8.0' apply false
}

// Module :app
plugins {
  id 'com.android.application'
  id 'org.jetbrains.kotlin.android'
  id 'kotlin-kapt'
  id 'androidx.navigation.safeargs'
}

android {
  namespace 'kr.sungil.androidkotlin'
  compileSdk 33

  defaultConfig {
    applicationId "kr.sungil.androidkotlin"
    minSdk 28
    targetSdk 33
    versionCode 1
    versionName "1.0"

    testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
  }

  buildTypes {
    release {
      minifyEnabled false
      proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
    }
  }
  compileOptions {
    sourceCompatibility JavaVersion.VERSION_11
    targetCompatibility JavaVersion.VERSION_11
  }
  kotlinOptions {
    jvmTarget = '11'
  }
  buildFeatures {
    dataBinding = true
  }
}

dependencies {

  implementation 'androidx.core:core-ktx:1.9.0'
  implementation 'androidx.appcompat:appcompat:1.6.1'
  implementation 'com.google.android.material:material:1.8.0'
  implementation 'androidx.constraintlayout:constraintlayout:2.1.4'

  // navigation graph
  implementation "androidx.navigation:navigation-fragment-ktx:2.5.3"
  implementation "androidx.navigation:navigation-ui-ktx:2.5.3"

  // Room and Lifecycle
  implementation "androidx.room:room-runtime:2.5.0"
  kapt "androidx.room:room-compiler:2.5.0"
  implementation "androidx.lifecycle:lifecycle-extensions:2.2.0"

  // Coroutines
  implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:1.6.4"
  implementation "org.jetbrains.kotlinx:kotlinx-coroutines-android:1.6.4"

  // ViewModel and LiveData
  implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:2.5.1"

  // Kotlin Extensions and Coroutines support for Room
  implementation "androidx.room:room-ktx:2.5.0"

  // Testing
  testImplementation 'junit:junit:4.13.2'
  androidTestImplementation 'androidx.test.ext:junit:1.1.5'
  androidTestImplementation 'androidx.test.espresso:espresso-core:3.5.1'

}
```

[App 2-ColorMyViews App](https://github.com/udacity/andfun-kotlin-color-my-views)

Ratios

```xml
<View
  android:layout_width="10dp"
  android:layout_height="0dp"
  app:layout_constraintBottom_toBottomOf="parent"
  app:layout_constraintDimensionRatio="h,1:10"
  app:layout_constraintEnd_toEndOf="parent"
  app:layout_constraintHorizontal_bias="0.316"
  app:layout_constraintStart_toStartOf="parent"
  app:layout_constraintTop_toTopOf="parent"
  app:layout_constraintVertical_bias="0.148" />
```

- Spread chain
- Packed chain
- Spread inside chain
- Packed chain with bias
- Weighted chain

```kotlin
private fun setListeners() {
  binding.apply {
    val clickableViews: List<View> = listOf(
      boxOneText, boxTwoText, boxThreeText
    )

    for (item in clickableViews) {
      item.setOnClickListener { makeColored(it) }
    }
  }
}
```

## Basic 2 - App Navigation
{: #upj_1676528931517}

[App 3-Trivia App](https://github.com/udacity/andfun-kotlin-android-trivia)

Principle of Navigation

1. There's always a Starting Place.
2. You can always Go Back.
3. Up goes Back (Mostly)

### navigation graph
{: #upj_1676528665751}

navigation dependency 

```groovy
implementation "androidx.navigation:navigation-fragment-ktx:2.5.3"
implementation "androidx.navigation:navigation-ui-ktx:2.5.3"
```

```xml
<fragment
  android:id="@+id/gameFragment"
  android:name="kr.sungil.androidkotlin.GameFragment"
  android:label="fragment_game"
  tools:layout="@layout/fragment_game" >
  <action
    android:id="@+id/action_gameFragment_to_gameWonFragment"
    app:destination="@id/gameWonFragment"
    app:popUpTo="@id/gameFragment"
    app:popUpToInclusive="true" />
  <action
    android:id="@+id/action_gameFragment_to_gameOverFragment"
    app:destination="@id/gameOverFragment"
    app:popUpTo="@id/gameFragment"
    app:popUpToInclusive="true" />
</fragment>
```

```kotlin
view.findNavController().navigate(R.id.action_gameFragment_to_gameWonFragment)
```

fragment view binding

```kotlin
class AboutFragment : Fragment(R.layout.fragment_about) {
  private var binding: FragmentAboutBinding? = null
  override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
    super.onViewCreated(view, savedInstanceState)
    val _binding = FragmentAboutBinding.bind(view)
    binding = _binding
  }
}
```

### add menu
{: #upj_1676528997565}

```kotlin
private fun setupMenu() {
  (requireActivity() as MenuHost).addMenuProvider(object : MenuProvider {
    override fun onCreateMenu(menu: Menu, menuInflater: MenuInflater) {
      menuInflater.inflate(R.menu.overflow_menu, menu)
    }

    override fun onMenuItemSelected(menuItem: MenuItem): Boolean {
      return NavigationUI.onNavDestinationSelected(menuItem, view!!.findNavController())
    }
  }, viewLifecycleOwner, Lifecycle.State.RESUMED)
}
```

### SafeArgs
{: #upj_1676528959278}

```groovy
// Project
buildscript {
  dependencies {
    classpath "androidx.navigation:navigation-safe-args-gradle-plugin:2.5.3"
  }
}
plugins {
  id 'com.android.application' version '7.3.1' apply false
  id 'com.android.library' version '7.3.1' apply false
  id 'org.jetbrains.kotlin.android' version '1.8.0' apply false
}
```

```groovy
// App
plugins {
  id 'com.android.application'
  id 'org.jetbrains.kotlin.android'
  id 'kotlin-kapt'
  id 'androidx.navigation.safeargs'
}
```

```xml
<!--add arguments-->
<fragment
  android:id="@+id/gameWonFragment"
  android:name="kr.sungil.androidkotlin.GameWonFragment"
  android:label="fragment_game_won"
  tools:layout="@layout/fragment_game_won"
  >
  <action
    android:id="@+id/action_gameWonFragment_to_gameFragment"
    app:destination="@id/gameFragment"
    />
  
  <argument
    android:name="numQuestions"
    app:argType="integer"
    android:defaultValue="0"
    />
  ↑ 이렇게 하면 에러날 수 있음
  <argument
    android:name="numCorrect"
    app:argType="integer"
    />
</fragment>
```

```kotlin
// send args
view.findNavController().navigate(GameFragmentDirections.actionGameFragmentToGameWonFragment())
view.findNavController()
  .navigate(GameFragmentDirections.actionGameFragmentToGameWonFragment(numQuestions, questionIndex))
// get args
var args = GameWonFragmentArgs.fromBundle(requireArguments())
```

```xml
<!--getString with parameters-->
<string name="share_success_text">I mastered #UdacityAndroidTrivia with %1$d/%2$d correct questions!</string>
```

```kotlin
getString(R.string.share_success_text, args.numCorrect, args.numQuestions)
```

### app drawer on up button
{: #upj_1676529022950}

```kotlin
class MainActivity : AppCompatActivity() {
  private lateinit var drawerLayout: DrawerLayout
  private lateinit var appBarConfiguration: AppBarConfiguration

  override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    val binding = ActivityMainBinding.inflate(layoutInflater)
    setContentView(binding.root)

    drawerLayout = binding.drawerLayout
    val navController = this.findNavController(R.id.myNavHostFragment)
    NavigationUI.setupActionBarWithNavController(this, navController, drawerLayout)
    appBarConfiguration = AppBarConfiguration(navController.graph, drawerLayout)
    navController.addOnDestinationChangedListener { nc: NavController, nd: NavDestination, bundle: Bundle? ->
      if(nd.id == nc.graph.startDestinationId) {
        drawerLayout.setDrawerLockMode(DrawerLayout.LOCK_MODE_UNLOCKED)
      } else {
        drawerLayout.setDrawerLockMode(DrawerLayout.LOCK_MODE_LOCKED_CLOSED)
      }
    }
    NavigationUI.setupWithNavController(binding.navView, navController)
  }

  override fun onSupportNavigateUp(): Boolean {
    val navController = this.findNavController(R.id.myNavHostFragment)
    return NavigationUI.navigateUp(navController, appBarConfiguration)
  }
}
```

## Basic 3 - Activity and Fragment Lifecycle
{: #upj_1676529035134}

[App 4-DessertPusher App](https://github.com/udacity/andfun-kotlin-dessert-pusher)

### Timber Log Tree
{: #upj_1676529045694}

```groovy
implementation 'com.jakewharton.timber:timber:5.0.1'
```

```kotlin
class PusherApplication : Application() {
  override fun onCreate() {
    super.onCreate()
    Timber.plant(Timber.DebugTree())
  }
}
```

```kotlin
Timber.i("onStart Called")
```

### Lifecycle Documents
{: #upj_1676529086822}

[Activity Lifecycle Worksheet](https://video.udacity-data.com/topher/2018/November/5be0f083_activity-lifecycle-worksheet/activity-lifecycle-worksheet.pdf),
[garbage collection](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)),
[Activity Lifecycle Summary](https://video.udacity-data.com/topher/2018/November/5be286d0_l4-1803sc-a-share-dialog-and-onpause-onresume-border/l4-1803sc-a-share-dialog-and-onpause-onresume-border.png)

Lifecycle cheet sheet: 
[Single activities](https://medium.com/androiddevelopers/the-android-lifecycle-cheat-sheet-part-i-single-activities-e49fd3d202ab),
[Multiple activities](https://medium.com/androiddevelopers/the-android-lifecycle-cheat-sheet-part-ii-multiple-activities-a411fd139f24),
[Fragments](https://medium.com/androiddevelopers/the-android-lifecycle-cheat-sheet-part-iii-fragments-afc87d4f37fd)

- Resumed(onResume, onPause): Activity is visible, and Activity has focus
- Started(onStart, onStop): Activity is visible

[Handling Lifecycle](https://developer.android.com/topic/libraries/architecture/lifecycle),
[Lifecycle Observer in Android blog](https://medium.com/@aritrodam773/lifecycle-observer-in-android-6e9d16ed49bc)

