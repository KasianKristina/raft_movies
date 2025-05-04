<script module>
	import { defineMeta } from '@storybook/addon-svelte-csf';
	import Button from './Button.svelte';
	import { fn } from '@storybook/test';

	const { Story } = defineMeta({
		title: 'Example/Button',
		component: Button,
		tags: ['autodocs'],
		args: {
			onClick: fn(),
		},
	});
</script>

<Story name="Primary" args={{ label: 'Button' }} />

<Story name="Disabled" args={{ label: 'Disabled button', disabled: true }} />
