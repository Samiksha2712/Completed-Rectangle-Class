# Completed-Rectangle-Class
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Rectangle
{
    public class Rect
    {
        private int l1;
        private int w1;


        public Rect()
        {
            l1 = 1;
            w1 = 1;
        }

        public Rect(int l1, int w1)
        {
            this.l1 = l1;
            this.w1 = w1;
        }

        public int GetLength()
        {
            return l1;
        }


        public int SetLength(int l1)
        {
            this.l1 = l1;
            return this.l1;
        }


        public int GetWidth()
        {
            return w1;
        }


        public int SetWidth(int w1)
        {
            this.w1 = w1;
            return this.w1;
        }

        public int GetPerimeter()
        {
            return (2 * l1) + (2 * w1);
        }

        public int GetArea()
        {
            return l1 * w1;
        }
    }
}

       
