# data-penjualan
tugas pemrograman visual
import javax.swing.*;

public class FormPelanggan extends JFrame {
    private JLabel lblNama, lblAlamat, lblTelepon;
    private JTextField txtNama, txtAlamat, txtTelepon;
    private JButton btnSimpan;

    public FormPelanggan() {
        setTitle("Form Data Pelanggan");
        setSize(300, 250);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        setLocationRelativeTo(null);
        setLayout(null);

        lblNama = new JLabel("Nama:");
        lblAlamat = new JLabel("Alamat:");
        lblTelepon = new JLabel("Telepon:");

        txtNama = new JTextField();
        txtAlamat = new JTextField();
        txtTelepon = new JTextField();

        btnSimpan = new JButton("Simpan");

        lblNama.setBounds(20, 20, 80, 25);
        txtNama.setBounds(100, 20, 150, 25);

        lblAlamat.setBounds(20, 60, 80, 25);
        txtAlamat.setBounds(100, 60, 150, 25);

        lblTelepon.setBounds(20, 100, 80, 25);
        txtTelepon.setBounds(100, 100, 150, 25);

        btnSimpan.setBounds(100, 150, 100, 30);

        add(lblNama);
        add(txtNama);
        add(lblAlamat);
        add(txtAlamat);
        add(lblTelepon);
        add(txtTelepon);
        add(btnSimpan);

        btnSimpan.addActionListener(e -> {
            String nama = txtNama.getText();
            String alamat = txtAlamat.getText();
            String telepon = txtTelepon.getText();

            JOptionPane.showMessageDialog(this,
                "Data Tersimpan:\nNama: " + nama + "\nAlamat: " + alamat + "\nTelepon: " + telepon);
        });
    }

    public static void main(String[] args) {
        new FormPelanggan().setVisible(true);
    }
}
