<template>
    <el-container class="login-container align-item-center">
        <el-row 
            :span='24' 
            class="login-form"
        >
            <h2>{{ $t('login.title') }}</h2>
            <el-col 
                :xs='24'
                :sm='24'
                :md='12' 
                :lg='12'
                :xl='12'
            >
                <div class="login-card">
                    <el-form ref="form">
                        <el-form-item :label="$t('login.form.account')">
                            <el-input></el-input>
                        </el-form-item>
                        <el-form-item :label="$t('login.form.password')">
                            <el-input 
                                type="password"
                                autocomplete="off"
                            ></el-input>
                        </el-form-item>
                    </el-form>
                    <el-row :span='24' class='mb-22'>
                        <el-checkbox>{{ $t('login.button.remember_me') }}</el-checkbox>
                    </el-row>
                    <el-row :span='24'>
                        <el-button type='primary'>{{ $t('login.button.login') }}</el-button>
                    </el-row>
                </div>
            </el-col>
        </el-row>
    </el-container>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
@import '../scss/base.scss';

.login-container {
    height: 100vh;
    background-image: url('../assets/images/working.png');
    background-image: url('../assets/images/working.png'), linear-gradient(#fff,#f8f9fe);
    background-size: 50%;
    background-repeat: no-repeat;
    background-position: right center;
    display: flex;

    @include mobile() {
        background-size: contain;
        background-position: top center;
        background-repeat: no-repeat;
        background-image: url('../assets/images/working.png'), linear-gradient(#f8f9fe, #fff);
    }

    .login-form {
        margin: 0 10px;
        padding-left: 6rem;
        width: 100%;

        @include mobile() {
            padding: 200px 10px 0;
        }

        .login-card {
            max-width: 400px;
            width: 100%;

            .mb-22 {
                margin-bottom: 22px;
            }
        }
    }
}
</style>