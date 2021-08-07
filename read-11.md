Images, Audio, & Video
In this Lesson7
HTML
Adding Images
Adding Audio
Adding Video
Figure & Caption
CSS
Sizing Images
Positioning Images
Users browse the internet in search of interesting and informational content, commonly found in the form of plain text. To accompany this plain text, HTML provides a way to give users rich media in the form of images, audio tracks, and videos.

The ability to include images, audio tracks, and videos within websites has been around for some time. Browser support for images has generally been pretty good, while audio and video support has left something to be desired. With the help of new technology, and the push of social media, more and more audio tracks and video clips have made their way online.

Today, we can freely use images, audio, and video knowing that support is widely accepted across all major browsers with the addition of HTML5 and the help of Flash alternatives.

Adding Images
To begin adding images to a page the img inline element is used. The img element is self containing, in that it doesn’t wrap any other content and exists as a single tag. For the img element to work, a src attribute value must be included to specify the source of the requested image. The src attribute value comes in way of a URL, most often relative to the server upon which the website is hosted.

In conjunction with the src attribute the alt attribute, known as alternative text, should be applied. The alt attribute value is displayed in place of the image should the image not be available. Also, the alt text is the cursor tooltip text that may be shown when hovering over the image.

<img src="cows.jpg" alt="Brown and white cows in a field">
Adding an Image Demo
Brown and white cows in a field
Supported Image Formats
Images come in a variety of different file formats, and each browser may choose to support a given file format or not. By and large, the most commonly supported file formats online include bmp, gif, jpg, and png. Of these, the most widely used formats today include jpg and png. jpg formatted images offer a quality looking image with high color counts while still being able to scale the file size for faster load times. png formatted images are great for images with transparencies or low color counts.

Sizing Images
There are a couple of different ways to size images so that they work well on a page. One option is to use the height and width attributes directly within the img tag in HTML. While this works, it also puts styles in the HTML. Since styles should specifically be reserved for CSS, let’s use the CSS height and width properties instead.

Specifying either a height or width will automatically adjust the other dimension to maintain the aspect ratio of the image. As an example, if I wanted an image to be 200 pixels tall, but didn't mind how wide it was, I could set the height to 200px and the width of the image would automatically adjust accordingly. Setting both a height and width will work as well, however doing so may also break the aspect ratio of an image causing it to appear contorted.

Before getting too excited about resizing images with HTML or CSS it is worth noting that images should be resized to their desired height and width outside of the browser if possible. Taking a 1,000 pixel wide image and dropping it down to 100 pixels wide in the browser still means the original image, all 1,000 pixels, will need to be loaded and then scaled down. This is a less than ideal solution and can cause a large load time, especially on mobile devices.

img {
  height: 200px;
  width: 200px;
}
Sizing an Image Demo
Brown and white cows in a grass field
Positioning Images
Images can be positioned in quite a few different ways, including inline, block, flush left, flush right, and so on. All of these positions are obtained using the CSS float property, along with other box model properties including margin, padding, border, and display.

Inline Positioning Images
The img element by default is an inline level element. Adding an image to a page without any styles will position that image directly in place while all the other content will fall inline with it as necessary, as seen below.

<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis  nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute <img src="images-audio-video/cows.jpg" alt="Brown and white cows in a grass field"> irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
Inline Positioning an Image Demo
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute Brown and white cows in a grass field irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Leaving images in their default positioning isn’t very common. Most often images are set to be displayed as block level elements or floated flush to one side. Using a small image inline with text should only be done when the image holds actual value to the page and has an appropriate alternative text. If an image, or icon, is used as part of the user interface or for decoration, it should be added to the page as a CSS background image.

Block Positioning Images
Adding the CSS property display and setting its value to block forces the image to be a block level element. Doing so makes the image appear on its own line, leaving the surrounding content to be positioned above and below the image.

img {
  display: block;
}
Block Positioning an Image Demo
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis auteBrown and white cows in a grass fieldirure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Positioning Images Flush Left or Right
Sometimes displaying an image as inline or block isn’t the ideal DKge. You may want the image to appear flush to the left or right while letting all of the other content surround the image as necessary. To do this the CSS float property is used with the value of either left or right.

Floating an image is a start, but all of the other content will align directly up against it. To provide an adequate amount of spacing around an image the margin property is used. Additionally, we can use the padding, border, and background properties to build a frame for the image if desired.

