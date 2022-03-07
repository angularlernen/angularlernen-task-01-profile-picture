A basic _profile picture_ Component
===================================

### Introduction

Components are fundamental building blogs in an Angular App.

Let's create one!

### Task

Create a _ProfilePictureComponent_ for representing a profile picture as a circle.

### HOWTOs

1. Run the comand `ng g c profile-picture`
2. Open the file `profile-picture.component.html`
3. Your html markup should represent an image with a frame.

```html
<div class="profilePicture">
  <img src="https://randomuser.me/api/portraits/women/29.jpg">
</div>
```

Hint: you can use https://randomuser.me/ to choose a random user picture.

4. Use the newly created component in the `app.component.html`.

5. Edit the `profile-picture.component.scss` file in order to give the component its specific circular look.

```css
$diameter: 120px;

$frame-color: white;
$frame-width: 5px;

$border-color: gray;
$border-width: 2px;

.profilePicture {
  display: flex;
  justify-content: center;
  align-items: center;
  
  cursor: pointer;

  background-color: $frame-color;
  
  width: $diameter;
  height: $diameter;
  border-style: solid;
  border-width: $border-width;
  border-color: $border-color;
  
  border-radius: 50%;

  img {
    object-fit: contain;
    width: $diameter - $frame-width;
    height: $diameter - $frame-width;

    border-radius: 50%;

    &:hover {
      filter: brightness(90%);
    }
  }
}
```