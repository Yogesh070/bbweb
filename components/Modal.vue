<template>
  <div>
      <transition name="modal">
        <div class="modal-mask">
          <div class="modal-wrapper">
            <div class="modal-container scrollbar">

              <div class="modal-header">
                <slot name="header">
                  <h1>{{service[activeOption].title}}</h1>
                </slot>
              </div>

              <div class="modal-body">
                <slot name="body">
                  <p>{{service[activeOption].summary}}</p>
                </slot>
              </div>

              <div class="modal-footer">
                <slot name="footer">
                  <button class="modal-default-button primary-button" @click="$emit('close')">
                    Close
                  </button>
                </slot>
              </div>
            </div>
          </div>
        </div>
      </transition>
  </div>
</template>

<script>
export default {
data() {
    return {
        
    }
},
props: {
    activeOption:Number,
    service:Array,
},
}
</script>

<style lang="scss" scopedß>

.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-container {
  /* width: 300px; */
  width: 60vw;
  height: 50vh;
  margin: 0px auto;
  padding: 20px 40px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.4s ease;
  display: grid;
  align-items: center;
  text-align: center;
  overflow: scroll;
}

.modal-header h3 {
  margin-top: 0;
  color: $base-color;
}

.modal-body {
  margin: 20px 0;
}

.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
  transition: all 1s ease-in-out;
}

</style>