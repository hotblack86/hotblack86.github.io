# video-gallery

Video gallery

A custom element that displays a collection of videos in a video gallery.

## Example

```html
<caption>Basic usage</caption>
<video-gallery>
<video-gallery-stage class="home-video__stage">
<div class="o-ratio o-ratio--16:9">
<div class="o-ratio__content">
<video-gallery-slide
 class="home-video__stage-video is-active"
 id="video-gallery-slide--1"
>
</video-gallery-slide>
<video-gallery-slide
 class="home-video__stage-video"
 id="video-gallery-slide--2"
>
</video-gallery-slide>
<video-gallery-slide
 class="home-video__stage-video"
 id="video-gallery-slide--3"
>
</video-gallery-slide>
</div>
</div>
</video-gallery-stage>

<video-gallery-thumbnails class="home-video__items">
<video-gallery-thumbnail class="home-video__item is-active">
<button
type="button"
class="home-video__item-link"
data-target-id="video-gallery-slide--{{ block.id }}"
>
<div class="o-ratio o-ratio--16:9">
 <div class="o-ratio__content">
   <img
     class="home-video__item-img"
     src="https://img.youtube.com/vi/[external_video_id]/mqdefault.jpg"
     alt="Video 1 trigger image"
     loading="lazy"
   >
   <div class="home-video__item-img--overlay u-bg-overlay"></div>
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center">
     {%- assign icon_title = 'sections.video.play_label' | t -%}
     {%- render 'icons-theme', icon: 'play', title: icon_title -%}
   </div>
 </div>
</div>
</button>
</video-gallery-thumbnail>
<video-gallery-thumbnail class="home-video__item">
<button
type="button"
class="home-video__item-link"
data-target-id="video-gallery-slide--2"
>
<div class="o-ratio o-ratio--16:9">
 <div class="o-ratio__content">
   <img
     class="home-video__item-img js-vimeo-thumb"
     src="#"
     alt="Video 2 trigger image"
     loading="lazy"
     data-vimeo-id="123456789"
     style="opacity: 0"
   >
   <div class="home-video__item-img--overlay u-bg-overlay"></div>
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center">
     {%- assign icon_title = 'sections.video.play_label' | t -%}
     {%- render 'icons-theme', icon: 'play', title: icon_title -%}
   </div>
 </div>
</div>
</button>
</video-gallery-thumbnail>
<video-gallery-thumbnail class="home-video__item is-active">
<button
type="button"
class="home-video__item-link"
data-target-id="video-gallery-slide--{{ block.id }}"
>
<div class="o-ratio o-ratio--16:9">
 <div class="o-ratio__content">
   <img
     class="home-video__item-img"
     src="{{ video_file.preview_image | image_url: width: 300 }}"
     alt="Video 3 trigger image"
     loading="lazy"
     width="300"
     height="{{ 300 | divided_by: video_file.preview_image.aspect_ratio | round }}"
   >
   <div class="home-video__item-img--overlay u-bg-overlay"></div>
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center">
     {%- assign icon_title = 'sections.video.play_label' | t -%}
     {%- render 'icons-theme', icon: 'play', title: icon_title -%}
   </div>
 </div>
</div>
</button>
</video-gallery-thumbnail>
</video-gallery-thumbnails>
</video-gallery>
```

## Methods

| Method         | Type                                  | Description                                      |
|----------------|---------------------------------------|--------------------------------------------------|
| `#handleClick` | `(e: any): void`                      |                                                  |
| `changeSlide`  | `(videSlideId: number): VideoGallery` | Change slide<br /><br />**videSlideId**: ID of the target slide |


# video-gallery-thumbnail

Video Gallery Thumbnail

A custom element that handles the display of a Vimeo video thumbnail in a video gallery.
