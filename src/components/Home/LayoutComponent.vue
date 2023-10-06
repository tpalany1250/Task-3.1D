<!-- <template>
    <video width="100%" controls>
    <source src="video/Bugatti.mp4" type="video/mp4">
    Your browser does not support the video tag.
    </video>
</template> -->


<template>
    <div>
      <!-- Video element and other common content -->
      <video width="100%" controls>
        <source src="video/Bugatti.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <!-- Other common content here -->
      <router-view></router-view>
    </div>
  </template>