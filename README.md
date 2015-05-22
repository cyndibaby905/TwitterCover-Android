## TwitterCover-Android ##

The Android version of [TwitterCover](https://github.com/cyndibaby905/TwitterCover)


## Requirements ##

Android 4.2 Jelly Bean +

Or Android 4.0 Ice Cream Sandwich + if you don't use [RenderScript](http://developer.android.com/guide/topics/renderscript/compute.html)


## How to use ##
	
*For a working implementation, Have a look at the Sample Project - app*

1. Include the library as local library project.

    ``` compile project(':twittercover') ```

2. Include the TwitterCoverListView in your layout.

	```xml
    <com.example.hangchen.twittercover.TwitterCoverListView
        android:id="@+id/layout_listview"
        android:dividerHeight="1dp"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        />
    ```

3. In your `onCreate` method refer to the View and setup header image.
	```java
    TwitterCoverListView listView = (TwitterCoverListView) findViewById(R.id.layout_listview);
        listView.setHeaderImage(BitmapFactory.decodeResource(getResources(), R.drawable.img_header));

        ArrayAdapter<String> adapter = new ArrayAdapter<String>(this,
                android.R.layout.simple_expandable_list_item_1,
                new String[]{
                        "Item 1", "Item 2", "Item 3", "Item 4", "Item 5",
                        "Item 6", "Item 7", "Item 8", "Item 9", "Item 10",
                        "Item 11", "Item 12", "Item 13", "Item 14", "Item 15",
                        "Item 16", "Item 17", "Item 18", "Item 19", "Item 20"
                }
        );
        listView.setAdapter(adapter);
     ```  

## How it looks ##

![TwitterCover-Android] (https://raw.githubusercontent.com/cyndibaby905/TwitterCover-Android/master/twittercover.gif)


## Thanks ##

* [Stack Blur](http://www.quasimondo.com/StackBlurForCanvas/StackBlurDemo.html) from [Mario Klingemann](http://incubator.quasimondo.com)


## Lincense ##

`TwitterCover-Android` is available under the MIT license. See the LICENSE file for more info.

