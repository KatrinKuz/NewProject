using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApplication7
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            double summa, razn, svet, lampa;
            if (double.TryParse(textBox1.Text, out summa) && double.TryParse(textBox2.Text, out razn))
            {
                svet = (summa - razn) / 2;
                lampa = svet + razn;
                textBox3.Text = String.Format("Стоимость светодиода: {0};стоимость энергосберегающей лампы: {1}", svet, lampa);
                return;
            }
        }
    }
}
