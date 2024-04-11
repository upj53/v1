---
title: Test Android 2-2
layout: upj_design
permalink: /drafts/android-2-2/
---

#### Table Of Contents

- TOC
{:toc}

## Basic 4-1 App Architecture (UI Layer)
{: #upj_1676529112182}

[App 5-GuessIt App](https://github.com/udacity/andfun-kotlin-guess-it)
([Codes](https://github1s.com/udacity/andfun-kotlin-guess-it))

[Architecture Sample App](https://github.com/android/architecture-samples),
[MVP 패턴](https://medium.com/upday-devs/android-architecture-patterns-part-2-model-view-presenter-8a6faaae14a5),
[앱 아키텍처](https://developer.android.com/topic/architecture?hl=ko),
[ViewModel 개요](https://developer.android.com/topic/libraries/architecture/viewmodel?hl=ko),
[ViewModel Doc](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModel),
[ViewModel Simple Example App](https://medium.com/androiddevelopers/viewmodels-a-simple-example-ed5ac416317e),
[UI 상태 저장](https://developer.android.com/topic/libraries/architecture/saving-states?hl=ko),
[ViewModel Posts](https://medium.com/androiddevelopers/viewmodels-persistence-onsaveinstancestate-restoring-ui-state-and-loaders-fc7cc4a6c090),
[LiveData 개요](https://developer.android.com/topic/libraries/architecture/livedata?hl=ko),
[LiveData Doc](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData),
[LiveData Lifecycle](https://developer.android.com/topic/libraries/architecture/lifecycle?hl=ko),
[Backing properties](https://kotlinlang.org/docs/properties.html#backing-properties),
[Kotlin 스타일 가이드](https://developer.android.com/kotlin/style-guide?hl=ko#backing-properties),
[캡슐화](https://ko.wikipedia.org/wiki/%EC%BA%A1%EC%8A%90%ED%99%94),
[LiveData Observer](https://developer.android.com/topic/libraries/architecture/livedata?hl=ko#observe_livedata_objects),
[CountDownTimer Class Docs](https://developer.android.com/reference/kotlin/android/os/CountDownTimer),
[ViewModelFactory](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModelProvider.Factory.html),
[Factory 디자인패턴](https://en.wikipedia.org/wiki/Factory_(object-oriented_programming)),
[Factory 예제](https://cjw-awdsd.tistory.com/54),
[레이아웃 및 결합 표현식](https://developer.android.com/topic/libraries/data-binding/expressions?hl=ko),
[ViewModel - DataBinding 연결](https://developer.android.com/topic/libraries/data-binding/architecture?hl=ko#viewmodel),
[LiveData 자동업데이트](https://developer.android.com/topic/libraries/data-binding/architecture?hl=ko#livedata),
[문자열 Formatting](https://developer.android.com/guide/topics/resources/string-resource?hl=ko#formatting-strings),
[Layout Binding 수식](https://developer.android.com/topic/libraries/data-binding/expressions?hl=ko#resources),

```xml
 <Button
     android:id="@+id/correct_button"
     android:layout_width="wrap_content"
     android:layout_height="wrap_content"
     android:layout_marginEnd="16dp"
     android:onClick="@{() -> gameViewModel.onCorrect()}"
     android:text="@string/got_it"
     android:theme="@style/GoButton"
     app:layout_constraintBottom_toBottomOf="parent"
     app:layout_constraintEnd_toEndOf="parent"
     app:layout_constraintHorizontal_bias="0.5"
     app:layout_constraintStart_toEndOf="@+id/skip_button"
     app:layout_constraintTop_toTopOf="@+id/guideline" />
```

```xml
<!--string.xml-->
<string name="quote_format">\"%s\"</string>
<string name="score_format">Current Score: %d</string>

<!--UI xml file-->
 <TextView
     android:id="@+id/word_text"
     android:layout_width="wrap_content"
     android:layout_height="wrap_content"
     android:animateLayoutChanges="true"
     android:fontFamily="sans-serif"
     android:text="@{@string/quote_format(gameViewModel.word)}"
     android:textAppearance="@style/TextAppearance.AppCompat.Headline"
     android:textColor="@color/black_text_color"
     android:textSize="34sp"
     android:textStyle="normal"
     app:layout_constraintBottom_toTopOf="@+id/score_text"
     app:layout_constraintEnd_toEndOf="parent"
     app:layout_constraintHorizontal_bias="0.5"
     app:layout_constraintStart_toStartOf="parent"
     app:layout_constraintTop_toBottomOf="@+id/word_is_text"
     app:layout_constraintVertical_chainStyle="packed"
     tools:text="&quot;Tuna&quot;" />
```

```kotlin
val currentTimeString = Transformations.map(currentTime) { time ->
    DateUtils.formatElapsedTime(time)
}
```

```kotlin
binding.setLifecycleOwner(this)
```

[Android Permission](https://developer.android.com/guide/topics/permissions/overview?hl=ko),


## Basic 4-2 App Architecture (Persistence)
{: #upj_1676529117694}

[SQL Syntax on SQLite](https://www.sqlite.org/lang.html)

[App 6-SleepTracker App](https://github.com/udacity/andfun-kotlin-sleep-tracker)
([Code](https://github1s.com/udacity/andfun-kotlin-sleep-tracker))

[Room Doc](https://developer.android.com/jetpack/androidx/releases/room?hl=ko),
[Room 으로 데이터 정의하기](https://developer.android.com/training/data-storage/room/defining-data?hl=ko),
[Room 으로 로컬 데이터베이스에 저장](https://developer.android.com/training/data-storage/room?hl=ko),
[PrimaryKey](https://developer.android.com/reference/androidx/room/PrimaryKey),
[ColumnInfo](https://developer.android.com/reference/androidx/room/ColumnInfo),
[Index](https://developer.android.com/reference/androidx/room),
[Database](https://developer.android.com/reference/androidx/room/Database),
[Dao](https://developer.android.com/reference/androidx/room/Dao),
[Query](https://developer.android.com/reference/androidx/room/Query),
[Delete](https://developer.android.com/reference/androidx/room/Delete),
[Insert](https://developer.android.com/reference/androidx/room/Insert),

DAO Annotations

- @Insert
- @Delete
- @Update
- @Query

[RoomDatabase](https://developer.android.com/reference/androidx/room/RoomDatabase),
[RoomDatabase.Builder](https://developer.android.com/reference/androidx/room/RoomDatabase.Builder),
[Database](https://developer.android.com/reference/androidx/room/Database),
[RawQuery](https://developer.android.com/reference/androidx/room/RawQuery),
[싱글턴 패턴](https://ko.wikipedia.org/wiki/%EC%8B%B1%EA%B8%80%ED%84%B4_%ED%8C%A8%ED%84%B4),
[Volatile Synchronized 올바른 사용법](https://developer.android.com/topic/architecture?hl=ko#separation-of-concerns),
[Companion Object](https://kotlinlang.org/docs/object-declarations.html#Companion-Objects)

[Room 데이터베이스 이전](https://developer.android.com/training/data-storage/room/migrating-db-versions?hl=ko),
[About Room Migrations Blog](https://medium.com/androiddevelopers/understanding-migrations-with-room-f01e04b07929),
[Migrations Testing](https://medium.com/androiddevelopers/testing-room-migrations-be93cdb0d975)

[Android에서 앱 테스트](https://developer.android.com/training/testing?hl=ko),
[테스트 기본 요소](https://developer.android.com/training/testing/fundamentals?hl=ko)

테스트의 장점

- 장애에 관한 신속한 피드백
- 개발 주기에서 조기 장애 감지
- 회귀에 신경 쓸 필요 없이 코드를 최적화할 수 있도록 하는 더 안전한 코드 리랙터링
- 기술적 문제를 최소화하는 안정적인 개발 속도

[레이아웃 재사용: include, merge](https://developer.android.com/develop/ui/views/layout/improving-layouts/reusing-layouts?hl=ko)

[ViewModelProvider.Factory](https://developer.android.com/reference/androidx/lifecycle/ViewModelProvider.Factory),
[팩토리 메서드 패턴](https://ko.wikipedia.org/wiki/%ED%8C%A9%ED%86%A0%EB%A6%AC_%EB%A9%94%EC%84%9C%EB%93%9C_%ED%8C%A8%ED%84%B4),
[템플릿 메소드 패턴](https://ko.wikipedia.org/wiki/%ED%85%9C%ED%94%8C%EB%A6%BF_%EB%A9%94%EC%86%8C%EB%93%9C_%ED%8C%A8%ED%84%B4),
[Template Method Pattern Blog](https://yaboong.github.io/design-pattern/2018/09/27/template-method-pattern/),

Coroutines [Colab for Coroutine](https://developer.android.com/codelabs/kotlin-coroutines#0)

- Asynchronous: The coroutine runs independently from the main execution steps of your program.
- Non-blocking: The system is not blocking the main or UI thread. (suspend)
- Sequential code 

Coroutines need

- Job: A background job. Conceptually, a job is a cancellable thing with a life-cycle that culminates in its completion.
- Dispatcher: The dispatcher sends off coroutines to run on various threads.
- Scope: The scope combines information, including a job and dispatcher, to define the context in which the coroutine runs.

[SimpleDateFormat](https://developer.android.com/reference/java/text/SimpleDateFormat),
[Coroutines Doc](https://kotlinlang.org/docs/coroutines-overview.html),
[Coroutine context and dispatchers](https://kotlinlang.org/docs/coroutine-context-and-dispatchers.html),
[Dispatchers](https://kotlinlang.org/api/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/-dispatchers/),
[Job](https://kotlinlang.org/api/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/-job/),
[launch](https://kotlinlang.org/api/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/launch.html),
[Returns and jumps Expressions in Kotlin](https://kotlinlang.org/docs/returns.html#return-at-labels),
[HtmlCompat](https://developer.android.com/reference/androidx/core/text/HtmlCompat),
[CDATA](https://www.w3.org/TR/REC-xml/#sec-cdata-sect),
[Chracter Data](https://www.w3.org/TR/REC-xml/#dt-chardata),

[Navigation](https://developer.android.com/guide/navigation?hl=ko),
[Navigation Design Graph](https://developer.android.com/guide/navigation/navigation-design-graph?hl=ko),

[버튼](https://developer.android.com/guide/topics/ui/controls/button?hl=ko),
[아키텍처 구성요소에 레이아웃 뷰 결합](https://developer.android.com/topic/libraries/data-binding/architecture?hl=ko),
[Snackbar](https://developer.android.com/reference/kotlin/androidx/compose/material/package-summary#Snackbar(androidx.compose.ui.Modifier,kotlin.Function0,kotlin.Boolean,androidx.compose.ui.graphics.Shape,androidx.compose.ui.graphics.Color,androidx.compose.ui.graphics.Color,androidx.compose.ui.unit.Dp,kotlin.Function0))

Colab for Coroutine
[Colab](https://developer.android.com/codelabs/kotlin-coroutines)
[Code](https://github.com/googlecodelabs/kotlin-coroutines)

## Basic 5 RecyclerView
{: #upj_1676529122062}

[App 7-SleepTracker-with-RecyclerView App](https://github.com/udacity/andfun-kotlin-sleep-tracker-with-recyclerview)
([Code](https://github1s.com/udacity/andfun-kotlin-sleep-tracker-with-recyclerview))

[RecyclerView Doc](https://developer.android.com/jetpack/androidx/releases/recyclerview?hl=ko),
[RecyclerView.Adapter Doc](https://developer.android.com/reference/androidx/recyclerview/widget/RecyclerView.Adapter),
[RecyclerView로 동적 목록 만들기](https://developer.android.com/guide/topics/ui/layout/recyclerview?hl=ko),
[RecyclerView.ViewHolder Doc](https://developer.android.com/reference/androidx/recyclerview/widget/RecyclerView.ViewHolder),
[DiffUtil](https://developer.android.com/reference/kotlin/androidx/recyclerview/widget/DiffUtil),
[데이터 결합 라이브러리 Binding Adapters](https://developer.android.com/topic/libraries/data-binding?hl=ko),
[RecyclerView로 동적 목록 만들기](https://developer.android.com/guide/topics/ui/layout/recyclerview?hl=ko#customizing),



## Basic 6 Connect to the Internet
{: #upj_1676529125902}

---
title: Android 2-2
layout: upj_design
addr: /pre/android-2-2/
permalink: /pre/android-2-2/
---

#### Table Of Contents

- TOC
{:toc}

## Basic 4-1 App Architecture (UI Layer)
{: #upj_1676529112182}

[App 5-GuessIt App](https://github.com/udacity/andfun-kotlin-guess-it)
([Codes](https://github1s.com/udacity/andfun-kotlin-guess-it))

[Architecture Sample App](https://github.com/android/architecture-samples),
[MVP 패턴](https://medium.com/upday-devs/android-architecture-patterns-part-2-model-view-presenter-8a6faaae14a5),
[앱 아키텍처](https://developer.android.com/topic/architecture?hl=ko),
[ViewModel 개요](https://developer.android.com/topic/libraries/architecture/viewmodel?hl=ko),
[ViewModel Doc](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModel),
[ViewModel Simple Example App](https://medium.com/androiddevelopers/viewmodels-a-simple-example-ed5ac416317e),
[UI 상태 저장](https://developer.android.com/topic/libraries/architecture/saving-states?hl=ko),
[ViewModel Posts](https://medium.com/androiddevelopers/viewmodels-persistence-onsaveinstancestate-restoring-ui-state-and-loaders-fc7cc4a6c090),
[LiveData 개요](https://developer.android.com/topic/libraries/architecture/livedata?hl=ko),
[LiveData Doc](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData),
[LiveData Lifecycle](https://developer.android.com/topic/libraries/architecture/lifecycle?hl=ko),
[Backing properties](https://kotlinlang.org/docs/properties.html#backing-properties),
[Kotlin 스타일 가이드](https://developer.android.com/kotlin/style-guide?hl=ko#backing-properties),
[캡슐화](https://ko.wikipedia.org/wiki/%EC%BA%A1%EC%8A%90%ED%99%94),
[LiveData Observer](https://developer.android.com/topic/libraries/architecture/livedata?hl=ko#observe_livedata_objects),
[CountDownTimer Class Docs](https://developer.android.com/reference/kotlin/android/os/CountDownTimer),
[ViewModelFactory](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModelProvider.Factory.html),
[Factory 디자인패턴](https://en.wikipedia.org/wiki/Factory_(object-oriented_programming)),
[Factory 예제](https://cjw-awdsd.tistory.com/54),
[레이아웃 및 결합 표현식](https://developer.android.com/topic/libraries/data-binding/expressions?hl=ko),
[ViewModel - DataBinding 연결](https://developer.android.com/topic/libraries/data-binding/architecture?hl=ko#viewmodel),
[LiveData 자동업데이트](https://developer.android.com/topic/libraries/data-binding/architecture?hl=ko#livedata),
[문자열 Formatting](https://developer.android.com/guide/topics/resources/string-resource?hl=ko#formatting-strings),
[Layout Binding 수식](https://developer.android.com/topic/libraries/data-binding/expressions?hl=ko#resources),

```xml
 <Button
     android:id="@+id/correct_button"
     android:layout_width="wrap_content"
     android:layout_height="wrap_content"
     android:layout_marginEnd="16dp"
     android:onClick="@{() -> gameViewModel.onCorrect()}"
     android:text="@string/got_it"
     android:theme="@style/GoButton"
     app:layout_constraintBottom_toBottomOf="parent"
     app:layout_constraintEnd_toEndOf="parent"
     app:layout_constraintHorizontal_bias="0.5"
     app:layout_constraintStart_toEndOf="@+id/skip_button"
     app:layout_constraintTop_toTopOf="@+id/guideline" />
```

```xml
<!--string.xml-->
<string name="quote_format">\"%s\"</string>
<string name="score_format">Current Score: %d</string>

<!--UI xml file-->
 <TextView
     android:id="@+id/word_text"
     android:layout_width="wrap_content"
     android:layout_height="wrap_content"
     android:animateLayoutChanges="true"
     android:fontFamily="sans-serif"
     android:text="@{@string/quote_format(gameViewModel.word)}"
     android:textAppearance="@style/TextAppearance.AppCompat.Headline"
     android:textColor="@color/black_text_color"
     android:textSize="34sp"
     android:textStyle="normal"
     app:layout_constraintBottom_toTopOf="@+id/score_text"
     app:layout_constraintEnd_toEndOf="parent"
     app:layout_constraintHorizontal_bias="0.5"
     app:layout_constraintStart_toStartOf="parent"
     app:layout_constraintTop_toBottomOf="@+id/word_is_text"
     app:layout_constraintVertical_chainStyle="packed"
     tools:text="&quot;Tuna&quot;" />
```

```kotlin
val currentTimeString = Transformations.map(currentTime) { time ->
    DateUtils.formatElapsedTime(time)
}
```

```kotlin
binding.setLifecycleOwner(this)
```

[Android Permission](https://developer.android.com/guide/topics/permissions/overview?hl=ko),


## Basic 4-2 App Architecture (Persistence)
{: #upj_1676529117694}

[SQL Syntax on SQLite](https://www.sqlite.org/lang.html)

[App 6-SleepTracker App](https://github.com/udacity/andfun-kotlin-sleep-tracker)
([Code](https://github1s.com/udacity/andfun-kotlin-sleep-tracker))

[Room Doc](https://developer.android.com/jetpack/androidx/releases/room?hl=ko),
[Room 으로 데이터 정의하기](https://developer.android.com/training/data-storage/room/defining-data?hl=ko),
[Room 으로 로컬 데이터베이스에 저장](https://developer.android.com/training/data-storage/room?hl=ko),
[PrimaryKey](https://developer.android.com/reference/androidx/room/PrimaryKey),
[ColumnInfo](https://developer.android.com/reference/androidx/room/ColumnInfo),
[Index](https://developer.android.com/reference/androidx/room),
[Database](https://developer.android.com/reference/androidx/room/Database),
[Dao](https://developer.android.com/reference/androidx/room/Dao),
[Query](https://developer.android.com/reference/androidx/room/Query),
[Delete](https://developer.android.com/reference/androidx/room/Delete),
[Insert](https://developer.android.com/reference/androidx/room/Insert),

DAO Annotations

- @Insert
- @Delete
- @Update
- @Query

[RoomDatabase](https://developer.android.com/reference/androidx/room/RoomDatabase),
[RoomDatabase.Builder](https://developer.android.com/reference/androidx/room/RoomDatabase.Builder),
[Database](https://developer.android.com/reference/androidx/room/Database),
[RawQuery](https://developer.android.com/reference/androidx/room/RawQuery),
[싱글턴 패턴](https://ko.wikipedia.org/wiki/%EC%8B%B1%EA%B8%80%ED%84%B4_%ED%8C%A8%ED%84%B4),
[Volatile Synchronized 올바른 사용법](https://developer.android.com/topic/architecture?hl=ko#separation-of-concerns),
[Companion Object](https://kotlinlang.org/docs/object-declarations.html#Companion-Objects)

[Room 데이터베이스 이전](https://developer.android.com/training/data-storage/room/migrating-db-versions?hl=ko),
[About Room Migrations Blog](https://medium.com/androiddevelopers/understanding-migrations-with-room-f01e04b07929),
[Migrations Testing](https://medium.com/androiddevelopers/testing-room-migrations-be93cdb0d975)

[Android에서 앱 테스트](https://developer.android.com/training/testing?hl=ko),
[테스트 기본 요소](https://developer.android.com/training/testing/fundamentals?hl=ko)

테스트의 장점

- 장애에 관한 신속한 피드백
- 개발 주기에서 조기 장애 감지
- 회귀에 신경 쓸 필요 없이 코드를 최적화할 수 있도록 하는 더 안전한 코드 리랙터링
- 기술적 문제를 최소화하는 안정적인 개발 속도

[레이아웃 재사용: include, merge](https://developer.android.com/develop/ui/views/layout/improving-layouts/reusing-layouts?hl=ko)

[ViewModelProvider.Factory](https://developer.android.com/reference/androidx/lifecycle/ViewModelProvider.Factory),
[팩토리 메서드 패턴](https://ko.wikipedia.org/wiki/%ED%8C%A9%ED%86%A0%EB%A6%AC_%EB%A9%94%EC%84%9C%EB%93%9C_%ED%8C%A8%ED%84%B4),
[템플릿 메소드 패턴](https://ko.wikipedia.org/wiki/%ED%85%9C%ED%94%8C%EB%A6%BF_%EB%A9%94%EC%86%8C%EB%93%9C_%ED%8C%A8%ED%84%B4),
[Template Method Pattern Blog](https://yaboong.github.io/design-pattern/2018/09/27/template-method-pattern/),

Coroutines [Colab for Coroutine](https://developer.android.com/codelabs/kotlin-coroutines#0)

- Asynchronous: The coroutine runs independently from the main execution steps of your program.
- Non-blocking: The system is not blocking the main or UI thread. (suspend)
- Sequential code 

Coroutines need

- Job: A background job. Conceptually, a job is a cancellable thing with a life-cycle that culminates in its completion.
- Dispatcher: The dispatcher sends off coroutines to run on various threads.
- Scope: The scope combines information, including a job and dispatcher, to define the context in which the coroutine runs.

[SimpleDateFormat](https://developer.android.com/reference/java/text/SimpleDateFormat),
[Coroutines Doc](https://kotlinlang.org/docs/coroutines-overview.html),
[Coroutine context and dispatchers](https://kotlinlang.org/docs/coroutine-context-and-dispatchers.html),
[Dispatchers](https://kotlinlang.org/api/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/-dispatchers/),
[Job](https://kotlinlang.org/api/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/-job/),
[launch](https://kotlinlang.org/api/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/launch.html),
[Returns and jumps Expressions in Kotlin](https://kotlinlang.org/docs/returns.html#return-at-labels),
[HtmlCompat](https://developer.android.com/reference/androidx/core/text/HtmlCompat),
[CDATA](https://www.w3.org/TR/REC-xml/#sec-cdata-sect),
[Chracter Data](https://www.w3.org/TR/REC-xml/#dt-chardata),

[Navigation](https://developer.android.com/guide/navigation?hl=ko),
[Navigation Design Graph](https://developer.android.com/guide/navigation/navigation-design-graph?hl=ko),

[버튼](https://developer.android.com/guide/topics/ui/controls/button?hl=ko),
[아키텍처 구성요소에 레이아웃 뷰 결합](https://developer.android.com/topic/libraries/data-binding/architecture?hl=ko),
[Snackbar](https://developer.android.com/reference/kotlin/androidx/compose/material/package-summary#Snackbar(androidx.compose.ui.Modifier,kotlin.Function0,kotlin.Boolean,androidx.compose.ui.graphics.Shape,androidx.compose.ui.graphics.Color,androidx.compose.ui.graphics.Color,androidx.compose.ui.unit.Dp,kotlin.Function0))

Colab for Coroutine
[Colab](https://developer.android.com/codelabs/kotlin-coroutines)
[Code](https://github.com/googlecodelabs/kotlin-coroutines)

## Basic 5 RecyclerView
{: #upj_1676529122062}

[App 7-SleepTracker-with-RecyclerView App](https://github.com/udacity/andfun-kotlin-sleep-tracker-with-recyclerview)
([Code](https://github1s.com/udacity/andfun-kotlin-sleep-tracker-with-recyclerview))

[RecyclerView Doc](https://developer.android.com/jetpack/androidx/releases/recyclerview?hl=ko),
[RecyclerView.Adapter Doc](https://developer.android.com/reference/androidx/recyclerview/widget/RecyclerView.Adapter),
[RecyclerView로 동적 목록 만들기](https://developer.android.com/guide/topics/ui/layout/recyclerview?hl=ko),
[RecyclerView.ViewHolder Doc](https://developer.android.com/reference/androidx/recyclerview/widget/RecyclerView.ViewHolder),


## Basic 6 Connect to the Internet
{: #upj_1676529125902}

## Basic 7 Behind the Scenes
{: #upj_1676529133902}

## Basic 8 Designing for Everyone
{: #upj_1676529137671}

## Basic 7 Behind the Scenes
{: #upj_1676529133902}

## Basic 8 Designing for Everyone
{: #upj_1676529137671}