img {
  background: #e8eae9;
  border: 1px solid #c6c9cc;
  float: right;
  margin: 8px 0 0 20px;
  padding: 4px;
}
Floating & Framing an Image Demo
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute Brown and white cows in a grass fieldirure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Mauris ut lectus quis mauris ornare iaculis a vel ligula. Quisque sed est sed arcu tincidunt aliquet. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nam posuere accumsan mauris, nec lacinia risus pretium et. Suspendisse eget nisi facilisis nisl tristique consequat. Vivamus scelerisque accumsan vulputate. Sed bibendum felis id dui ornare tincidunt. Sed a pretium nisl.

Adding Audio
HTML5 provides a quick and easy way to add audio and video files to be played on a website. Using the audio element an audio clip can be added to a page. Just as with the img element, an audio element also needs a source URL specified via the src attribute.

<audio src="images-audio-video/jazz.ogg"></audio>
To accompany the src attribute on the audio element there are a handful of other attributes that may be used, the most popular of which include autoplay, controls, loop, and preload.

By default the audio element doesn’t show up on the page. If the Boolean attribute autoplay were passed in, nothing would be shown on the page, however the audio clip would automatically start playing upon loading the page. As a Boolean, the autoplay attribute serves as a toggle function. It will toggle the audio on or off when the page loads.

To actually show the audio element on the page, use the Boolean attribute controls. The controls attribute will show the default browser controls including play and pause, seeking, and volume.

<audio src="images-audio-video/jazz.ogg" controls></audio>
Adding Audio Demo
The loop attribute is also a Boolean attribute available to the audio element. Adding the loop attribute will repeat the audio clip endlessly, from beginning to end.

Lastly, the preload attribute has three different values, including none, auto, and metadata. The none value will not preload any information or data regarding the audio clip, while the auto value will preload all information and data. The metadata value will preload media information about the clip, such as the length. The preload attribute is useful in the case that users might not actually need or want to listen to an audio clip. It helps save on bandwidth and allows the page to load faster for non-essential audio clips.

Audio Fallbacks
Different browsers may support different audio formats and some may not support audio at all. In this case we can list multiple audio fallbacks including different audio file formats, a Flash alternative, or the option to directly download the audio clip.

To start, using the HTML5 audio element we can specify different file formats using multiple sources via the source element. The source element works in conjunction with the src and type attributes. The src attribute specifies the source URL while the type attribute specifies the MIME-type of the audio clip, helping browsers better understand the audio clip format.

Some browsers will not support the HTML5 audio element at all, in which case a Flash player fallback may be used. There are many different Flash players out there so you will need to research which one will work best for you. Two popular available options include SWFObject and Flowplayer.

<audio controls>
  <source src="jazz.ogg" type="audio/ogg">
  <source src="jazz.mp3" type="audio/mpeg">
  <object type="application/x-shockwave-flash" data="player.swf?audio=jazz.mp3">
    <param name="movie" value="player.swf?audio=jazz.mp3">
    <p>This browser does not support the audio format. Please <a href="jazz.mp3" title="Jazz song">download</a> the audio clip.</p>
  </object>
</audio>
To cover every browser, including the ones that do not support ogg or mp3 audio formats and do not have a Flash plug-in installed, a link to simply download the audio clip is included. This link is placed within the Flash player code as a last case scenario should Flash not be available.

Adding Video
Adding in HTML5 videos is very similar to that of adding in audio. In this case however, we use the video element in place of the audio element. All of the same attributes (source, autoplay, controls, loop, and preload) and fallbacks apply here too.

With audio, if the controls Boolean attribute wasn’t specified the audio clip wouldn’t be shown. With videos, not specifying the controls attribute shows the video, however doesn’t provide any way to play it unless the autoplay Boolean attribute is also applied. Best practice here would be to include the controls attribute unless there is good a reason not to allow users to start, stop, or replay the video.

Since videos will be displayed on the page it doesn’t hurt to specify dimensions, most commonly with a fixed height or width in CSS. This helps ensure that the video isn’t too large and stays within the implied layout of a page. Additionally, specifying a size helps browsers render the videos faster and allows them to allocate the proper space needed for the video to be shown.

<video src="earth.ogv" controls></video>
Adding Video Demo
Customizing Audio & Video Controls
By default audio and video controls are determined by each browser independently. Depending on the website more control over the look and feel of the media player may be needed. In this case a customized player can be built, but requires a little bit of JavaScript to get the player working.

Poster Attribute
One additional attribute available on the video element is the poster attribute. The poster attribute allows you to specify an image, in the form of a URL, to be shown before video is played. A poster image could be a still frame from the video or any other desired image. While not practical, the example below uses the picture of cows as the poster for the Earth video.

<video src="earth.ogv" controls poster="cows.jpg"></video>
