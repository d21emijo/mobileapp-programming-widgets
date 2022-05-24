
# Rapport dugga 3-widgets

- [x]    Add a layout of your choice, e.g. `LinearLayout` or `ConstraintLayout`
- [x]    Add at least three different widgets inside that layout, e.g. `EditText`, `ImageView`, and `Button` and use at least the margin attribute
- [x]    Position the widgets in a different way than the way they first appeared when added to the layout

för att skapa en constraint layout så har 2 st olika constraintlayouts använts som "lådor" den ena röd med en textview en bild och en ratingbar,
den andra gröna "lådan" med en kanpp i.

![image](https://user-images.githubusercontent.com/102797583/166894650-52e3241f-b818-4442-8218-30ae7d1e2831.png)


## constraint 1 textview , imgview , RatingBar
```
    <androidx.constraintlayout.widget.ConstraintLayout
        android:id="@+id/constraintLayout"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:layout_marginStart="32dp"
        android:layout_marginLeft="32dp"
        android:layout_marginTop="32dp"
        android:layout_marginEnd="32dp"
        android:layout_marginRight="32dp"
        android:layout_marginBottom="260dp"
        android:background="#5C0606"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent">
```
i den första constraintlayouten ovan där färgen är röd har bild, rating och text -views nestlats in i activity_main.xml filen.

## constraint 2 grön -knapp
```
    <androidx.constraintlayout.widget.ConstraintLayout
        android:id="@+id/constraintLayout2"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:layout_marginStart="32dp"
        android:layout_marginLeft="32dp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="32dp"
        android:layout_marginRight="32dp"
        android:layout_marginBottom="120dp"
        android:background="#217C5C"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/constraintLayout">

        <Button
            android:id="@+id/button2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:shadowColor="@android:color/background_dark"
            android:shadowDx="10"
            android:shadowDy="0"
            android:shadowRadius="5"
            android:text="Button"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent" />
    </androidx.constraintlayout.widget.ConstraintLayout>
```
på samma sätt som i den röda constrainlayouten är också den gröna layouten med knappen uppbyggd där layouten (lådan) där constrainlayouten är parent till button.

för att justera hur dessa sitter i appen används constraints inom den lådan de tillhör och margins,
(ex : android:layout_marginBottom="120dp", och app:layout_constraintTop_toBottomOf="@+id/constraintLayout">).

