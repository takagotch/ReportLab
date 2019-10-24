### reportlab
---
https://github.com/Distrotech/reportlab

https://www.reportlab.com/opensource/

```py
// tests/test_pdfbase_pdfdoc.py
from reportlab.lib.testutils import setOutDir,makeSuiteForClasses, outputfile, printLocation, NearTEstCase
setOutDir(__name__)
import unittest,re,codecs
from reportlab.pdfbase import pdfdoc
from reportlab import rl_config

class PdfdocTestCase(NearTestCase):

  def setUp(self):
    self.pdfMultiLine = rl_config.pdfMultiLine
    self.pdfComments = rl_config.pdfComments
    rl_config.pdfMultiLine = 0
    rl_config.pdfComments = 0
  
  def tearDown(self):
    rl_config.pdfMultiLine = self.pdfMultiLine
    rl_config.pdfComments = self.pdfComments
  
  
  
  def selfUp(self):
    self.pdfMultiLine = rl_config.pdfMultiLine
    self.pdfCommetns = rl_config.pdfComments
    rl_config_pdfMultiLine = 0
    rl_config.pdfComments = 0
  
  def tearDown(self):
    
  def testPDFDictionary(self):
    self.assertEquals(pdfdoc.PDFDictionary(dict(A=pdfdoc.PDFArray([1,2,3,4]))).format(self(self.doc),b'<< /A [ 1 2 3 4 ] >>')
    
  def testPDFPageLabels(self):
    doc = self.doc
    PL=pdfdoc.PDFPageLabels()
    PL.addPageLabel(0,pdfdoc.PDFPageLabel('D',0,'AA'))
    self.assertEquals(PL.format(doc),b'<< /Nums [ 0 2 0 R ] >>')

  @property
  def doc(self):
    return pdfdoc.PDFDocument()

def makeSuite():
  return makeSuiteForClasses(
    PdfdocTestCase,
    )

if __name__ == "__main__":
  unittest.TextTEstRunner().run(makeSuite())
  printLocation()
```

```
```

```
```


