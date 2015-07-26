# WSProgressHUD
This is a beauful hud view for iPhone &amp; iPad

![Demo](https://raw.githubusercontent.com/devSC/WSProgressHUD/master/Demo/Demo.gif)

#Usage
To run the WSProgressHUD project

``` objc
//Show on the self.view

@implementation ViewController
{
    WSProgressHUD *hud;
}
- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.

    //Add HUD to view
    hud = [[WSProgressHUD alloc] initWithView:self.navigationController.view];
    [self.view addSubview:hud];

    //show
    [hud showWithString:@"Wating..." maskType:WSProgressHUDMaskTypeBlack];

    dispatch_after(dispatch_time(DISPATCH_TIME_NOW, (int64_t)(1 * NSEC_PER_SEC)), dispatch_get_main_queue(), ^{
        [hud dismiss];
    });

}

//Show on the window
    //show
    [WSProgressHUD show];

    //Show with mask
    [WSProgressHUD showWithMaskType:WSProgressHUDMaskTypeBlack];
    
    //Show with mask without tabbar
    [WSProgressHUD showWithStatus:@"Loading..." maskType:WSProgressHUDMaskTypeBlack maskWithout:WSProgressHUDMaskWithoutTabbar];
    
    //Show with string
    [WSProgressHUD showWithStatus:@"Loading..."];

    //Show with facebook shimmering
    [WSProgressHUD showShimmeringString:@"WSProgressHUD Loading..."];

    //Show with Progress
    [WSProgressHUD showProgress:progress status:@"Updating..."];

    //Show with image
    [WSProgressHUD showSuccessWithStatus:@"Thanks.."];
    
    //Show with string
    [WSProgressHUD showImage:nil status:@"WSProgressHUD"]

    //Dismiss
    [WSProgressHUD dismiss];
```

##Thanks

@Shimmering
@SVProgressHUD
@MMMaterialDesignSpinner

## Author
Wilson-yuan, wilson.yuan.dev@gmail.com

## License
WSProgressHUD is available under the MIT license. See the LICENSE file for more info.





