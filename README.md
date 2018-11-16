# programa-inicial
Laura Cuartas Pascual bravo

using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApp1
{
    static class Program
    {
        /// <summary>
        /// Punto de entrada principal para la aplicación.
        /// </summary>
        [STAThread]
        static void Main()
        {
            Application.EnableVisualStyles();
            Application.SetCompatibleTextRenderingDefault(false);
            Application.Run(new frmOpMat());
        }
    }
}

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApp1
{
    public partial class frmOpMat : Form
    {
        public frmOpMat()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {

            //se inicializan la variables en 0
            lblAumentoA.Text = "";
            lblAumentoB.Text = "";
            lblAumentoC.Text = "";
            lblNuevoA.Text = "";
            lblNuevoB.Text = "";
            lblNuevoC.Text = "";
            lblFormula.Text = "";
            lblDtoDvA.Text = "";
            lblDtoDvB.Text = "";
            lblDtoDvC.Text = "";
            lblNvaDvA.Text = "";
            lblNvaDvB.Text = "";
            lblNvaDvC.Text = "";



        }
        //Botón para calcular el porcentaje de aumento del arriendo
        private void btnAumento_Click(object sender, EventArgs e)
        {
            //declaración de variables

            double a = Convert.ToDouble(txtA.Text);
            double b = Convert.ToDouble(txtB.Text);
            double c = Convert.ToDouble(txtC.Text);

            //declaración de variables y operaciones
            double x = a * 0.08;
            double y = b * 0.08;
            double z = c * 0.08;

            //impresión en labels
            lblAumentoA.Text = x.ToString();
            lblAumentoB.Text = y.ToString();
            lblAumentoC.Text = z.ToString();

        }
        //botón para calcular el valor del arriendo más el aumento
        private void btnNuevo_Click(object sender, EventArgs e)
        {
            //declaración de variables
            double a = Convert.ToDouble(txtA.Text);
            double b = Convert.ToDouble(txtB.Text);
            double c = Convert.ToDouble(txtC.Text);

            //declaración de variables y operaciones
            double x = (a * 0.08) + a;
            double y = (b * 0.08) + b;
            double z = (c * 0.08) + c;

            //impresión en labels
            lblNuevoA.Text = x.ToString();
            lblNuevoB.Text = y.ToString();
            lblNuevoC.Text = z.ToString();
        }

        private void lblNuevoB_Click(object sender, EventArgs e)
        {

        }

        private void lblAumentoB_Click(object sender, EventArgs e)
        {

        }

        private void lblAumentoC_Click(object sender, EventArgs e)
        {

        }

        private void lblNuevoC_Click(object sender, EventArgs e)
        {

        }

        private void lblNuevoA_Click(object sender, EventArgs e)
        {

        }

        private void lblAumentoA_Click(object sender, EventArgs e)
        {

        }

        //botón para conocer el porcentaje de decremento de la divisa
        private void button2_Click(object sender, EventArgs e)
        {
            //declaración de variables
            double a = Convert.ToDouble(txtA.Text);
            double b = Convert.ToDouble(txtB.Text);
            double c = Convert.ToDouble(txtC.Text);

            //declaración de variables y operaciones
            double x = (a * 0.05);
            double y = (b * 0.07);
            double z = (c * 0.06);

            //impresión de resultados en labels
            lblDtoDvA.Text = x.ToString();
            lblDtoDvB.Text = y.ToString();
            lblDtoDvC.Text = z.ToString();

        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void label2_Click(object sender, EventArgs e)
        {

        }

        private void label3_Click(object sender, EventArgs e)
        {

        }

        private void label4_Click(object sender, EventArgs e)
        {

        }

        private void label5_Click(object sender, EventArgs e)
        {

        }

        private void label6_Click(object sender, EventArgs e)
        {

        }

        //botón para calcular el valor de la divisa menos el porcentaje de decremento
        private void button1_Click(object sender, EventArgs e)
        {

            //declaración de variables
            double a = Convert.ToDouble(txtA.Text);
            double b = Convert.ToDouble(txtB.Text);
            double c = Convert.ToDouble(txtC.Text);

            //declaración de variables y operaciones
            double x = a - (a * 0.05);
            double y = b - (b * 0.07);
            double z = c - (c * 0.06);

            //impresión de resultados en labels
            lblNvaDvA.Text = x.ToString();
            lblNvaDvB.Text = y.ToString();
            lblNvaDvC.Text = z.ToString();

        }

        //botón para fórmula del estudiante
        private void btnFormula_Click(object sender, EventArgs e)
        {
            //declaración de variables
            double a = Convert.ToDouble(txtA.Text);
            double b = Convert.ToDouble(txtB.Text);
            double c = Convert.ToDouble(txtC.Text);

            //declaración de variables y operaciones
            double t = 4 * a * c;
            double s = b * b;
            double x = s - t;

            //condicional para validar que "b al cuadrado" es mayor que 4ac
            if (s > t)
            {
                //operación para calucarl la raiz cuadrada y la división por 2a
                double y = Math.Sqrt(x);
                double z = (-b + y);
                double w = z / (a + a);

                //impresión de resultados
                lblFormula.Text = w.ToString();
            }

            //en caso de que "b al cuadrado" no sea mayor que 4ac, aparecerá esta ventana de texto
            else
            { MessageBox.Show("El valor de B al cuadrado debe ser mayor o igual que 4ac"); }
        }

        private void grpDivisas_Enter(object sender, EventArgs e)
        {

        }
    }
}
        
