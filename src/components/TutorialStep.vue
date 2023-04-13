<template>
    <div
        class="relative flex items-center max-h-[331px] border border-[#ddd] rouned-[5px]"
    >
        <slot />
        <span
            class="absolute -top-6 -left-6 w-[58px] h-[58px] rounded-full bg-[#327fc7] text-white text-[30px] flex justify-center items-center"
            >{{ stepNumber }}</span
        >
    </div>
</template>

<script>
export default {
    name: 'TutorialStep',
    props: {
        stepNumber: Number | String,
    },
};
</script>
