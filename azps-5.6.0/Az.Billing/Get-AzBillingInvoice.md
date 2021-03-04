---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 604109a80171ff4bb294dc1643081cd8e933d728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922491"
---
# <span data-ttu-id="d5256-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="d5256-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="d5256-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5256-102">SYNOPSIS</span></span>
<span data-ttu-id="d5256-103">Abrechnungsrechnungen des Abonnements erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5256-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="d5256-104">Abrechnungsrechnungen eines Abrechnungskontos und Eines Abrechnungsprofils erhalten</span><span class="sxs-lookup"><span data-stu-id="d5256-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="d5256-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5256-105">SYNTAX</span></span>

### <span data-ttu-id="d5256-106">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5256-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="d5256-107">Neueste Version</span><span class="sxs-lookup"><span data-stu-id="d5256-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="d5256-108">Single</span><span class="sxs-lookup"><span data-stu-id="d5256-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5256-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5256-109">DESCRIPTION</span></span>
<span data-ttu-id="d5256-110">Das **Get-AzBillingInvoice-Cmdlet** erhält Abrechnungsrechnungen des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="d5256-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="d5256-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5256-111">EXAMPLES</span></span>

### <span data-ttu-id="d5256-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5256-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="d5256-113">Erhalten Sie die neueste Rechnung des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="d5256-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="d5256-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5256-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="d5256-115">Erhalten Sie die Rechnung des Abonnements mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="d5256-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="d5256-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d5256-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="d5256-117">Holen Sie sich alle verfügbaren Rechnungen des Abonnements in umgekehrter chronologischer Reihenfolge ab der neuesten Rechnung ohne Download-URL.</span><span class="sxs-lookup"><span data-stu-id="d5256-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="d5256-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d5256-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="d5256-119">Holen Sie sich die letzten 10 Rechnungen des Abonnements, und fügen Sie die Download-URL in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="d5256-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="d5256-120">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="d5256-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="d5256-121">Holen Sie sich die spezifische Rechnung nach Name, und fügen Sie die Download-URL in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="d5256-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="d5256-122">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="d5256-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="d5256-123">Holen Sie sich Rechnungen über den Namen des Abrechnungskontos, und fügen Sie die Download-URL für jede Rechnung in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="d5256-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="d5256-124">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="d5256-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="d5256-125">Erhalten Sie eine bestimmte Rechnung nach Rechnungsname und Rechnungskontoname, und fügen Sie die Download-URL für jede Rechnung in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="d5256-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="d5256-126">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="d5256-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="d5256-127">Holen Sie sich den Namen des aktuellen Rechnungskontos, und fügen Sie die Download-URL für rechnung in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="d5256-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="d5256-128">Beispiel 9</span><span class="sxs-lookup"><span data-stu-id="d5256-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="d5256-129">Holen Sie sich die neuesten 10 Rechnungen des jeweiligen Abrechnungskontos und eines bestimmten Abrechnungsprofils, und fügen Sie die Download-URL in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="d5256-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="d5256-130">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="d5256-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="d5256-131">Holen Sie sich die neueste Rechnung über den Namen des Abrechnungskontos und den Namen des Abrechnungsprofils, und fügen Sie die Download-URL für rechnung in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="d5256-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="d5256-132">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="d5256-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="d5256-133">Erhalten Sie Rechnungen nach Dem Namen des Abrechnungskontos und dem Namen des Abrechnungsprofils für einen Abrechnungszeitraum, der durch perioStart-Datum und PeriodEnd-Datum angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d5256-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="d5256-134">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d5256-134">PARAMETERS</span></span>

### <span data-ttu-id="d5256-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5256-135">-DefaultProfile</span></span>
<span data-ttu-id="d5256-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d5256-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5256-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="d5256-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="d5256-138">Generieren Sie die Download-URL der Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="d5256-138">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5256-139">-Latest</span><span class="sxs-lookup"><span data-stu-id="d5256-139">-Latest</span></span>
<span data-ttu-id="d5256-140">Erhalten Sie die neueste Rechnung.</span><span class="sxs-lookup"><span data-stu-id="d5256-140">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5256-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d5256-141">-MaxCount</span></span>
<span data-ttu-id="d5256-142">Bestimmt die maximale Anzahl von Datensätzen, die zurückzukehren sind.</span><span class="sxs-lookup"><span data-stu-id="d5256-142">Determines the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5256-143">-Name</span><span class="sxs-lookup"><span data-stu-id="d5256-143">-Name</span></span>
<span data-ttu-id="d5256-144">Name einer bestimmten Rechnung, die sie erhalten soll, oder der aktuellste, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d5256-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5256-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="d5256-145">-BillingAccountName</span></span>
<span data-ttu-id="d5256-146">Name eines bestimmten Abrechnungskontos, für das Rechnungen erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="d5256-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5256-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="d5256-147">-BillingProfileName</span></span>
<span data-ttu-id="d5256-148">Name eines bestimmten Abrechnungsprofils zum Erhalten von Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="d5256-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5256-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="d5256-149">-PeriodStartDate</span></span>
<span data-ttu-id="d5256-150">Startdatum für Rechnung.</span><span class="sxs-lookup"><span data-stu-id="d5256-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5256-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="d5256-151">-PeriodEndDate</span></span>
<span data-ttu-id="d5256-152">Enddatum für Rechnung.</span><span class="sxs-lookup"><span data-stu-id="d5256-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="d5256-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5256-153">CommonParameters</span></span>
<span data-ttu-id="d5256-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5256-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5256-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5256-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5256-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5256-156">INPUTS</span></span>

### <span data-ttu-id="d5256-157">Keine</span><span class="sxs-lookup"><span data-stu-id="d5256-157">None</span></span>

## <span data-ttu-id="d5256-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5256-158">OUTPUTS</span></span>

### <span data-ttu-id="d5256-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="d5256-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="d5256-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d5256-160">NOTES</span></span>

## <span data-ttu-id="d5256-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d5256-161">RELATED LINKS</span></span>
