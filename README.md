# Completed-Rectangle-Class
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Rectangle01;
using NUnit.Framework;

namespace SENG8040_Assignment_1_tests
{
    [TestFixture]
    class SENG8040_Assignment1_tests
    {
        [Test]
        public void GetLength_input5_expectedlengthresultequals5()
        {
            //arrange
            int l = 5;
            int w = 4;
            Rectangle.Rect testrectangle = new Rectangle.Rect(l, w);

            //act
            int length = testrectangle.GetLength();

            //assert
            Assert.AreEqual(l, length);

        }
        [Test]
        public void SetLength_input6_expectedsetlengthtoequals6()
        {
            //arrange
            int l = 6;
            int w = 7;
            Rectangle.Rect testrectangle = new Rectangle.Rect(l, w);

            //act
            int length = testrectangle.SetLength(l);

           //assert
            Assert.AreEqual(l, length);
        }
        [Test]
        public void GetWidth_input10_expectedwidthtoequals10()
        {
            //arrange
            int l = 2;
            int w = 10;
            Rectangle.Rect testrectangle = new Rectangle.Rect(l, w);

            //act
            int width = testrectangle.GetWidth();

            //assert
            Assert.AreEqual(w, width);
        }
        [Test]
        public void SetWidth_input15_expectedsetWidthtoequals15()
        {
            //arrange
            int l = 4;
            int w = 15;
            Rectangle.Rect testrectangle = new Rectangle.Rect(l, w);

            //act
            int width = testrectangle.SetWidth(w);

            //assert
            Assert.AreEqual(w, width);
        }
        [Test]
        public void GetPerimeter_inputlength2width8_expectedGetperimeterequals20()
        {
            //arrange
            int l = 2;
            int w = 8;
            int perimeter = 2 * (l + w);
            Rectangle.Rect testrectangle = new Rectangle.Rect(l, w);

            //act
            int expectedresult = testrectangle.GetPerimeter();

            //assert
            Assert.AreEqual(perimeter, expectedresult);
        }
        [Test]

        public void GetArea_inputlength3width9_expectedGetAreaequals27()
        {
            //arrange
            int l = 3;
            int w = 9;
            int area = (l * w);
            Rectangle.Rect testrectangle = new Rectangle.Rect(l, w);

            //act
            int expectedResult = testrectangle.GetArea();

            //assert
            Assert.AreEqual(area, expectedResult);
        }
    }
}











       
