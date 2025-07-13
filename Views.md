# Setting up a view for showing a map for content type 'Rental'

- ပထမဆုံး ကိုယ့်ရဲ့ content type ထဲမှာ taxonomy term 'အိမ်ငှါး' 'မြေငှါး' 'အိမ်ရောင်း' 'မြေရောင်း' ဆိုတာထည့်ထားရမယ်။ ထည့်ဖို့အတွက် 'content type' field ထဲမှာ reference ကို ရွေးရမယ်။
- (source: https://www.drupal.org/docs/contributed-modules/geolocation-field/how-to-add-a-custom-marker-using-taxonomy-term#:~:text=Under%20Fields%2C%20add%20the%20image,Download%20&%20Extend)
- Under Fields, add the image field from the taxonomy to the View (you may want to hide it from display)
- Open Format: Geolocation CommonMap > Settings and select the marker field under Advanced settings > Icon source field
- Save the View and you will see your markers, differentiated by that taxonomy term
