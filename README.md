# yii2-googleplacesautocomplete
Google Places Auto Complete widget for Yii2


##Installation

Add below to your `composer.json` file

```
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/petrabarus/yii2-googleplacesautocomplete"
        }
    ],
    "requires": {
        "petrabarus/yii2-googleplacesautocomplete": "*"
    }
```

##Usage

Using widget and model.

```
use PetraBarus\Yii2\GooglePlacesAutoComplete\GooglePlacesAutoComplete;

echo GooglePlacesAutoComplete::widget([
    'model' => $model,
    'attribute' => 'location'
]);
```

Using widget for custom field name and value.

```
use PetraBarus\Yii2\GooglePlacesAutoComplete\GooglePlacesAutoComplete;
echo GooglePlacesAutoComplete::widget([
    'name' => 'place'
    'value' => 'Jakarta'
]);

```

Using active form.

```
use yii\bootstrap\ActiveForm;
use PetraBarus\Yii2\GooglePlacesAutoComplete\GooglePlacesAutoComplete;

echo $form = ActiveForm::begin();
echo $form->field($model, 'location')->widget(GooglePlacesAutoComplete::className());
```
