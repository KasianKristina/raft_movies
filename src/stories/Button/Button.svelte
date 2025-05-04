<script lang="ts">
	import './button.css';

	interface Props {
		label: string;
		onClick?: () => void;
		disabled?: boolean;
	}

	const { label, onClick, disabled = false }: Props = $props();
</script>

<button type="button" class="button" onclick={onClick} {disabled}>
	{label}
</button>
