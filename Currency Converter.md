// HW08 - JavaFX Currency Converter
// By Min Chang

Dollars to Pounds
Input value: $10000
Exchange 8100.00

Input value: $one grand
Error Invalid Dollar Amount
Please only use digits.

// As shown, the program converts a Dollar input value to its corresponding Pound value. 
// Once the user clicks the Exchange button, the input value is converted and the Pound 
// value is printed below the button. If the user inputs a non-numeric value, an error message is displayed.






Java Code: 

import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.Alert;
import javafx.scene.control.TextField;
import javafx.scene.layout.HBox;
import javafx.scene.layout.VBox;
import javafx.scene.text.Text;
import javafx.scene.control.Label;
import javafx.stage.Stage;
import javafx.scene.control.Alert;

public class DollarsToPounds extends Application {

    final static double EXCHANGE_RATE = 0.81;

    public void start(Stage stage) {

        Label valueLbl = new Label("Input value: $");

        Label poundsLbl = new Label();

        TextField dollarsTxt = new TextField();

        Button exchangeBtn = new Button("Exchange");

        exchangeBtn.setOnAction(event -> {
            String dollarsStr = dollarsTxt.getText();
            try {
                double dollars = Double.parseDouble(dollarsStr);
                double pounds = exchange(dollars);
                poundsLbl.setText(String.format("%.2f", pounds));
            } catch (NumberFormatException e) {
                Alert a = new Alert(Alert.AlertType.ERROR)
                a.setTitle("Error");
                a.setHeaderText("Invalid Dollar Amount");
                a.setContentText("Please only use digits.");
                a.showAndWait();
            }
        });

        HBox input = new HBox();
        input.setAlignment(Pos.CENTER);
        input.getChildren().addAll(valueLbl, dollarsTxt); // Filled "getChildren().addAll"

        VBox root = new VBox(); // Filled "VBox"
        root.setAlignment(Pos.CENTER);
        root.setSpacing(8);
        root.getChildren().addAll(input, exchangeBtn, poundsLbl); // Filled "getChildren().addAll"

        Scene scene = new Scene(root, 400, 400); // Filled "Scene", "root", "400, 400"
        stage.setTitle("Dollars to Pounds"); // Filled "setTitle"
        stage.setScene(scene); // Filled "setScene(scene)"
        stage.show();
    }

    private double exchange(double dollars) {
        return dollars * EXCHANGE_RATE; // Filled "EXCHANGE_RATE"
    }

    public static void main(String[] args) {
        launch(args);
    }
}



