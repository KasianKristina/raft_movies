<script lang="ts">
	import './button.css';

	interface Props {
		/** What background color to use */
		backgroundColor?: string;
		/** Button contents */
		label: string;
		/** The onclick event handler */
		onClick?: () => void;
	}

	const { backgroundColor, label, onClick }: Props = $props();
</script>

<button
	type="button"
	class={'button'}
	class:button--primary={false}
	style:background-color={backgroundColor}
	onclick={onClick}
>
	{label}
</button>
