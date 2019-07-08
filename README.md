# jQuery Bootstrap Modal Confirmations

A jQuery Extension to create quick and simple action confirmations for buttons and links. 

You can use this extension to turn any <a>, <button> or <input type="submit"> or even other elements that have a click action 
into a confirmation modal. 
  
## Example Usage
  
```javascript

/* Simple */
jQuery(element).ConfirmationModal();

/* Custom Text, Titles and Buttons */
jQuery(element).confirmationModal({
	text: "Are you sure you want to delete this record",
	title: "Confirm deletion",
	btnconfirm: 'Delete',
	btncancel: 'Cancel',
});

/* Apply to all with class */

jQuery(document).ready(function(){
	jQuery('.confirm-action').each(function(i, elem){
		jQuery(elem).confirmationModal();
	})
});

```

You can override options using data attributes within your element. For example


```
<a href="/delete-the-record/432" data-confirmation-text="Are you sure you want to delete record number 432" data-confirmation-title="delete record 432" data-confirmation-btnconfirm="Delete">

```

Clicking the element will throw up a confirmation modal with a "Confirm" option and a "Cancel" option. 

If confirm is clicked then the element will proceed with it's default click eventn
If cancel is clicked the elements default click event is cancelled.

Modals are dynamically appended and removed from DOM to ensure things remain tidy. 

## TODO:

* Add Methods to force open or close an elements modal 
* Add callback options for when a confirmation or cancel is made
