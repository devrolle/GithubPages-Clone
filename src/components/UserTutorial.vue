<template>
    <TutorialStep :stepNumber="1">
        <div class="text-center py-10 px-3 w-3/5">
            <h5 class="text-[30px] font-roboto font-light">
                Create a repository
            </h5>
            <p class="m-[30px] text-base font-light leading-7">
                Head over to <a href="https://github.com">GitHub</a> and
                <a href="https://github.com/new"
                    >create a new public repository</a
                >
                named <span class="italic">username.github.io</span>, where
                <span class="italic">username</span> is your username (or
                organization name) on GitHub.
            </p>
            <p class="text-sm">
                If the first part of the repository doesn’t exactly match your
                username, it won’t work, so make sure to get it right.
            </p>
        </div>
        <div class="relative">
            <img
                src="https://pages.github.com/images/user-repo@2x.png"
                alt="step-image"
                class="max-h-[325px]"
            />
        </div>
    </TutorialStep>
</template>

<script>
import TutorialStep from './TutorialStep.vue';

export default {
    name: 'UserTutorial',
    components: {
        TutorialStep,
    },
};
</script>

<style scoped>
p a {
    color: #4183c4;
}
</style>
