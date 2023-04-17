<template>
    <TutorialStep :stepNumber="stepNumber">
        <div class="step-content">
            <p class="step-heading">{{ heading }}</p>
            <p class="step-text">
                {{ text }}
            </p>
            <Terminal>
                <TerminalLine v-for="line in terminalLinesContent">
                    {{ line }}
                </TerminalLine>
            </Terminal>
        </div>
    </TutorialStep>
</template>

<script>
import TutorialStep from './TutorialStep.vue';
import Terminal from './Terminal.vue';
import TerminalLine from './TerminalLine.vue';

export default {
    name: 'TerminalStep',
    props: {
        stepNumber: Number,
        heading: String,
        text: String,
        terminalLinesContent: Array,
    },
    components: {
        TutorialStep,
        Terminal,
        TerminalLine,
    },
};
</script>
