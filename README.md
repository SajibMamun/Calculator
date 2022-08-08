# Calculator
Design use Neumorphism material

Process:

# Dependency
Add this in your root build.gradle file (not your module build.gradle file):


allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}



Then, add the library to your module build.gradle



dependencies {
    implementation 'com.github.fornewid:neumorphism:{latest_version}'
}




# Design Process
<soup.neumorphism.NeumorphCardView
    // Pre-defined style
    style="@style/Widget.Neumorph.CardView"

    // Set shadow elevation and colors
    app:neumorph_shadowElevation="6dp"
    app:neumorph_shadowColorLight="@color/solid_light_color"
    app:neumorph_shadowColorDark="@color/solid_dark_color"

    // Set light source
    app:neumorph_lightSource="leftTop|leftBottom|rightTop|rightBottom"

    // Set shape type and corner size
    app:neumorph_shapeType="{flat|pressed|basin}"
    app:neumorph_shapeAppearance="@style/CustomShapeAppearance"

    // Set background or stroke
    app:neumorph_backgroundColor="@color/background_color"
    app:neumorph_strokeColor="@color/stroke_color"
    app:neumorph_strokeWidth="@dimen/stroke_width"

    // Use a inset to avoid clipping shadow. (default=12dp)
    app:neumorph_inset="12dp"
    app:neumorph_insetStart="12dp"
    app:neumorph_insetEnd="12dp"
    app:neumorph_insetTop="12dp"
    app:neumorph_insetBottom="12dp"

    // Use a padding. (default=12dp)
    android:padding="12dp">

    <!-- NeumorphCardView extends FrameLayout. So you can wrap childrens like this. -->
    <ConstraintLayout />
</soup.neumorphism.NeumorphCardView>

<style name="CustomShapeAppearance">
    <item name="neumorph_cornerFamily">{rounded|oval}</item>
    <item name="neumorph_cornerSize">32dp</item>

    <!-- Or if wants different radii depending on the corner. -->
    <item name="neumorph_cornerSizeTopLeft">16dp</item>
    <item name="neumorph_cornerSizeTopRight">16dp</item>
    <item name="neumorph_cornerSizeBottomLeft">16dp</item>
    <item name="neumorph_cornerSizeBottomRight">16dp</item>
</style>
