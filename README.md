# Automation
Below are some automation tests samples on eMag.ro website that I wrote while working on previous projects.

-------


**1. Should have the correct page title**
```
describe('eMag.ro',()=>{
	it('should have the correct page title', async()=>{
			await browser.url('https://www.emag.ro');
			await expect(browser).toHaveTitle('eMAG.ro - Căutarea nu se oprește niciodată');
	});
});
```

-----------

**2. Should contain a cart button**
```
describe('eMag.ro',()=>{
	it('should contain a cart button', async()=>{
			const cartButton = await $('#my_cart');
			await expect(cartButton).toBeDisplayed();
	});
});
```

------------

**3. Should open eMag Genius page**
```
describe('eMag.ro',()=>{
	it('should open eMag Genius page', async()=>{
		const geniusButton = await $('[title="eMag Genius]');
		await geniusButton.click();
		await expect(browser).toHaveTitle('Genius: livrare gratuită și oferte exclusive pe eMAG, Tazz, Fashion Days și Freshful - eMAG.ro');

	});
});
```

----------

**Should have a working search**
```
describe('eMag.ro',()=>{
	it('should have a working search',async () =>{
		const serchBox = await $('#searchboxTrigger');
		const serchButton = await $(.searchbox-submit-button);
		await serchBox.setValue('tricou polo');
		await serchButton.click();

	});
});
```

-----------
