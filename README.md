# Tourism_tot

#Store data in nfc
public NdefMessage createTextMessage(String content) {
 try {
    byte[] lang = Locale.getDefault().getLanguage().getBytes("**************************");
    byte[] text = content.getBytes("************************"); 

    int langSize = lang.length;
    int textLength = text.length;

    ByteArrayOutputStream payload = new ByteArrayOutputStream(1 + langSize + textLength);
 
 
 #  payload.write((byte) (langSize & 0x1F));
    payload.write(lang, 0, langSize);
    payload.write(text, 0, textLength);
    NdefRecord record = new NdefRecord(NdefRecord.TNF_WELL_KNOWN,
    NdefRecord.RTD_TEXT, new byte[0],
    payload.toByteArray());
    return new NdefMessage(new NdefRecord[]{record});
  }
  catch (Exception e) {
    e.printStackTrace();
  }

  return null;
}

# Creating database
public NdefMessage createTextMessage(String content) {
 try {
    byte[] lang = Locale.getDefault().getLanguage().getBytes("**************************");
    byte[] text = content.getBytes("************************"); 

    int langSize = lang.length;
    int textLength = text.length;

    ByteArrayOutputStream payload = new ByteArrayOutputStream(1 + langSize + textLength);
    payload.write((byte) (langSize & 0x1F));
    payload.write(lang, 0, langSize);
    payload.write(text, 0, textLength);
    NdefRecord record = new NdefRecord(NdefRecord.TNF_WELL_KNOWN,
    NdefRecord.RTD_TEXT, new byte[0],
    payload.toByteArray());
    return new NdefMessage(new NdefRecord[]{record});
  }
  catch (Exception e) {
    e.printStackTrace();
  }

  return null;
}
        #region Windows Form Designer generated code  
	  
       /// <summary>  
	        /// Required method for Designer support - do not modify  
	        /// the contents of this method with the code editor.  
	        /// </summary>  
	        private void InitializeComponent()  
	        {  this.txttag = new System.Windows.Forms.TextBox();  
	            this.label1 = new System.Windows.Forms.Label();  
	            this.label2 = new System.Windows.Forms.Label();  
	            this.label3 = new System.Windows.Forms.Label();  
	            this.label4 = new System.Windows.Forms.Label(); 
              this.label5 = new System.Windows.Forms.Label();  
           this.txtstudname = new System.Windows.Forms.TextBox();  
	            this.txtrollno = new System.Windows.Forms.TextBox();  
	            this.comboclass = new System.Windows.Forms.ComboBox();  
	            this.combosec = new System.Windows.Forms.ComboBox();  
	            this.btnsubmit = new System.Windows.Forms.Button();  	            this.btncancel = new System.Windows.Forms.Button();  
            this.SuspendLayout();  .	            //   
	            // txttag .	            //   
	            this.txttaocation = new System.Drawing.Point(138, 50);  
	            this.txttag.Name = "txttag";  
	            this.txttag.Size = new System.Drawing.Size(100, 20);  
	            this.txttag.TabIndex = 0;  
	            //   
	            // label1  
	            //   
	            this.label1.AutoSize = true;  
	            this.label1.Location = new System.Drawing.Point(60, 50);  
	            this.label1.Name = "label1";  
	            this.label1.Size = new System.Drawing.Size(40, 13);  
	            this.label1.TabIndex = 1;  
	            this.label1.Text = "Tag ID";  
	            //   
	            // label2  
	            //   
	            this.label2.AutoSize = true;  
	            this.label2.Location = new System.Drawing.Point(44, 78);  
	            this.label2.Name = "label2";  
	            this.label2.Size = new System.Drawing.Size(75, 13);  
	            this.label2.TabIndex = 2;  
	            this.label2.Text = "Student Name";  
	            //   
	            // label3  
          //   
          this.label3.AutoSize = true;  
	            this.label3.Location = new System.Drawing.Point(60, 108);  
	            this.label3.Name = "label3";  
	            this.label3.Size = new System.Drawing.Size(42, 13);  
	            this.label3.TabIndex = 3;  
	            this.label3.Text = "Roll No";  
	            //   
	            // label4  
	            //   
	            this.label4.AutoSize = true;  
	            this.label4.Location = new System.Drawing.Point(60, 135);  
	            this.label4.Name = "label4";  
	            this.label4.Size = new System.Drawing.Size(32, 13);  
	            this.label4.TabIndex = 4;  
	            this.label4.Text = "Class";  
	            //   
	            // label5  
	            //   
            this.label5.AutoSize = true;  
	            this.label5.Location = new System.Drawing.Point(57, 163);  
	            this.label5.Name = "label5";  
	            this.label5.Size = new System.Drawing.Size(43, 13);  
	            this.label5.TabIndex = 5;  
	            this.label5.Text = "Section";  
	            //   
	            // txtstudname  
	            //   
	            this.txtstudname.Location = new System.Drawing.Point(138, 78);  
	            this.txtstudname.Name = "txtstudname";  
           this.txtstudname.Size = new System.Drawing.Size(100, 20);  
          this.txtstudname.TabIndex = 6;  
	            //   
	            // txtrollno  
	            //   
	            this.txtrollno.Location = new System.Drawing.Point(138, 105);  
	            this.txtrollno.Name = "txtrollno";  
	            this.txtrollno.Size = new System.Drawing.Size(100, 20);  
	            this.txtrollno.TabIndex = 7;  
	            //   
	            // comboclass  
	            //   
	            this.comboclass.FormattingEnabled = true;  
	            this.comboclass.Items.AddRange(new object[] {  
	            "I",  
	            "II",  
	            "III",  
	            "IV",  
	            "V",  
	            "VI",  
	            "VII",  
              "VIII",  
	            "IX",  	            
              "X"});  
	            this.comboclass.Location = new System.Drawing.Point(138, 132);  
	            this.comboclass.Name = "comboclass";  
.	            this.comboclass.Size = new System.Drawing.Size(121, 21);  
	            this.comboclass.TabIndex = 8;  
         //   
	            // combosec  
            //   
	            this.combosec.FormattingEnabled = true;  
	            this.combosec.Items.AddRange(new object[] {  
	            "A",  
	            "B",  
              "C",  
	            "D",  
              "E",  
              "F",  
	            "G",  
	            "H"});  
	            this.combosec.Location = new System.Drawing.Point(138, 160);  
	            this.combosec.Name = "combosec";  
	            this.combosec.Size = new System.Drawing.Size(121, 21);  
	            this.combosec.TabIndex = 9;  
	            //   
	            // btnsubmit  
	            //   
	            this.btnsubmit.Location = new System.Drawing.Point(105, 202);  
	            this.btnsubmit.Name = "btnsubmit";  
	            this.btnsubmit.Size = new System.Drawing.Size(75, 23);  
	            this.btnsubmit.TabIndex = 10;  
	            this.btnsubmit.Text = "Submit";  
            this.btnsubmit.UseVisualStyleBackColor = true;  
	            this.btnsubmit.Click += new System.EventHandler(this.btnsubmit_Click);  
	            //   
         // btncancel  
	            //   
	            this.btncancel.Location = new System.Drawing.Point(197, 202);  
	            this.btncancel.Name = "btncancel";  
	            this.btncancel.Size = new System.Drawing.Size(75, 23);  
	            this.btncancel.TabIndex = 11;  
	            this.btncancel.Text = "Cancel";  
	            this.btncancel.UseVisualStyleBackColor = true;  
	            //   
	            // Form1  
	            //   
	            this.AutoScaleDimensions = new System.Drawing.SizeF(6F, 13F);  
	            this.AutoScaleMode = System.Windows.Forms.AutoScaleMode.Font;  
	            this.ClientSize = new System.Drawing.Size(290, 261);  
	            this.Controls.Add(this.btncancel);  
	            this.Controls.Add(this.btnsubmit);  
	            this.Controls.Add(this.combosec);  
	            this.Controls.Add(this.comboclass);  
	            this.Controls.Add(this.txtrollno);  
	            this.Controls.Add(this.txtstudname);  
	            this.Controls.Add(this.label5);  
	            this.Controls.Add(this.label4);  
	            this.Controls.Add(this.label3);  
	            this.Controls.Add(this.label2);  
	            this.Controls.Add(this.label1);  
	            this.Controls.Add(this.txttag);  
            this.Name = "Form1";  
	            this.Text = "Form1";  
	            this.Load += new System.EventHandler(this.Form1_Load);  
	            this.ResumeLayout(false);  
	            this.PerformLayout();  
	  
	        }  
	 
	        #endregion  
	  
	        private System.Windows.Forms.TextBox txttag;  
	        private System.Windows.Forms.Label label1;  
	        private System.Windows.Forms.Label label2;  
	        private System.Windows.Forms.Label label3;  
	        private System.Windows.Forms.Label label4;  
	        private System.Windows.Forms.Label label5;  
	        private System.Windows.Forms.TextBox txtstudname;  
	        private System.Windows.Forms.TextBox txtrollno;  
	        private System.Windows.Forms.ComboBox comboclass;  
	        private System.Windows.Forms.ComboBox combosec;  
	        private System.Windows.Forms.Button btnsubmit;  
	        private System.Windows.Forms.Button btncancel;  
	    }  
	}  


