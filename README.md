# student-kurs
import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JTabbedPane;
import java.awt.BorderLayout;
import javax.swing.JButton;
import javax.swing.JTextPane;
import javax.swing.JTextField;
import javax.swing.JLabel;
import javax.swing.JTable;
import javax.swing.JComboBox;
import java.awt.GridBagLayout;
import java.awt.GridBagConstraints;
import java.awt.Insets;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;

public class gui {

	private JFrame frame;
	private JTextField txtSkrivInKurskodpersonnummer;
	private JTable table;
	private JTextField txtPersonnummer;
	private JTextField txtNamn;
	private JTextField txtAdress;
	private JTextField txtKursnummer;
	private JTextField textField_1;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					gui window = new gui();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public gui() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.setBounds(100, 100, 627, 599);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		JTabbedPane tabbedPane = new JTabbedPane(JTabbedPane.TOP);
		tabbedPane.setBounds(0, 0, 606, 21);
		frame.getContentPane().add(tabbedPane);
		
		JTabbedPane tabbedPane_1 = new JTabbedPane(JTabbedPane.TOP);
		tabbedPane.addTab("New tab", null, tabbedPane_1, null);
		
		JTabbedPane tabbedPane_2 = new JTabbedPane(JTabbedPane.TOP);
		tabbedPane.addTab("New tab", null, tabbedPane_2, null);
		
		JLabel lblAngeKurskodpersonnummer = new JLabel("Ange kurskod/personnummer");
		lblAngeKurskodpersonnummer.setBounds(10, 19, 190, 16);
		frame.getContentPane().add(lblAngeKurskodpersonnummer);
		
		txtSkrivInKurskodpersonnummer = new JTextField();
		txtSkrivInKurskodpersonnummer.setBounds(10, 40, 134, 28);
		frame.getContentPane().add(txtSkrivInKurskodpersonnummer);
		txtSkrivInKurskodpersonnummer.setColumns(10);
		
		JButton btnSkKurs = new JButton("Sök Kurs");
		btnSkKurs.setBounds(10, 73, 99, 29);
		frame.getContentPane().add(btnSkKurs);
		
		JButton btnSkStudent = new JButton("Sök Student");
		btnSkStudent.setBounds(114, 73, 119, 29);
		frame.getContentPane().add(btnSkStudent);
		
		table = new JTable();
		table.setBounds(20, 114, 586, 199);
		frame.getContentPane().add(table);
		
		JLabel lblLggTillStudent = new JLabel("Lägg till Student");
		lblLggTillStudent.setBounds(10, 325, 103, 16);
		frame.getContentPane().add(lblLggTillStudent);
		
		txtPersonnummer = new JTextField();
		txtPersonnummer.setBounds(10, 347, 134, 28);
		txtPersonnummer.setText("Personnummer");
		frame.getContentPane().add(txtPersonnummer);
		txtPersonnummer.setColumns(10);
		
		txtNamn = new JTextField();
		txtNamn.setBounds(10, 380, 134, 28);
		txtNamn.setText("Namn");
		frame.getContentPane().add(txtNamn);
		txtNamn.setColumns(10);
		
		txtAdress = new JTextField();
		txtAdress.setBounds(10, 413, 134, 28);
		txtAdress.setText("Adress");
		txtAdress.setColumns(10);
		frame.getContentPane().add(txtAdress);
		
		JLabel lblVljKurs = new JLabel("Välj kurs");
		lblVljKurs.setBounds(10, 453, 99, 16);
		frame.getContentPane().add(lblVljKurs);
		
		JComboBox comboBox = new JComboBox();
		comboBox.setBounds(10, 473, 134, 27);
		frame.getContentPane().add(comboBox);
		
		JButton btnRegistera = new JButton("Registera");
		btnRegistera.setBounds(7, 501, 102, 29);
		frame.getContentPane().add(btnRegistera);
		
		JLabel lblLggTillKurs = new JLabel("Lägg till Kurs");
		lblLggTillKurs.setBounds(174, 325, 103, 16);
		frame.getContentPane().add(lblLggTillKurs);
		
		txtKursnummer = new JTextField();
		txtKursnummer.setText("Kurskod");
		txtKursnummer.setColumns(10);
		txtKursnummer.setBounds(174, 347, 134, 28);
		frame.getContentPane().add(txtKursnummer);
		
		textField_1 = new JTextField();
		textField_1.setText("Namn");
		textField_1.setColumns(10);
		textField_1.setBounds(174, 380, 134, 28);
		frame.getContentPane().add(textField_1);
		
		JButton button = new JButton("Registera");
		button.setBounds(175, 414, 102, 29);
		frame.getContentPane().add(button);
		
		JComboBox comboBox_1 = new JComboBox();
		comboBox_1.setBounds(354, 349, 119, 27);
		frame.getContentPane().add(comboBox_1);
		
		JLabel lblSttBetyg = new JLabel("Sätt betyg");
		lblSttBetyg.setBounds(354, 325, 80, 16);
		frame.getContentPane().add(lblSttBetyg);
		
		JComboBox comboBox_2 = new JComboBox();
		comboBox_2.setBounds(354, 382, 119, 27);
		frame.getContentPane().add(comboBox_2);
		
		JComboBox comboBox_3 = new JComboBox();
		comboBox_3.setBounds(354, 415, 119, 27);
		frame.getContentPane().add(comboBox_3);
		
		JButton btnNewButton = new JButton("Sätt betyg");
		btnNewButton.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			}
		});
		btnNewButton.setBounds(356, 448, 117, 29);
		frame.getContentPane().add(btnNewButton);
	}
}
