---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178635"
---
# <span data-ttu-id="00a27-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="00a27-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="00a27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00a27-102">SYNOPSIS</span></span>
<span data-ttu-id="00a27-103">Abrechnungs Rechnungen des Abonnements abrufen.</span><span class="sxs-lookup"><span data-stu-id="00a27-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="00a27-104">Abrufen von Abrechnungs Rechnungen eines Abrechnungskontos und eines Abrechnungs Profils</span><span class="sxs-lookup"><span data-stu-id="00a27-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="00a27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00a27-105">SYNTAX</span></span>

### <span data-ttu-id="00a27-106">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="00a27-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="00a27-107">Neueste</span><span class="sxs-lookup"><span data-stu-id="00a27-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="00a27-108">Einzel</span><span class="sxs-lookup"><span data-stu-id="00a27-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00a27-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00a27-109">DESCRIPTION</span></span>
<span data-ttu-id="00a27-110">Das Cmdlet " **Get-AzBillingInvoice** " ruft Rechnungs Rechnungen des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="00a27-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="00a27-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00a27-111">EXAMPLES</span></span>

### <span data-ttu-id="00a27-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00a27-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="00a27-113">Besorgen Sie sich die aktuelle Rechnung des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="00a27-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="00a27-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="00a27-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="00a27-115">Besorgen Sie sich die Rechnung des Abonnements mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="00a27-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="00a27-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="00a27-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="00a27-117">Abrufen aller verfügbaren Rechnungen des Abonnements in umgekehrter chronologischer Reihenfolge, beginnend mit der letzten Rechnung ohne Download-URL.</span><span class="sxs-lookup"><span data-stu-id="00a27-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="00a27-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="00a27-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="00a27-119">Holen Sie sich die letzten 10 Rechnungen des Abonnements, und fügen Sie die Download-URL in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="00a27-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="00a27-120">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="00a27-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="00a27-121">Beziehen Sie die spezifische Rechnung nach Namen, und fügen Sie die Download-URL in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="00a27-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="00a27-122">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="00a27-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="00a27-123">Sie erhalten Rechnungen nach Rechnungskonto Name und fügen die Download-URL für jede Rechnung in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="00a27-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="00a27-124">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="00a27-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="00a27-125">Erhalten Sie eine bestimmte Rechnung nach Rechnungsname und Rechnungskonto Namen, und fügen Sie die Download-URL für jede Rechnung in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="00a27-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="00a27-126">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="00a27-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="00a27-127">Aktuelle Rechnung nach Rechnungskonto Namen abrufen und die Download-URL für Rechnung in das Ergebnis einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="00a27-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="00a27-128">Beispiel 9</span><span class="sxs-lookup"><span data-stu-id="00a27-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="00a27-129">Holen Sie sich die letzten 10 Rechnungen des jeweiligen Abrechnungskontos und des bestimmten Abrechnungs Profils, und fügen Sie die Download-URL in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="00a27-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="00a27-130">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="00a27-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="00a27-131">Aktuelle Rechnung nach Rechnungskonto Name und Rechnungsprofil Namen abrufen und die Download-URL für Rechnung in das Ergebnis einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="00a27-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="00a27-132">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="00a27-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="00a27-133">Sie erhalten Rechnungen nach Rechnungskonto Name und Rechnungsprofil Name für einen Abrechnungszeitraum, der durch perioStart Datum und periodEnd Datum angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="00a27-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="00a27-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="00a27-134">PARAMETERS</span></span>

### <span data-ttu-id="00a27-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a27-135">-DefaultProfile</span></span>
<span data-ttu-id="00a27-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="00a27-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00a27-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="00a27-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="00a27-138">Generieren Sie die Download-URL der Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="00a27-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="00a27-139">-Neueste</span><span class="sxs-lookup"><span data-stu-id="00a27-139">-Latest</span></span>
<span data-ttu-id="00a27-140">Besorgen Sie sich die neueste Rechnung.</span><span class="sxs-lookup"><span data-stu-id="00a27-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="00a27-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="00a27-141">-MaxCount</span></span>
<span data-ttu-id="00a27-142">Bestimmt die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00a27-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="00a27-143">-Name</span><span class="sxs-lookup"><span data-stu-id="00a27-143">-Name</span></span>
<span data-ttu-id="00a27-144">Der Name einer bestimmten Rechnung, die abgerufen werden soll, oder der letzte, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="00a27-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="00a27-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="00a27-145">-BillingAccountName</span></span>
<span data-ttu-id="00a27-146">Der Name eines bestimmten Abrechnungskontos, für das Rechnungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00a27-146">Name of a specific billing account to get invoices for.</span></span>

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

### <span data-ttu-id="00a27-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="00a27-147">-BillingProfileName</span></span>
<span data-ttu-id="00a27-148">Der Name eines bestimmten Abrechnungs Profils, für das Rechnungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00a27-148">Name of a specific billing profile to get invoices for.</span></span>

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

### <span data-ttu-id="00a27-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="00a27-149">-PeriodStartDate</span></span>
<span data-ttu-id="00a27-150">Anfangstermin für Rechnung.</span><span class="sxs-lookup"><span data-stu-id="00a27-150">Start date for invoice.</span></span>

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

### <span data-ttu-id="00a27-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="00a27-151">-PeriodEndDate</span></span>
<span data-ttu-id="00a27-152">Enddatum für Rechnung.</span><span class="sxs-lookup"><span data-stu-id="00a27-152">End date for invoice.</span></span>

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



### <span data-ttu-id="00a27-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a27-153">CommonParameters</span></span>
<span data-ttu-id="00a27-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00a27-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a27-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00a27-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a27-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00a27-156">INPUTS</span></span>

### <span data-ttu-id="00a27-157">Keine</span><span class="sxs-lookup"><span data-stu-id="00a27-157">None</span></span>

## <span data-ttu-id="00a27-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00a27-158">OUTPUTS</span></span>

### <span data-ttu-id="00a27-159">Microsoft. Azure. Commands. Billing. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="00a27-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="00a27-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="00a27-160">NOTES</span></span>

## <span data-ttu-id="00a27-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00a27-161">RELATED LINKS</span></span>
