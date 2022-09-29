---
author: ''
category: Magento
date: '2015-01-18'
summary: ''
title: Create A Custom Block in Magento 1
---
# Create a custom design block in Magento 1

## Step 1: Register module in `app/etc/modules/<yourblockname>.xml

	<?xml version="1.0" encoding="UTF-8"?>
	<config>
		<modules>
			<Inchoo_AdminBlock>
				<version>1.0.0.0</version>
			</Inchoo_AdminBlock>
		</modules>
		<global>
			<blocks>
				<inchoo_adminblock>
					<class>Inchoo_AdminBlock_Block</class>
				</inchoo_adminblock>
			</blocks>
		</global>
		<admin>
			<routers>
				<adminhtml>
					<args>
						<modules>
							<inchoo_adminblock after="Mage_Adminhtml">Inchoo_Adminblock_Adminhtml</inchoo_adminblock>
						</modules>
					</args>
				</adminhtml>
			</routers>
		</admin>
	</config>
