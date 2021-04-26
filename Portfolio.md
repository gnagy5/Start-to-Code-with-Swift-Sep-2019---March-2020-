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

