<script module>
	import { defineMeta } from '@storybook/addon-svelte-csf';
	import Button from './Button.svelte';
	import { fn } from '@storybook/test';

	// More on how to set up stories at: https://storybook.js.org/docs/writing-stories
	const { Story } = defineMeta({
		title: 'Example/Button',
		component: Button,
		tags: ['autodocs'],
		argTypes: {
			backgroundColor: { control: 'color' },
		},
		args: {
			onClick: fn(),
		},
	});
</script>

<!-- More on writing stories with args: https://storybook.js.org/docs/writing-stories/args -->
<Story name="Primary" args={{ label: 'Button' }} />

<Story name="Disabled" args={{ label: 'Disabled button', disabled: true }} />

<Story name="Large" args={{ label: 'Button' }} />

<Story name="Small" args={{ label: 'Button' }} />
