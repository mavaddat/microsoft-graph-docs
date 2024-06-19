---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewPrintJob()
configuration := graphmodels.NewPrintJobConfiguration()
feedOrientation := graphmodels.LONGEDGEFIRST_PRINTERFEEDORIENTATION 
configuration.SetFeedOrientation(&feedOrientation) 


integerRange := graphmodels.NewIntegerRange()
start := int64(1)
integerRange.SetStart(&start) 
end := int64(1)
integerRange.SetEnd(&end) 

pageRanges := []graphmodels.IntegerRangeable {
	integerRange,
}
configuration.SetPageRanges(pageRanges)
quality := graphmodels.MEDIUM_PRINTQUALITY 
configuration.SetQuality(&quality) 
dpi := int32(600)
configuration.SetDpi(&dpi) 
orientation := graphmodels.LANDSCAPE_PRINTORIENTATION 
configuration.SetOrientation(&orientation) 
copies := int32(1)
configuration.SetCopies(&copies) 
duplexMode := graphmodels.ONESIDED_PRINTDUPLEXMODE 
configuration.SetDuplexMode(&duplexMode) 
colorMode := graphmodels.BLACKANDWHITE_PRINTCOLORMODE 
configuration.SetColorMode(&colorMode) 
inputBin := "by-pass-tray"
configuration.SetInputBin(&inputBin) 
outputBin := "output-tray"
configuration.SetOutputBin(&outputBin) 
mediaSize := "A4"
configuration.SetMediaSize(&mediaSize) 
margin := graphmodels.NewPrintMargin()
top := int32(0)
margin.SetTop(&top) 
bottom := int32(0)
margin.SetBottom(&bottom) 
left := int32(0)
margin.SetLeft(&left) 
right := int32(0)
margin.SetRight(&right) 
configuration.SetMargin(margin)
mediaType := "stationery"
configuration.SetMediaType(&mediaType) 
finishings := null
configuration.SetFinishings(&finishings) 
pagesPerSheet := int32(1)
configuration.SetPagesPerSheet(&pagesPerSheet) 
multipageLayout := graphmodels.CLOCKWISEFROMBOTTOMLEFT_PRINTMULTIPAGELAYOUT 
configuration.SetMultipageLayout(&multipageLayout) 
collate := false
configuration.SetCollate(&collate) 
scaling := graphmodels.SHRINKTOFIT_PRINTSCALING 
configuration.SetScaling(&scaling) 
fitPdfToPage := false
configuration.SetFitPdfToPage(&fitPdfToPage) 
requestBody.SetConfiguration(configuration)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
jobs, err := graphClient.Print().Printers().ByPrinterId("printer-id").Jobs().Post(context.Background(), requestBody, nil)


```