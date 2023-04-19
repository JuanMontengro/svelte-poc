<script>
	import Card, {
		Content,
		PrimaryAction,
		Media,
		Actions,
		ActionButtons,
		ActionIcons
	} from '@smui/card';
	import Button, { Label } from '@smui/button';
	import IconButton, { Icon } from '@smui/icon-button';
	import Chip, { Text } from '@smui/chips';

	export let details = {
		title: '',
		description: '',
		status: '',
		lang: '',
		stars: 0,
		shares: 0
	};
	const { title, description, status, lang, stars, shares } = details;

	let clicked = 0;
</script>

<div class="card-display">
	<div class="card-container">
		<Card>
			<Content class="mdc-typography--body2" style="padding-bottom: 0;">
				<img src="/images/github.png" alt="Github" />
				<h2 class="mdc-typography--headline6 card-title">
					{title}
					<Chip
						chip={status}
						style="border-radius: unset;
						text-transform: capitalize;
						font-size: 12px;
						margin-left: 10px;
						height: 25px;"
					>
						<Text>{status}</Text>
					</Chip>
				</h2>
				<div class="card-description">
					{description}
				</div>
			</Content>

			<Actions>
				<ActionButtons>
					<Chip
						chip={lang}
						style="background: unset;
						display: flex;
						justify-content: space-between;
						min-width: 60px;
						font-size: 15px;
						padding: 0 5px;"
					>
						<img style="height:17px;" src="/images/rectangle.png" alt="rectangle" />
						<Text style="color: #b3b3b3;">{lang}</Text>
					</Chip>
					<Chip
						chip={stars}
						style="background: unset;
						display: flex;
						justify-content: space-between;
						min-width: 50px;
						font-size: 15px;
						padding: 0 5px;"
					>
						<img style="height:17px;" src="/images/star.png" alt="rectangle" />
						<Text style="color: #b3b3b3;">{stars}</Text>
					</Chip>
					<Chip
						chip={lang}
						style="background: unset;
						display: flex;
						justify-content: space-between;
						min-width: 50px;
						font-size: 15px;
						padding: 0 5px;"
					>
						<img style="height:17px;" src="/images/share.png" alt="rectangle" />
						<Text style="color: #b3b3b3;">{shares}</Text>
					</Chip>
				</ActionButtons>
			</Actions>
		</Card>
	</div>
</div>

<style>
	.card-container {
		max-width: 540px;
	}
	.card-title {
		margin: 0;
		display: flex;
		font-size: 21px;
		padding: 12px 0;
	}
	.card-description {
		padding-top: 10px;
		color: #787d8e;
		font-size: 16px;
	}
	.mdc-chip:hover {
		background-color: unset !important;
	}
</style>
