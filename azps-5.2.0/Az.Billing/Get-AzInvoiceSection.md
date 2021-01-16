---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295619"
---
# <span data-ttu-id="91869-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="91869-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="91869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91869-102">SYNOPSIS</span></span>
<span data-ttu-id="91869-103">Sie erhalten Rechnungsabschnitte.</span><span class="sxs-lookup"><span data-stu-id="91869-103">Get invoice sections.</span></span>

## <span data-ttu-id="91869-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91869-104">SYNTAX</span></span>

### <span data-ttu-id="91869-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="91869-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91869-106">Single</span><span class="sxs-lookup"><span data-stu-id="91869-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91869-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91869-107">DESCRIPTION</span></span>
<span data-ttu-id="91869-108">Das **Cmdlet "Get-AzInvoiceSection"** ruft Rechnungsabschnitte unter dem angegebenen Abrechnungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="91869-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="91869-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91869-109">EXAMPLES</span></span>

### <span data-ttu-id="91869-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91869-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="91869-111">Hier finden Sie alle Rechnungsabschnitte unter dem angegebenen Abrechnungsprofil.</span><span class="sxs-lookup"><span data-stu-id="91869-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="91869-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="91869-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="91869-113">Holen Sie sich den Rechnungsabschnitt mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="91869-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="91869-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91869-114">PARAMETERS</span></span>

### <span data-ttu-id="91869-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91869-115">-DefaultProfile</span></span>
<span data-ttu-id="91869-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="91869-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91869-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="91869-117">-BillingAccountName</span></span>
<span data-ttu-id="91869-118">Der Name des jeweiligen Abrechnungskontos.</span><span class="sxs-lookup"><span data-stu-id="91869-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="91869-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="91869-119">-BillingProfileName</span></span>
<span data-ttu-id="91869-120">Name des jeweiligen Abrechnungsprofils.</span><span class="sxs-lookup"><span data-stu-id="91869-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="91869-121">-Name</span><span class="sxs-lookup"><span data-stu-id="91869-121">-Name</span></span>
<span data-ttu-id="91869-122">Name eines bestimmten Rechnungsabschnitts.</span><span class="sxs-lookup"><span data-stu-id="91869-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="91869-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91869-123">CommonParameters</span></span>
<span data-ttu-id="91869-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91869-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91869-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91869-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91869-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91869-126">INPUTS</span></span>

### <span data-ttu-id="91869-127">Keine</span><span class="sxs-lookup"><span data-stu-id="91869-127">None</span></span>

## <span data-ttu-id="91869-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91869-128">OUTPUTS</span></span>

### <span data-ttu-id="91869-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="91869-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="91869-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91869-130">NOTES</span></span>

## <span data-ttu-id="91869-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91869-131">RELATED LINKS</span></span>
