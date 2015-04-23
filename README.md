# formvalidator
Formvalidator is a jQuery plugin that performs basic field validation based on html attributes. When called on an element containing data fields (such as a form element) the plugin traverses to the data fields and returns a collection of invalid fields.

The plugin uses several html data attributes to perform its validation: 'data-vrule', 'data-vminval', 'data-vmaxval', 'data-vregex', and 'data-verror'. The first attribute, 'data-vrule', sets the validation rule to be applied to the element. If 'data-vrule' is not present the field is ignored and assumed valid. The next three attributes are optional parameters used in various validation rules as described below.

The last attribute, 'data-verror', is set by the plugin on each element that is returned by the plugin and contains a message describing the validation error.

The validation rule for the field is set using the 'data-vrule' attribute. The following rules are supported:

<table><tbody>
<tr>
<td>notempty</td><td>The field cannot be empty</td>
</tr>
<tr>
<td>minlength</td><td>field has a minimum length specified in 'data-vminval'</td>
</tr>
<tr>
<td>maxlength</td><td>field has a maximum length specified in 'data-vmaxval'</td>
</tr>
<tr>
<td>lenbetween</td><td>field must have a length between the values in 'data-vminval' and 'data-vmaxval' inclusive</td>
</tr>
<tr>
<td>valbetween</td><td>field must have a value between the values in 'data-vminval' and  'data-vmaxval' inclusive</td>
</tr>
<tr>
<td>isnumeric</td><td>field must be a valid number (float or integer)</td>
</tr>
<tr>
<td>isalpha</td><td>field only contains the letters a-z</td>
</tr>
<tr>
<td>isalphanumeric</td><td>field only contains the letters a-z and numbers 0-9</td>
</tr>
<tr>
<td>isemail</td><td>field appears to be a valid email address</td>
</tr>
<tr>
<td>matchregex</td><td>field matches the regular expression given in 'data-vregex'</td>
</tr>
</tbody></table>
