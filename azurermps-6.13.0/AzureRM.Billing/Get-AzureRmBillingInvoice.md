---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 1f21022294b1bcf5c75a7cf49dcc009600dc4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501194"
---
# <span data-ttu-id="bb8f3-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="bb8f3-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="bb8f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8f3-103">Abrechnungs Rechnungen des Abonnements abrufen.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb8f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb8f3-104">SYNTAX</span></span>

### <span data-ttu-id="bb8f3-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb8f3-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8f3-106">Neueste</span><span class="sxs-lookup"><span data-stu-id="bb8f3-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb8f3-107">Einzel</span><span class="sxs-lookup"><span data-stu-id="bb8f3-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb8f3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb8f3-108">DESCRIPTION</span></span>
<span data-ttu-id="bb8f3-109">Das Cmdlet " **Get-AzureRmBillingInvoice** " ruft Rechnungs Rechnungen des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="bb8f3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb8f3-110">EXAMPLES</span></span>

### <span data-ttu-id="bb8f3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb8f3-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="bb8f3-112">Besorgen Sie sich die aktuelle Rechnung des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="bb8f3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bb8f3-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="bb8f3-114">Besorgen Sie sich die Rechnung des Abonnements mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="bb8f3-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bb8f3-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="bb8f3-116">Abrufen aller verfügbaren Rechnungen des Abonnements in umgekehrter chronologischer Reihenfolge, beginnend mit der letzten Rechnung ohne Download-URL.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="bb8f3-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="bb8f3-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="bb8f3-118">Holen Sie sich die letzten 10 Rechnungen des Abonnements, und fügen Sie die Download-URL in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="bb8f3-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb8f3-119">PARAMETERS</span></span>

### <span data-ttu-id="bb8f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8f3-120">-DefaultProfile</span></span>
<span data-ttu-id="bb8f3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bb8f3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f3-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="bb8f3-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="bb8f3-123">Generieren Sie die Download-URL der Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f3-124">-Neueste</span><span class="sxs-lookup"><span data-stu-id="bb8f3-124">-Latest</span></span>
<span data-ttu-id="bb8f3-125">Besorgen Sie sich die neueste Rechnung.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="bb8f3-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bb8f3-126">-MaxCount</span></span>
<span data-ttu-id="bb8f3-127">Bestimmt die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="bb8f3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bb8f3-128">-Name</span></span>
<span data-ttu-id="bb8f3-129">Der Name einer bestimmten Rechnung, die abgerufen werden soll, oder der letzte, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="bb8f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8f3-130">CommonParameters</span></span>
<span data-ttu-id="bb8f3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8f3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb8f3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8f3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb8f3-133">INPUTS</span></span>

### <span data-ttu-id="bb8f3-134">Keine</span><span class="sxs-lookup"><span data-stu-id="bb8f3-134">None</span></span>

## <span data-ttu-id="bb8f3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb8f3-135">OUTPUTS</span></span>

### <span data-ttu-id="bb8f3-136">Microsoft. Azure. Commands. Billing. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="bb8f3-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="bb8f3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb8f3-137">NOTES</span></span>

## <span data-ttu-id="bb8f3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb8f3-138">RELATED LINKS</span></span>
