# video-gallery

Video gallery

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
 {% render 'video-player',
   id: 'video-player-1',
   video_type: "youtube",
   external_video_id: "1234567789",
   poster_image: preview_image_object,
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}
</video-gallery-slide>
<video-gallery-slide
 class="home-video__stage-video"
 id="video-gallery-slide--2"
>
 {% render 'video-player',
   id: 'video-player-2',
   video_type: "vimeo",
   external_video_id: "1234567789",
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}
</video-gallery-slide>
<video-gallery-slide
 class="home-video__stage-video"
 id="video-gallery-slide--3"
>
 {% render 'video-player',
   id: 'video-player-1',
   video_type: 'html5',
   video: video,
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}
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
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center icon-fallback">
     <i class="icon icon--play" aria-hidden="true"></i>
     <span class="icon-fallback__text">{{ 'sections.video.play_label' | t }}</span>
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
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center icon-fallback">
     <i class="icon icon--play" aria-hidden="true"></i>
     <span class="icon-fallback__text">{{ 'sections.video.play_label' | t }}</span>
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
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center icon-fallback">
     <i class="icon icon--play" aria-hidden="true"></i>
     <span class="icon-fallback__text">{{ 'sections.video.play_label' | t }}</span>
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

## Methods

| Method                  | Type                |
|-------------------------|---------------------|
| `#updateVimeoThumbnail` | `(): Promise<void>` |
