import UIKit
class ViewController: UIViewController {
  @IBOutlet weak var loadCellLabel: UILabel!
  override func viewDidLoad() {
    super.viewDidLoad()
    // Initialize the load cell sensor.
    let loadCell = LoadCell(scale: 100)
    // Start reading the load cell sensor.
    loadCell.startReading()
    // Update the load cell label with the current reading.
    let loadCellValue = loadCell.getLoadCellValue()
    loadCellLabel.text = String(loadCellValue)
  }
}
