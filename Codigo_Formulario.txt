package Prueba;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JPanel;
import java.awt.Color;
import javax.swing.JLabel;
import javax.swing.JOptionPane;
import javax.swing.JTextField;
import java.awt.Font;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;

public class WindowsBuilder {

	private JFrame frame;
	private JTextField txtCodigo;
	private JTextField txtNombre;
	private JTextField txtExtension;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					WindowsBuilder window = new WindowsBuilder();
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
	public WindowsBuilder() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.getContentPane().setBackground(new Color(221, 160, 221));
		frame.setBounds(100, 100, 450, 300);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		JPanel panel = new JPanel();
		panel.setBackground(new Color(0, 255, 255));
		panel.setBounds(41, 41, 341, 176);
		frame.getContentPane().add(panel);
		panel.setLayout(null);
		
		JLabel lblNewLabel = new JLabel("C\u00F3digo Departamento");
		lblNewLabel.setFont(new Font("Tahoma", Font.PLAIN, 12));
		lblNewLabel.setBounds(34, 35, 128, 14);
		panel.add(lblNewLabel);
		
		JLabel lblNombreDepartamento = new JLabel("Nombre Departamento");
		lblNombreDepartamento.setFont(new Font("Tahoma", Font.PLAIN, 12));
		lblNombreDepartamento.setBounds(34, 76, 128, 14);
		panel.add(lblNombreDepartamento);
		
		JLabel lblExtensinDepartamento = new JLabel("Extensi\u00F3n Departamento");
		lblExtensinDepartamento.setFont(new Font("Tahoma", Font.PLAIN, 12));
		lblExtensinDepartamento.setBounds(34, 117, 144, 14);
		panel.add(lblExtensinDepartamento);
		
		txtCodigo = new JTextField();
		txtCodigo.setBounds(182, 33, 109, 20);
		panel.add(txtCodigo);
		txtCodigo.setColumns(10);
		
		txtNombre = new JTextField();
		txtNombre.setBounds(182, 74, 109, 20);
		panel.add(txtNombre);
		txtNombre.setColumns(10);
		
		txtExtension = new JTextField();
		txtExtension.setBounds(182, 115, 109, 20);
		panel.add(txtExtension);
		txtExtension.setColumns(10);
		
		JLabel lblNewLabel_1 = new JLabel("FORMULARIO");
		lblNewLabel_1.setFont(new Font("Tahoma", Font.BOLD, 14));
		lblNewLabel_1.setBounds(164, 11, 137, 19);
		frame.getContentPane().add(lblNewLabel_1);
		
		JButton btnNewButton = new JButton("Inserte Datos");
		btnNewButton.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				System.out.println("SE HA PULSADO EL BOTÓN INSERTAR");
				JOptionPane.showMessageDialog(btnNewButton, "Se ha pulsado el botón correctamente.");
			}
		});
		btnNewButton.setBounds(63, 228, 119, 23);
		frame.getContentPane().add(btnNewButton);
		
		JButton btnNewButton_1 = new JButton("Salir");
		btnNewButton_1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				System.out.println("SE HA PULSADO EL BOTÓN LIMPIAR");
				System.exit(0);
			}
		});
		btnNewButton_1.setBounds(265, 228, 89, 23);
		frame.getContentPane().add(btnNewButton_1);
	}
}
