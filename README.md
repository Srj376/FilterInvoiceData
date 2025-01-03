# FilterInvoiceData

in_InvoiceData.AsEnumerable.Where(
Function(row) row("Total").ToString().Contains("USD")
AndAlso Not row("Date").ToString.Contains("0000")
AndAlso DateTime.ParseExact(row("Date").ToString(), "yyyy-MM-dd", System.Globalization.CultureInfo.InvariantCulture) < DateTime.ParseExact(given_DateStr, "yyyy-MM-dd", System.Globalization.CultureInfo.InvariantCulture)
).CopyToDataTable


https://www.tutlane.com/tutorial/linq/linq-syntax-query-syntax-method-syntax
