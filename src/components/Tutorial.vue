<template>
    <section class="flex flex-col items-center">
        <div class="max-w-[910px] text-center">
            <h3 class="font-roboto font-light text-5xl mt-[90px]">
                Ready to get started? Build your own site from scratch or
                generate one for your project.
            </h3>
            <h4
                class="font-roboto font-light text-[21px] mt-[40px] w-4/5 mx-auto"
            >
                You get one site per GitHub account and organization,<br />
                and unlimited project sites. Let‘s get started.
            </h4>
            <div id="tabs" class="mt-[45px]">
                <button
                    @click="($event) => updateType('user-site')"
                    :class="
                        instructionsType === 'user-site'
                            ? 'tab active'
                            : 'tab in-active'
                    "
                >
                    User or organization site
                </button>
                <button
                    @click="($event) => updateType('project-site')"
                    :class="
                        instructionsType === 'project-site'
                            ? 'tab active'
                            : 'tab in-active'
                    "
                >
                    Project Site
                </button>
                <div class="my-[90px]">
                    <ProjectTutorial
                        v-show="instructionsType === 'project-site'"
                    />
                    <UserTutorial v-show="instructionsType === 'user-site'" />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import UserTutorial from './UserTutorial.vue';
import ProjectTutorial from './ProjectTutorial.vue';

export default {
    name: 'Tutorial',
    data() {
        return {
            instructionsType: 'user-site',
        };
    },
    methods: {
        updateType(type) {
            if (this.instructionsType !== type) {
                this.instructionsType = type;
            }
        },
    },
    components: {
        UserTutorial,
        ProjectTutorial,
    },
};
</script>

<style scoped>
.tab {
    padding: 10px 20px;
    font-size: 15px;
    line-height: 1em;
}

.tab:nth-child(1) {
    border-radius: 5px 0 0 5px;
}
.tab:nth-child(2) {
    border-radius: 0 5px 5px 0;
}

.active {
    color: #fff;
    background-color: #327fc7;
    border: 1px solid #327fc7;
}

.in-active {
    background-color: white;
    border: 1px solid #ddd;
    transition: all 200ms ease-in-out;
}

.in-active:hover {
    border: 1px solid #327fc7;
    color: #327fc7;
}
</style>
