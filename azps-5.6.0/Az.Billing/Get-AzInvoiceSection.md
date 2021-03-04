---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: 6bf0b5a25772d430695737d70ff68cae5c5aa0d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949611"
---
# <span data-ttu-id="cdba3-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="cdba3-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="cdba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdba3-102">SYNOPSIS</span></span>
<span data-ttu-id="cdba3-103">Rechnungsabschnitte erhalten.</span><span class="sxs-lookup"><span data-stu-id="cdba3-103">Get invoice sections.</span></span>

## <span data-ttu-id="cdba3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdba3-104">SYNTAX</span></span>

### <span data-ttu-id="cdba3-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="cdba3-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdba3-106">Single</span><span class="sxs-lookup"><span data-stu-id="cdba3-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdba3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cdba3-107">DESCRIPTION</span></span>
<span data-ttu-id="cdba3-108">Das **Cmdlet Get-AzInvoiceSection** ruft Rechnungsabschnitte unter dem angegebenen Abrechnungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="cdba3-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="cdba3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cdba3-109">EXAMPLES</span></span>

### <span data-ttu-id="cdba3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cdba3-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="cdba3-111">Holen Sie sich alle Rechnungsabschnitte unter dem angegebenen Abrechnungsprofil.</span><span class="sxs-lookup"><span data-stu-id="cdba3-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="cdba3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cdba3-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="cdba3-113">Holen Sie sich den Rechnungsabschnitt mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="cdba3-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="cdba3-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cdba3-114">PARAMETERS</span></span>

### <span data-ttu-id="cdba3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdba3-115">-DefaultProfile</span></span>
<span data-ttu-id="cdba3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cdba3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdba3-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="cdba3-117">-BillingAccountName</span></span>
<span data-ttu-id="cdba3-118">Name des jeweiligen Abrechnungskontos.</span><span class="sxs-lookup"><span data-stu-id="cdba3-118">Name of the specific billing account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdba3-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="cdba3-119">-BillingProfileName</span></span>
<span data-ttu-id="cdba3-120">Name des jeweiligen Abrechnungsprofils.</span><span class="sxs-lookup"><span data-stu-id="cdba3-120">Name of the specific billing profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdba3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cdba3-121">-Name</span></span>
<span data-ttu-id="cdba3-122">Name eines bestimmten Rechnungsabschnitts.</span><span class="sxs-lookup"><span data-stu-id="cdba3-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="cdba3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdba3-123">CommonParameters</span></span>
<span data-ttu-id="cdba3-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdba3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdba3-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdba3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdba3-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cdba3-126">INPUTS</span></span>

### <span data-ttu-id="cdba3-127">Keine</span><span class="sxs-lookup"><span data-stu-id="cdba3-127">None</span></span>

## <span data-ttu-id="cdba3-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cdba3-128">OUTPUTS</span></span>

### <span data-ttu-id="cdba3-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="cdba3-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="cdba3-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cdba3-130">NOTES</span></span>

## <span data-ttu-id="cdba3-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cdba3-131">RELATED LINKS</span></span>
