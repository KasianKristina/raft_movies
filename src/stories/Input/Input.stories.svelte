<script module>
	import { defineMeta } from '@storybook/addon-svelte-csf';
	import Button from './Input.svelte';
	import { fn } from '@storybook/test';

	const { Story } = defineMeta({
		title: 'Example/Input',
		component: Button,
		tags: ['autodocs'],
		args: {
			onClick: fn(),
		},
	});
</script>

<Story name="Primary" args={{ label: 'Label' }} />

<Story name="Disabled" args={{ label: 'Disabled label', disabled: true }} />

<Story name="Placeholder" args={{ placeholder: 'Placeholder' }} />

<Story name="Error" args={{ label: 'Error', errorMessage: 'Error message' }} />
