# UIButton-Configuration

//  ViewController.swift
//  UIButtonProperties
//
//  Created by TanjilaNur-00115 on 28/4/23.

import UIKit

class ViewController: UIViewController {

    @IBOutlet weak var button: UIButton!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
    }

    @IBAction func practiceButton(_ sender: UIButton) {
        //do what will happen after clicking
    }
    
    func configureTitle() {
        //1. titleLabel: This property returns the label that is used to display the button’s text.
        
        let titleLabel = button.titleLabel
        titleLabel?.font = UIFont.systemFont(ofSize: 20)
        titleLabel?.textColor = UIColor.blue
        
        //12. setTitle(_ title: String?, for state: UIControl.State): This method sets the title for a specified state.
        
        button.setTitle("Click me", for: .normal)
        button.setTitle("Don't click", for: .disabled)
    }
    
    func configureTintColor() {
        //2. tintColor: This property sets the color of the button’s text, image, and background.
        
        button.tintColor = UIColor.red
    }
    
    func configureSetImage() {
        //13. setImage(_ image: UIImage?, for state: UIControl.State): This method sets the image for a specified state.
        
        button.setImage(UIImage(named: "heart_icon"), for: .normal)
        button.setImage(UIImage(named: "heart_icon"), for: .disabled)
    }
    
    func configureBackgroundImage() {
        //11. backgroundImage(for state: UIControl.State): This method returns the background image for a specified state.
        
        let backgroundImage = UIImage(named: "background")
        button.setBackgroundImage(backgroundImage, for: .normal)
    }
    
    func configureContentHorizontalAlignment() {
        //4. contentHorizontalAlignment: This property sets the horizontal alignment of the button’s title and image within the button.
        
        button.contentHorizontalAlignment = .left
    }

    func configureContentVerticalAlignment() {
        //5. contentVerticalAlignment: This property sets the vertical alignment of the button’s title and image within the button.
        
        button.contentVerticalAlignment = .center
    }
    
    func configureAddTarget() {
        //14. addTarget(_ target: Any?, action: Selector, for controlEvents: UIControl.Event): This method adds a target and action for a specified control event.
        
        button.setTitle("Click me", for: .normal)
        button.addTarget(self, action: #selector(buttonTapped), for: .touchUpInside)
    }
    @objc func buttonTapped() {
      print("Button tapped")
    }
    
    func configureContentEdgeInsets() {
        //3. contentEdgeInsets: This property sets the padding between the button’s title, image, and the edges of the button.
        
        button.contentEdgeInsets = UIEdgeInsets(top: 10, left: 20, bottom: 10, right: 20)
    }
    
    func configureImageEdgeInsets() {
        //6. imageEdgeInsets: This property sets the padding between the button’s image and the edges of the button.
        
        button.imageEdgeInsets = UIEdgeInsets(top: 0, left: 10, bottom: 0, right: 0)
    }
    
    func configureTitleEdgeInsets() {
        //7. titleEdgeInsets: This property sets the padding between the button’s title and the edges of the button.
        
        button.titleEdgeInsets = UIEdgeInsets(top: 0, left: 0, bottom: 0, right: 10)
    }
    
    func configureAdjustsImageWhenHighlighted() {
        //8. adjustsImageWhenHighlighted: This property determines whether the button’s image changes when the button is highlighted.
        
        button.adjustsImageWhenHighlighted = true
    }
    
    func configureAdjustsImageWhenDisabled() {
        //9. adjustsImageWhenDisabled: This property determines whether the button’s image changes when the button is disabled.
        
        button.adjustsImageWhenDisabled = true
    }
    
    func configureShowsTouchWhenHighlighted() {
        //10. showsTouchWhenHighlighted: This property determines whether a highlight is shown when the button is touched.
        
        button.showsTouchWhenHighlighted = true
    }
}
