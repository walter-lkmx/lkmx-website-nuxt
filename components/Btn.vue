<template>
  <nuxt-link class="btn" :to="url" :class="[color, !shortcut ? shortcut : `shortcut--${shortcut}`]">
    <p ref="text"></p>
  </nuxt-link>
</template>

<script>
  export default {
    props: {
      color: {
        type: String,
        required: false,
        default: 'blue',
      },
      text: {
        type: String,
        required: true,
      },
      shortcut: {
        type: String,
        default: '0',
        required: false,
      },
      url: {
        type: String,
        required: false,
      },
    },
    methods: {
      getText() {
        let slicedText = [];
        slicedText = [...this.text.split(/\s+/)];
        const getShortcut = function (shortcut) {
          let shortcutNumber = Number(shortcut);
          return shortcutNumber;
        };
        getShortcut(this.shortcut);
        let str = '';
        for (let i = 0; i < slicedText.length; i++) {
          let firstLetter = Object.values(slicedText[i].slice(0, 1)).join('');
          let lastLetters = Object.values(slicedText[i].slice(1)).join('');
          let joined = `<span class="shortcut--${i+1}">${firstLetter}</span>` + `${lastLetters} `;
          str += joined
          // console.log(str);
          this.$refs.text.innerHTML = str;
        }
      },
    },
    mounted() {
      this.getText();
    }
  }

</script>

<style lang="scss">
  .btn {
    padding: 11px 20px;
    text-decoration: none;
    max-width: fit-content;
    &.blue {
      background: var(--color-accent-cyan);
      color: var(--color-neutral-black);

      &:visited {
        color: var(--color-neutral-black);
      }
      &:active {
        p {
          color: var(--color-neutral-white);
        }

        background: var(--color-accent-blue-02);
      }
    }

    &.pink {
      background: var(--color-accent-pink);
      color: var(--color-neutral-white);

      &:visited {
        color: var(--color-neutral-white);
      }

      &:hover {
        p {
          color: var(--color-neutral-white);
        }
      }
      &:active {
        p {
          color: var(--color-neutral-white);
        }

        background: var(--color-accent-blue-02);
      }
    }
    &.shortcut {
      @for $i from 1 through 5 {
        &--#{$i} {
          &:hover {
          span.shortcut--#{$i} {
              text-decoration: underline;
              font-weight: 700;
            }
          }
          &:active {
          span.shortcut--#{$i} {
              text-decoration: underline;
              font-weight: 700;
              color: var(--color-accent-yellow);
            }
          }
        }
      }
    }
  }

</style>
