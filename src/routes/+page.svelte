<script>
	import { Gantt } from "wx-svelte-gantt";

	const tasks = [
		{
			id: 1,
			start: new Date(2024, 3, 2),
			end: new Date(2024, 3, 17),
			text: "Project planning",
			progress: 30,
			parent: 0,
			type: "summary",
			open: true,
			details: "Outline the project's scope and resources.",
		},
	];
	const links = [];
	const scales = [
		{ unit: "month", step: 1, format: "MMMM yyy" },
		{ unit: "day", step: 1, format: "d", css: dayStyle },
	];
</script>

<Gantt {tasks} {links} {scales} />