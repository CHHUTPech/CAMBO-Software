<template>
  <div class="card">
    <div class="card__head">
      <svg width="32" height="32" viewBox="0 0 24 24">
        <path
          fill="currentColor"
          d="M3.75 19.75q-.325-.325-.325-.75t.325-.75L9.8 12.2q.15-.15.325-.213q.175-.062.375-.062t.375.062q.175.063.325.213l3.3 3.3l6.4-7.2q.275-.325.713-.325q.437 0 .737.3q.275.275.288.663q.012.387-.263.687L15.2 17.7q-.15.175-.337.262q-.188.088-.388.088t-.387-.075q-.188-.075-.338-.225L10.5 14.5l-5.25 5.25q-.325.325-.75.325t-.75-.325ZM4 13.3q-.125 0-.25-.063q-.125-.062-.2-.212l-.5-1.075l-1.075-.5q-.15-.075-.212-.2Q1.7 11.125 1.7 11t.063-.25q.062-.125.212-.2l1.075-.5l.5-1.075q.075-.15.2-.213Q3.875 8.7 4 8.7t.25.062q.125.063.2.213l.5 1.075l1.075.5q.275.125.275.45t-.275.45l-1.075.5l-.5 1.075q-.075.15-.2.212q-.125.063-.25.063Zm11-2q-.125 0-.25-.063q-.125-.062-.2-.212l-.5-1.075l-1.075-.5q-.15-.075-.212-.2Q12.7 9.125 12.7 9t.063-.25q.062-.125.212-.2l1.075-.5l.5-1.075q.075-.15.2-.213q.125-.062.25-.062t.25.062q.125.063.2.213l.5 1.075l1.075.5q.15.075.213.2q.062.125.062.25t-.062.25q-.063.125-.213.2l-1.075.5l-.5 1.075q-.075.15-.2.212q-.125.063-.25.063Zm-6.5-3q-.125 0-.25-.075T8.05 8L7.4 6.6L6 5.95q-.15-.075-.225-.2Q5.7 5.625 5.7 5.5t.075-.25q.075-.125.225-.2l1.4-.65l.65-1.4q.075-.15.2-.225q.125-.075.25-.075t.25.075q.125.075.2.225l.65 1.4l1.4.65q.15.075.225.2q.075.125.075.25t-.075.25q-.075.125-.225.2l-1.4.65L8.95 8q-.075.15-.2.225q-.125.075-.25.075Z"
        />
      </svg>
    </div>
    <div class="card__body">
      <h3>{{ name }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    logo: String,
  },
}
</script>

<style scoped>
.card {
  padding: 0.5rem;
  margin: 0.5rem;
  border: 1px solid white;
  transition: all 0.5s;
  border-radius: 0.2rem;
  display: grid;
  width: 250px;
  grid-template-rows: 1fr 1fr;
  cursor: grabbing;
}
.card:hover {
  border: 1px solid #cc8e1a;
  transition: all 0.5s;
  box-shadow: 0px 0px 11px 0px rgba(0, 70, 145, 0.75);
  -webkit-box-shadow: 0px 0px 11px 0px rgba(0, 70, 145, 0.75);
  -moz-box-shadow: 0px 0px 11px 0px rgba(0, 70, 145, 0.75);
}
.card > div {
  text-align: center;
}
.card div > svg {
  width: 80px;
  height: 80px;
  transition: all 0.7s;
  color: #cc8e1a;
}
.card:hover div > svg {
  transition: all 0.7s;
  color: white;
}
.card div h3 {
  color: white;
  font-size: 1.5rem;

  transition: all 0.7s;
}
.card:hover div h3 {
  /* font-size: 30px; */
  color: #cc8e1a;
}

.card__head {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  /* outline: 1px solid red; */
}
.card__body {
  /* outline: 1px solid green; */

  max-height: 100%;
  overflow-y: hidden;
}
</style>
