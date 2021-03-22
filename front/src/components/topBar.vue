<template>
  <div class="row mt-5 d-flex justify-content-center align-items-center">
    <div class="col-lg-3 col-xs-12">
      <img
        src="../assets/img/logo.png"
        width="69px"
        height="14px"
        alt="Windbnb"
      />
    </div>
    <div class="col-lg-5 col-xs-12"></div>
    <div class="col-lg-4 col-xs-12 d-flex justify-content-end">
      <div class="box-search font-mulish">
        <input
          class="input-search"
          type="text"
          placeholder="Helsinki, Finland"
        />
        <input class="input-guest" placeholder="Add guests" type="text" />
        <div class="icon-search">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-search"
            viewBox="0 0 16 16"
          >
            <path
              d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.box-search {
  width: 297px;
  height: 55px;
  border-radius: 16px;
  background-color: #fff;
  box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: row;
}

.input-search {
  width: 45%;
  font-size: 14px;
  text-align: center;
  border: none;
  border-top-left-radius: 16px;
  border-bottom-left-radius: 16px;
}

input {
  outline: none;
}

.input-search input:focus {
  outline: none;
}

.input-guest {
  width: 40%;
  border: none;
  border-left: 1px solid #f2f2f2;
  border-right: 1px solid #f2f2f2;
  font-size: 14px;
  text-align: center;
}

.input-guest:placeholder {
  color: #bdbdbd;
}

.icon-search {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 15%;
  color: #eb5757;
  font-weight: bold;
}
</style>