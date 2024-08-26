<script>
	// 料理名、画像URL、出前館のリンクを含むデータのリスト
	let dishes = [
		{
			name: '洋食',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhg5nDb_mCwhuyWtSDadS6fFWmUKskJCha5EifBMoq68cjQDZ11qrrEbRvUApAUlslPxUMNSshjnXqQpSZz1SBgwWdBTD7-i4tCsU39fQukZDMjRHmB8V5UgTak5uhbV-RwF37CIRnRt9Ex/s400/food_omurice.png',
			url: 'https://demae-can.com/search/delivery/13104067006/50'
		},
		{
			name: 'カレーライス',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh5puNP-5AEBx1MofxgChBg-Gp0RBd5SEKwczB9RPXuH8128OlJ06jzCiarIVDxGcRmdCt4rRqdgQEm6cZ2M4yyfl6SCGzrZxfBpuXSKG0NlGPWYpsOvZUTjBEOfpTyW1-nsrD_tyLP2BeR/s180-c/food_curryrice_white.png',
			url: 'https://demae-can.com/search/delivery/13104067006/11'
		},
		{
			name: 'ピザ',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEijnnnXzseyv8G5Y3bqtOfJe3hRg3McyQaZAdYJkmlXf6gO8mnnL80bciX7jI2TUHTMsPMitftjLtwBNGsDl8JXf2IC40elWijvbFTM9gU2BZq478kKqTVVKKutEp1KWhX66-O4ExPHKFEt/s1600/pizza_margherita.png',
			url: 'https://demae-can.com/search/delivery/13104067006/02'
		},
		{
			name: '中華',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhgEnSqN0gYA1O4zZ_ww2_avUG0EIsCCQtCt1_4hLRzsQRVRAgHDL6CsM3HyRwFV6D4t8tlZjPhZF58OLI0Avy8_04_Q2Sy6kYBlkH86CSpHxsK1Ql71DS9gxIaT-oHss0_Sv2nyXsnhsvB/s180-c/food_chuukadon.png',
			url: 'https://demae-can.com/search/delivery/13104067006/04'
		},
		{
			name: '寿司・海鮮',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhnFR5bNaKk3rRor5-ZbT0mq-u5Lw34grDRjrcC-FDlMxWtRAlv1ZsMNPSXCCeAfkSKq2BhX9WsgqSUlpcE4xrVMRPsla6qDaLpV9L94aS3cflZDD-0HF9P_Ks2-2-DVomXL3PGfYhFqRon/s180-c/sushi_oke_nigiri.png',
			url: 'https://demae-can.com/search/delivery/13104067006/03'
		},
		{
			name: 'インドカレー',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjDIT9tdDJnlNPIwuaqTU8pdV_gxO37lVsHRdhqSrMuLDCHWMnDl-lvu-QUWlvW7TU25uDKcRwyAcUQCKnimTsLdzcEmXIUr5JuXYS6N2kXdBSeRQA7eZGjv3XI321ZnNmqiLyQvlxXYbYy/s180-c/food_india_meals.png',
			url: 'https://demae-can.com/search/delivery/13104067006/112'
		},
		{
			name: '韓国料理',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjEpN71Cliyf4hY1Dv1WEMXd4UsOwBKldt8rf08IGDuXmxYP9_3o2devQsy8qRsH3JsypAKOElokIeEjXZ4D8O92B-f3aCFwMJlpMs-robvyGbllmHiyBud2-2CBxjQ0Lu_MkqIbFqo4QY/s180-c/food_samugetan.png',
			url: 'https://demae-can.com/search/delivery/13104067006/97'
		},
		{
			name: '弁当',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh4ObAD8nU4kjXaO778Pmyw9qzc3SN-hGn2JAuTkU0DkdMENOaXm1QveitivLDnxTjkkWgxLnvV2udz8cqji9OjJjVxOfTGAEC_HCKxc-Xg0djeNPrBkmvvdHYJf5RuUyRZMmUR18M4pgk/s180-c/food_obentou_makunouchi.png',
			url: 'https://demae-can.com/search/delivery/13104067006/01'
		},
		{
			name: 'フライドチキン・唐揚げ',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgPyBa_EmVAQ_T1F_ugtbvCEvbrSac5mrofACdMyqrD6hCB7JLM6qmDRhtfghjsJtn_NWMuh1hyphenhyphenJJeUfXy0KryKhgOM_HKti0t52fWNnRFioDBUs0mJ9i2NpyC1Fntqw25gDbYjBov165Fz/s180-c/food_fried_chicken.png',
			url: 'https://demae-can.com/search/delivery/13104067006/45'
		},
		{
			name: 'ハンバーグ・ステーキ',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgg8yS9EiOn9aTYt5ZWeVL5pwGMVvSDFpYaxGOwSPeShc7Ogz7ygKUZcmLnsvA-O3yO678S5q8GRs-EaZkd_J0_H_ofa-ku7jh8jCHsNbQRt965hMNgBdjSo1U8yuORmUy2TRrjYKmK4wg/s180-c/food_wafu_hamburg.png',
			url: 'https://demae-can.com/search/delivery/13104067006/051'
		},
		{
			name: '和食',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgnX-maVnstIKmTcWpAwpO-jCbD5ozcpNyDjbt-8yaDLMIxzcJ5W6G6Rn2n8Z8_xr6QYIQ7oJsfcb095xQommc9bmnB4F8knAJ9xUSKaeDjCQS1G97HqZPL8QVp-DPm0VRHx9cRwC74FLA/s180-c/bousai_nikujaga.png',
			url: 'https://demae-can.com/search/delivery/13104067006/07'
		},
		{
			name: 'そば・うどん',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiepyYZ8XM8mmzE5G-UAgdXO2skw1S-DbYPasrkWrRZTEKGNzqaGdioJXuzW5zP9AwPo4yw-0XraJ3AIj87sHXVsfnFBXBRLOXVSpqgjAk47yo078AkSkiDNG8dGDyBBjKL37Scekdf2vFz/s180-c/soba_kake.png',
			url: 'https://demae-can.com/search/delivery/13104067006/06'
		},
		{
			name: '丼',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsjtH80qVRerWsd1SYsH0tanZwwZgd1J6303or1gBpSBYoxfYp9OPUJllkwjHDy7ylsB7JGZbMzVdlsjeiuTbPn6eym7Zf2T45GO2x7HJD-9zyW2eaDPMjB7EMuaWyNjZ8512V3iK1Yrsw/s180-c/food_sauce_katsudon.png',
			url: 'https://demae-can.com/search/delivery/13104067006/62'
		},
		{
			name: 'ラーメン',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEijQFSiB_2tYowkTZYG58CjFidc7IFBBtcfJ6R98qAN7d1pQW6Ei11yw_fcLdD4MkGnjiqUORQBh5g-QhuZP6LOxGWdS38wz6tUr3PQM9eKFsu60fG87X1M5YSd0Wg8RL7-hGScc6SRPlWj/s180-c/ramen_syouyu.png',
			url: 'https://demae-can.com/search/delivery/13104067006/61'
		},
		{
			name: 'たこ焼き・お好み焼き',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjx0G1fQr277AhjDsA3BiRriI55q_FmzkPQBpRX6EVB57iPqI8KJm5bJkMk7m55Ge83nkDuvdUSG7UKS1Ju7pNXkIkzGXdoJIqkT86duzcyZXIM3paaQRDVD9f4g_ZU9EfvGx-kleEKkuLY/s180-c/food_takoyaki.png',
			url: 'https://demae-can.com/search/delivery/13104067006/09'
		},
		{
			name: 'バーガー・サンドイッチ',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiZQ2T87XFh7Uey2g7f4AzBt069odOigndEFLrXDl40UXAb2r0AiD0Ps4HsvWgB9eH-BzuGyNMhnnMnkYMXZhSuS1wG2bphuy2in59RG2oShXgpfsXpMDcjQnrJVmohjYawzI5j1XcL3bD5/s180-c/hamburger_meat_sauce.png',
			url: 'https://demae-can.com/search/delivery/13104067006/18'
		},
		{
			name: 'エスニック',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhkY4OavJALCcuOtuWqZTWkA4eVQajZ4erR62as-FqBXOZslgDY7cMvtUR-jnCkPvkHfgg9E460nk83r5xvYz0PRVz1XQc_vztxnnRJh9awqsl9QACrqsEL1-pPosqJTIkqsxr3OA_pntFf/s180-c/namaharumaki.png',
			url: 'https://demae-can.com/search/delivery/13104067006/60'
		},
		{
			name: 'とんかつ・天ぷら',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjr4pJuFfFx9-3dJJnO1YO_AtWXImcmnzg56JcE8ANXt9kNK2dV5kUMab-PIo7VEkUyUzOyEObNTtGZDP5P11Bk7kR08-AJVBy_HYPpyRpxTf6yg8ELt5fWYB5Q3W6z8SAHC60Rb_1pR9Ht/s180-c/food_tonkatsu.png',
			url: 'https://demae-can.com/search/delivery/13104067006/08'
		},
		{
			name: 'パスタ・イタリアン',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi3gLY0WdSLizyaRtsYdzQEaW_cyfzARgrXx6HqQfpzPP9LdvIHZltREA9CFICtHgKgkyET8hfeMCrp4L2oORcrwxM75LzQt3Enjvm6JY9klwu_1DpIO4FOJ0eTqyGJWIyJU8dRP_VzfpWM/s180-c/food_spaghetti_bolognese_meatsauce.png',
			url: 'https://demae-can.com/search/delivery/13104067006/67'
		},
		{
			name: '焼肉・しゃぶしゃぶ',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjHz4Pc_s6-TuROmvfeJrQzymf3d7Oiks2eoWUCHPBgDXS6CqxeytcPxPMVkij4PwwUNmg4Z10voDrmPhd79i0Vk1gc_n447VltbrWjrKMz_Q4CuQQP9KfWNfQFglabD6MR7PslQPeyzOFf/s180-c/niku_yakiniku.png',
			url: 'https://demae-can.com/search/delivery/13104067006/10'
		},
		{
			name: 'ヘルシー料理',
			image:
				'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg0BLEAz8FhafJpc8bSr4f9HgZs2fFHHquXD_7SjoVX2zrRUI4YXR63OefBPRSmayTBI0icIZpk2K7fNHR3blEwXBty-bpHs4-ynFMSZDxki5hYSReX2O3MomxEVxacN9al42I-CJXH7jg/s180-c/food_vegetable_sald.png',
			url: 'https://demae-can.com/search/delivery/13104067006/52'
		}
	];

	// ランダムな料理名とその画像とURLを選ぶ関数
	function getRandomDish() {
		const randomIndex = Math.floor(Math.random() * dishes.length);
		return dishes[randomIndex];
	}

	// 初期表示用の料理名と画像
	let selectedDish = getRandomDish();

	// ボタンをクリックした時に料理名と画像を更新
	function updateDish() {
		selectedDish = getRandomDish();
	}
