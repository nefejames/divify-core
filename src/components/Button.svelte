<script>
  export let buttonCopy = "";
  export let isPrimaryBtn;
</script>

<button class:primaryBtn={isPrimaryBtn}>{buttonCopy}</button>

<style>
  button {
    color: var(--btn-color);
    padding: 0.7rem 1.4rem;
    cursor: pointer;
    border: none;
    background: var(--secondary-color);
    border-radius: 8px;
    outline: none;
    font-size: 1.2rem;
    font-weight: 200;
    box-shadow: var(--box-shadow);
  }

  .primaryBtn {
    background: var(--primary-color);
    margin-right: 0.7rem;
  }
</style>
