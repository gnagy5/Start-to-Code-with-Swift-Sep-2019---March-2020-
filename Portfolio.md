## Portfolio

Here is an example of some Swift coding I made in my recent "Start to Code in Swift" class at OSU.

```markdown
//
//  ViewController.swift
//  Login
//
//  Created by Nagy, Gregory E. on 7/28/20.
//  Copyright © 2020 Greg Nagy. All rights reserved.
//  Greg Nagy 8-4-2020

import UIKit

class ViewController: UIViewController {
    @IBOutlet var userName: UITextField!
    @IBOutlet var forgotUserNameButton: UIButton!
    @IBOutlet var forgotPasswordButton: UIButton!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
    }
    @IBAction func forgotUserNameTapped(_ sender: Any) {
    performSegue(withIdentifier: "FullLoginSegue", sender: forgotUserNameButton)
    }
    @IBAction func forgotPasswordTapped(_ sender: Any) {
    performSegue(withIdentifier: "FullLoginSegue", sender: forgotPasswordButton)
    }
    
    override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
        guard let sender = sender as? UIButton else {return}
        if sender == forgotPasswordButton {
            segue.destination.navigationItem.title = "Forgot Password"
        } else if sender == forgotUserNameButton {
            segue.destination.navigationItem.title = "Forgot Username"
        } else {
            segue.destination.navigationItem.title = userName.text
        }
    }
}
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/gnagy5/Start-to-Code-with-Swift-Sep-2019---March-2020-/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

