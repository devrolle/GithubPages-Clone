<template>
    <TutorialStep :stepNumber="1">
        <div class="text-center py-10 px-3 w-3/5">
            <p class="step-heading">Create a repository</p>
            <p class="step-text m-[30px]">
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
    <TutorialStep stepNumber="?">
        <div class="step-content">
            <p class="step-heading">What git client are you using?</p>
            <div class="tabs mt-[30px]">
                <button
                    @click="($event) => updateGitType('terminal')"
                    :class="
                        gitType === 'terminal' ? 'tab active' : 'tab in-active'
                    "
                >
                    A terminal
                </button>
                <button
                    @click="($event) => updateGitType('desktop')"
                    :class="
                        gitType === 'desktop' ? 'tab active' : 'tab in-active'
                    "
                >
                    GitHub Desktop
                </button>
                <button
                    @click="($event) => updateGitType('unknown')"
                    :class="
                        gitType === 'unknown' ? 'tab active' : 'tab in-active'
                    "
                >
                    I don&apos;t know
                </button>
            </div>
        </div>
    </TutorialStep>
    <UserTerminalTutorial v-show="gitType === 'terminal'" />
    <UserDesktopTutorial v-show="gitType === 'desktop'" />
    <UserUnknownGitTutorial v-show="gitType === 'unknown'" />
</template>

<script>
import TutorialStep from './TutorialStep.vue';
import UserTerminalTutorial from './UserTerminalTutorial.vue';
import UserDesktopTutorial from './UserDesktopTutorial.vue';
import UserUnknownGitTutorial from './UserUnknownGitTutorial.vue';

export default {
    name: 'UserTutorial',
    components: {
        TutorialStep,
        UserTerminalTutorial,
        UserDesktopTutorial,
        UserUnknownGitTutorial,
    },
    data() {
        return {
            gitType: 'terminal',
        };
    },
    methods: {
        updateGitType(type) {
            if (this.gitType !== type) {
                this.gitType = type;
            }
        },
    },
};
</script>

<style>
.step-heading {
    font-family: 'Roboto', 'sans serif';
    font-weight: 300;
    font-size: 30px;
}

.step-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    padding-top: 40px;
    padding-bottom: 60px;
}

.step-text {
    font-size: 16px;
    font-weight: 300;
    line-height: 200%;
}
</style>
