<script>
export default {
    name: "Membership"
}
</script>

<template>
    <section id="membership">
        <div class="ms_container">
            <div class="row row-cols-2">

                <!-- COLUMN LEFT -->
                <div class="col">
                    <img src="../../assets/images/home_img-compressor.jpg" alt="Membership Image">
                </div>

                <!-- COLUMN RIGHT -->
                <div class="col">
                    <h5 class="text-white mb-4">Sign Up For A Free Training Session!</h5>

                    <!-- FORM -->
                    <form>

                        <!-- Name -->
                        <div class="form-group">
                            <label class="text-secondary mb-2" for="exampleInputPassword1">Name *</label>
                            <input type="name" class="form-control ms_form mb-3" id="exampleInputName"
                                aria-describedby="nameHelp">
                            <small id="nameHelp" class="form-text text-muted"></small>
                        </div>

                        <!-- Email -->
                        <div class="form-group">
                            <label class="text-secondary mb-2" for="exampleInputEmail1">Email </label>
                            <input type="email" class="form-control ms_form mb-5" id="exampleInputEmail1"
                                aria-describedby="emailHelp">
                            <small id="emailHelp" class="form-text text-muted"></small>
                        </div>

                        <!-- Button -->
                        <button type="submit" class="btn">START NOW!</button>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    background-color: $grey_secondary;

    .ms_container {

        .col {
            padding: 20px;

            img {
                transition: .5s ease-in-out;
                cursor: pointer;
            }

            img:hover {
                scale: 1.04;
                box-shadow: 0 0 8px $red_primary;
            }

            h5 {
                font-weight: 700;
            }

            form {

                .ms_form {
                    background-color: $grey_secondary;
                    border-radius: 0;
                    transition: background-color 0.5s ease;
                }

                .ms_form:focus {
                    background-color: white;
                }

                .btn {
                    background-color: $red_primary;
                    border-radius: 0;
                    width: 100%;
                    color: $grey_primary;
                    transition: color 0.2s ease-in-out;
                }

                .btn:hover {
                    color: white;
                }
            }
        }
    }
}</style>