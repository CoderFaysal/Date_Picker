# Date Picker in just 1 miniute

## On Click Lisitiner er Moddhe

```
MaterialDatePicker<Long> materialDatePicker = MaterialDatePicker.Builder.datePicker()
                        .setTitleText("Select a date")
                        .setSelection(MaterialDatePicker.todayInUtcMilliseconds())
                        .build();
                materialDatePicker.addOnPositiveButtonClickListener(new MaterialPickerOnPositiveButtonClickListener<Long>() {
                    @Override
                    public void onPositiveButtonClick(Long selection) {
                        String date = new SimpleDateFormat("MMM dd, yyyy", Locale.getDefault()).format(new Date(selection));
                        dateformat.setText(date);
                    }
                });
                materialDatePicker.show(getSupportFragmentManager(), "tag");
```
