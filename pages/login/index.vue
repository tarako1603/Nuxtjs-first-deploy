<template>
    <div class="flex min-h-full items-center justify-center py-12 px-4 sm:px-6 lg:px-8">
        <div class="w-full max-w-md space-y-8">
            <div>
                <div class="flex justify-center items-center">
                    <img class="h-12 w-auto"
                        src="https://preview.redd.it/2ssi8ft315b71.png?auto=webp&s=0fbae78f60d85a7c1a1ca510cdc2baaf0852dd9d"
                        alt="Your Company" />
                    <img class="h-6 w-auto"
                        src="https://t4.ftcdn.net/jpg/01/26/10/59/360_F_126105961_6vHCTRX2cPOnQTBvx9OSAwRUapYTEmYA.jpg"
                        alt="Your Company" />
                    <img class="h-12 w-auto"
                        src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600" alt="Your Company" />
                </div>

                <h2 class="mt-6 text-center text-3xl font-bold tracking-tight text-gray-900">サインイン</h2>

            </div>
            <form class="mt-8 space-y-6" @submit.prevent="login">
                <input type="hidden" name="remember" value="true" />
                <div class="-space-y-px rounded-md shadow-sm">
                    <div>
                        <label for="email-address" class="sr-only">メールアドレス</label>
                        <input id="email-address" name="email" type="email" autocomplete="email" required=""
                            class="relative block w-full appearance-none rounded-none rounded-t-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm"
                            placeholder="メールアドレス" v-model="email"/>
                    </div>
                    <div>
                        <label for="password" class="sr-only">パスワード</label>
                        <input id="password" name="password" type="password" autocomplete="current-password" required=""
                            class="relative block w-full appearance-none rounded-none rounded-b-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm"
                            placeholder="パスワード" v-model="password" />
                    </div>
                </div>

                <div class="flex items-center justify-between">
                    <div class="flex items-center">
                        <input id="remember-me" name="remember-me" type="checkbox"
                            class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-500" />
                        <label for="remember-me" class="ml-2 block text-sm text-gray-900">ログイン状態を保存</label>
                    </div>

                    <div class="text-sm">
                        <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">パスワードを忘れた場合</a>
                    </div>
                </div>

                <div>
                    <button type="submit"
                        class="group relative flex w-full justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 text-sm font-medium text-white hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">
                        <span class="absolute inset-y-0 left-0 flex items-center pl-3">
                            <LockClosedIcon class="h-5 w-5 text-indigo-500 group-hover:text-indigo-400"
                                aria-hidden="true" />
                        </span>
                        サインイン
                    </button>
                </div>
            </form>
        </div>
    </div>
</template>

<script setup>
import { LockClosedIcon } from '@heroicons/vue/20/solid'

const email = ref("");
const password = ref("");

const login = () => {
    console.log(email.value)
    console.log(password.value)
}
</script>