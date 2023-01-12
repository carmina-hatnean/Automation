# Automation
Below are some automation tests samples on eMag.ro website that I wrote while working on previous projects.

-------


**Should have the correct page title**

describe('eMag.ro',()=>{
	it('should have the correct page title', async()=>{
			await browser.url('https://www.emag.ro');
			await expect(browser).toHaveTitle('eMAG.ro - Căutarea nu se oprește niciodată');
	});
});


-----------
