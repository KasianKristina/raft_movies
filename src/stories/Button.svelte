<script lang="ts">
	import './button.css';

	interface Props {
		/** What background color to use */
		backgroundColor?: string;
		/** Button contents */
		label: string;
		/** The onclick event handler */
		onClick?: () => void;
		disabled?: boolean;
	}

	const { backgroundColor, label, onClick, disabled = false }: Props = $props();
</script>

<button
	type="button"
	class={'button'}
	class:button--primary={false}
	style:background-color={backgroundColor}
	onclick={onClick}
	disabled={disabled}
>
	{label}
</button>
