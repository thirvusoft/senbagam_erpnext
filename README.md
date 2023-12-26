1. purchase_invoice.py: erpnext/accounts/doctype/purchase_invoice/purchase_invoice.py
                           Line 528 Adding(ignore_permissions=True)
                           Function: on_submit --> Line Adding 491 to 528 For Serial No Updating in Purchase Invoice Item Table
                                                   Line 568 to 571 adding for batch no empty in Purchase Invoice Item Table
3. sales_invoice.py:erpnext/accounts/doctype/sales_invoice/sales_invoice.py
                          Line 93, Line Change Loyalty Points Settings to Sales Value Based Discount Settings
                          Line 132 and 133 are commanding and Line 265 and 266 are Commanding 
5. lead.js: erpnext/crm/doctype/lead/lead.js
                          Line 46 &47  --> Line Are Commanding for Button --> Prospect, Add to Prospect
6. delivery_note.js:erpnext/stock/doctype/delivery_note/delivery_note.js
                          Line 168 to 171 --> Lines are Commanding for Button --> Shipment
                          Line 173 to 175 --> Lines are Commanding for Button --> Installation Note
7. taxes_and_totals.py: erpnext/controllers/taxes_and_totals.py
                          Line 21: Adding --> from erpnext.utilities.regional import temporary_flag
                          Function: get_itemised_tax_breakup_html -->  Line 945--> Removing and Line 955 to 963 --> Removing
                                                                       Line 955 to 959 --> adding and Line 969 and 970 --> Removing and 965 Adding
                          Function: get_round_off_applicable_accounts --> Line 979 to 981 --> Removing and Line 974 to 976 Adding and Line 1006 also Removing
                                                                          Line 1001 to 1009 --> Adding
                          Function: get_rounded_tax_amount --> Line 1051 to 1053 removing, and 1054 to 1057 adding
                          Function: set_amounts_in_company_currency --> Line 1090 removing, and 1094 Line Adding
8. itemised_tax_breakup.html: erpnext/templates/includes/itemised_tax_breakup.html
                          (itemised_taxable_amount.get(item, 0)) --> Replaced to taxes.taxable_amount in Line 22 and 28
                          class='text-right' --> Replaced to class="text-right" in Line 18 and 28
                          17th Line Adding --> 					<td>{{ taxes.item }}</td>
                          15th Line Changed  --> {% for item, taxes in itemised_tax.items() %} to  {% for taxes in itemised_tax_data %}
9. regional.py: erpnext/utilities/regional.py
                New File Creation
10. batch.py: erpnext/stock/doctype/batch/batch.py
                           Lines Removing 295 to 305 --> 	if not batch_no:
                                                          		frappe.msgprint(
                                                          			_(
                                                          				"Please select a Batch for Item {0}. Unable to find a single batch that fulfills this requirement"
                                                          			).format(frappe.bold(item_code))
                                                          		)
                                                          		if throw:
                                                          			raise UnableToSelectBatchError
                                                          	print("batch_no")
                                                          	print(batch_no)
                          Lines Adding 295 to 308 --> company=frappe.get_value("Warehouse",warehouse,"company")
                                                        	company_type=frappe.get_value("Company",company,"company_type")
                                                        	sales_value=frappe.get_value("Company Type",company_type,"sales")
                                                        	purchase_value=frappe.get_value("Company Type",company_type,"purchase")
                                                        	if sales_value==1 and purchase_value==1:
                                                        		if not batch_no:
                                                        			frappe.msgprint(
                                                        				_(
                                                        					"Please select a Batch for Item {0}. Unable to find a single batch that fulfills this requirement"
                                                        				).format(frappe.bold(item_code))
                                                        			)
                                                        			if throw:
                                                        				raise UnableToSelectBatchError
11. contact_address_quick_entry.js: erpnext/public/js/utils/contact_address_quick_entry.js
                                  ,adding in line 83
12. transaction.js: erpnext/public/js/controllers/transaction.js
                    Line 416 Adding --> 		var without_serial=0
                    Line 425 to 490 editing and adding
13. delivery_note.py: erpnext/stock/doctype/delivery_note/delivery_note.py
                    Lines 142 to 144 Are commanding for Batch and Serial no Settings
14. purchase_receipt.py: erpnext/stock/doctype/purchase_receipt/purchase_receipt.py
                    Line 121 to 124 are Commanding and line 248 is also Commanding
15. stock_ledger_entry.py: erpnext/stock/doctype/stock_ledger_entry/stock_ledger_entry.py
                    Lines 106 to 111 Are commanding for the purpose of Batch Number Message
16. get_item_details.py: erpnext/stock/get_item_details.py
                    Line 158 change --> or (args.get("doctype") == "Sales Invoice" and args.get("update_stock")) to or (args.get("doctype") == "Sales Invoice" or args.get("update_stock"))
                    Lines 164 to 177 are Removing
                    Lines 164 to 226 are Adding
17. stock_ledger.py: erpnext/stock/report/stock_ledger/stock_ledger.py
                   Lines 94 and 95 are commanding and 98 to 100 are also commanding
18. stock_ledger.py:erpnext/stock/stock_ledger.py
                   Lines 146 to 158 are Commanding
19. serial_no.py: erpnext/stock/doctype/serial_no/serial_no.py
                  Lines 335 to 342 are Commanding
                  Lines 446 to 449 are Commanding
                  Lines 576 to 603 are Removing
                  Lines 578 to 677 are adding
        
                   
    

      
