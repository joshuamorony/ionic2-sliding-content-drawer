## Example Usage

```
<ion-content padding>
  The world is your oyster.
  <p>
    If you get lost, the <a href="http://ionicframework.com/docs/v2">docs</a> will be your guide.
  </p>
</ion-content>

<content-drawer [options]="drawerOptions">
	<div class="content">
	  The world is your oyster.
	  <p>
	    If you get lost, the <a href="http://ionicframework.com/docs/v2">docs</a> will be your guide.
	  </p>
	</div>
</content-drawer>
```

```
import { Component } from '@angular/core';
import { NavController } from 'ionic-angular';

@Component({
  selector: 'page-home',
  templateUrl: 'home.html'
})
export class HomePage {

	drawerOptions: any;

	constructor(public navCtrl: NavController) {

		this.drawerOptions = {
			handleHeight: 50,
			thresholdFromBottom: 200,
			thresholdFromTop: 200,
			bounceBack: true
		};

	}

}
```

**handleHeight** - How big the handle to pull the drawer area up and down should be
**thresholdFromBottom** - How far from the bottom the handle should be before snapping to the bottom
**thresholdFromTop** - How far from the top the handle should be before snapping to the top
**bounceBack** - If true, the drawer will always snap to the top or bottom when released (whichever is closer based on the threshold)