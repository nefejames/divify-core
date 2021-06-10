<script>
  export let buttonCopy = "";
  export let isPrimaryBtn;
</script>

<button class:primaryBtn={isPrimaryBtn}>{buttonCopy}</button>

<style>
  button {
    /* color: #0d0c22; */
    padding: 0.7rem 1.4rem;
    cursor: pointer;
    border: none;
    background: #ea4c89;
    border-radius: 8px;
    outline: none;
    font-size: 1.2rem;
    font-weight: 400;
    box-shadow: 0px 0px 0px 1px #e7e7e9 inset;
  }

  .primaryBtn {
    background: #215ee9;
    margin-right: 0.7rem;
  }
</style>
