1. purchase_invoice.py: erpnext/accounts/doctype/purchase_invoice/purchase_invoice.py
                           Line 528 Adding(ignore_permissions=True)
2. sales_invoice.py:erpnext/accounts/doctype/sales_invoice/sales_invoice.py
                          Line 93, Line Change Loyalty Points Settings to Sales Value Based Discount Settings
3. lead.js: erpnext/crm/doctype/lead/lead.js
                          Line 46 &47  --> Line Are Commanding for Button --> Prospect, Add to Prospect
4. delivery_note.js:erpnext/stock/doctype/delivery_note/delivery_note.js
                          Line 168 to 171 --> Lines are Commanding for Button --> Shipment
                          Line 173 to 175 --> Lines are Commanding for Button --> Installation Note
5. taxes_and_totals.py: erpnext/controllers/taxes_and_totals.py
                          Line 21: Adding --> from erpnext.utilities.regional import temporary_flag
                          Function: get_itemised_tax_breakup_html -->  Line 945--> Removing and Line 955 to 963 --> Removing
                                                                       Line 955 to 959 --> adding and Line 969 and 970 --> Removing and 965 Adding
                          Function: get_round_off_applicable_accounts --> Line 979 to 981 --> Removing and Line 974 to 976 Adding and Line 1006 also Removing
                                                                          Line 1001 to 1009 --> Adding
                          Function: get_rounded_tax_amount --> Line 1051 to 1053 removing, and 1054 to 1057 adding
                          Function: set_amounts_in_company_currency --> Line 1090 removing, and 1094 Line Adding
6. itemised_tax_breakup.html: erpnext/templates/includes/itemised_tax_breakup.html
                          (itemised_taxable_amount.get(item, 0)) --> Replaced to taxes.taxable_amount in Line 22 and 28
                          class='text-right' --> Replaced to class="text-right" in Line 18 and 28
                          17th Line Adding --> 					<td>{{ taxes.item }}</td>
                          15th Line Changed  --> {% for item, taxes in itemised_tax.items() %} to  {% for taxes in itemised_tax_data %}
7. regional.py: erpnext/utilities/regional.py
                New File Creation
                          
      
