# superbrowser | How To Create A Web Browser In C# 

How To Create A Web Browser In C#
YouTube tutorial OOP Ep. 2

```C#
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace superbrowser
{
    public partial class mainForm : Form
    {
        public mainForm()
        {
            InitializeComponent();
        }

        #region methods

        public void facebookNavigate()
        {
            webBrowser1.Navigate("http://www.facebook.com");
        }

        public void youtubeNavigate()
        {
            webBrowser1.Navigate("http://www.youtube.com");
        }

        public void twitterNavigate()
        {
            webBrowser1.Navigate("http://www.twitter.com");
        }

        #endregion


        private void exitToolStripMenuItem_Click(object sender, EventArgs e)
        {
            this.Close();
        }

        private void aboutToolStripMenuItem_Click(object sender, EventArgs e)
        {
            MessageBox.Show("This webbrowser was made by Chris aka dark knight", "Title");
        }

        private void facebookToolStripMenuItem_Click(object sender, EventArgs e)
        {
            facebookNavigate();
        }

        private void youTubeToolStripMenuItem_Click(object sender, EventArgs e)
        {
            youtubeNavigate();
        }

        private void twitterToolStripMenuItem_Click(object sender, EventArgs e)
        {
            twitterNavigate();
        }

        private void searchButton_Click(object sender, EventArgs e)
        {
            webBrowser1.Navigate(textBox1.Text);
        }

        private void textBox1_KeyPress(object sender, KeyPressEventArgs e)
        {
            if(e.KeyChar == (char)ConsoleKey.Enter)
            {
                webBrowser1.Navigate(textBox1.Text);
            }
        }

        private void pictureBox1_Click(object sender, EventArgs e)
        {
            twitterNavigate();
        }

        private void pictureBox2_Click(object sender, EventArgs e)
        {
            facebookNavigate();
        }

        private void pictureBox3_Click(object sender, EventArgs e)
        {
            youtubeNavigate();
        }
    }
}

```
