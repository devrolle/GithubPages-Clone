<template>
    <TerminalStep
        :stepNumber="2"
        heading="Clone The Repository"
        text="Go to the folder where you want to store your project, and clone
                the new repository:"
        :terminalLinesContent="[
            'git clone https://github.com/username/username.github.io',
        ]"
    />
    <TerminalStep
        :stepNumber="3"
        heading="Hello World"
        text="Enter the project folder and add an index.html file:"
        :terminalLinesContent="[
            'cd username.github.io',
            `echo, Hello World > index.html`,
        ]"
    />
    <TerminalStep
        :stepNumber="4"
        heading="Push It"
        text="Add, commit, and push your changes:"
        :terminalLinesContent="[
            'git add --all',
            'git commit -m Initial commit',
            'git push -u origin main',
        ]"
    />
    <TutorialStep :stepNumber="5">
        <div class="step-content">
            <p class="step-heading">…and you're done!</p>
            <p class="step-text">
                Fire up a browser and go to
                <strong class="font-bold">https://username.github.io.</strong>
            </p>
            <!-- Add Checkmark -->
        </div>
    </TutorialStep>
</template>

<script lang="js">
import TutorialStep from './TutorialStep.vue';
import StepTerminal from './Terminal.vue';
import TerminalLine from './TerminalLine.vue';
import TerminalStep from './TerminalStep.vue';


export default {
	name: 'UserTerminalTutorial',
	components: {
		TutorialStep,
		StepTerminal,
		TerminalLine,
		TerminalStep,
	}
}
</script>