</script>

<main>
	<div class="container">
		<h1>今日のランチは {selectedDish.name}</h1>
		<div class="dish-image">
			<img src={selectedDish.image} alt={selectedDish.name} />
		</div>
		<a href={selectedDish.url} target="_blank" rel="noopener noreferrer" class="order-button"
			>出前館はこちら</a
		>
		<button on:click={updateDish} class="update-button">別の料理を選ぶ</button>
	</div>
</main>

<style>
	main {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		margin: 0;
		background: radial-gradient(circle, #f9f9f9, #e0e0e0);
		font-family: 'Arial', sans-serif;
	}

	.container {
		text-align: center;
		background: #fff;
		border-radius: 12px;
		padding: 2rem;
		box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
		max-width: 500px;
		width: 90%;
	}

	h1 {
		font-size: 2rem;
		margin-bottom: 1rem;
		color: #333;
	}

	.dish-image {
		position: relative;
		display: inline-block;
		width: 100%;
		max-width: 400px;
		margin: 1rem 0;
		border-radius: 12px;
		overflow: hidden;
		box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
	}

	img {
		width: 100%;
		height: auto;
		transition:
			transform 0.3s ease,
			box-shadow 0.3s ease;
	}

	img:hover {
		transform: scale(1.05);
		box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3);
	}

	a.order-button {
		display: inline-block;
		margin-top: 1rem;
		padding: 0.75rem 1.5rem;
		font-size: 1.1rem;
		color: #fff;
		background-color: #ff6f61;
		text-decoration: none;
		border-radius: 6px;
		transition:
			background-color 0.3s ease,
			transform 0.3s ease;
	}

	a.order-button:hover {
		background-color: #e55d50;
		transform: translateY(-2px);
	}

	button.update-button {
		margin-top: 1rem;
		padding: 0.75rem 1.5rem;
		font-size: 1.1rem;
		cursor: pointer;
		border: none;
		border-radius: 6px;
		background-color: #4a90e2;
		color: #fff;
		transition:
			background-color 0.3s ease,
			transform 0.3s ease;
	}

	button.update-button:hover {
		background-color: #357abd;
		transform: translateY(-2px);
	}
</style>
