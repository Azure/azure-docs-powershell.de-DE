---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297634"
---
# <span data-ttu-id="38e2e-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="38e2e-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="38e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="38e2e-103">Abrechnungsprofile erhalten.</span><span class="sxs-lookup"><span data-stu-id="38e2e-103">Get billing profiles.</span></span>

## <span data-ttu-id="38e2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38e2e-104">SYNTAX</span></span>

### <span data-ttu-id="38e2e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="38e2e-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38e2e-106">Single</span><span class="sxs-lookup"><span data-stu-id="38e2e-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38e2e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38e2e-107">DESCRIPTION</span></span>
<span data-ttu-id="38e2e-108">Das **Get-AzBillingProfile-Cmdlet** ruft Abrechnungsprofile unter dem angegebenen Abrechnungskonto ab.</span><span class="sxs-lookup"><span data-stu-id="38e2e-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="38e2e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38e2e-109">EXAMPLES</span></span>

### <span data-ttu-id="38e2e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38e2e-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="38e2e-111">Erhalten Sie alle Abrechnungsprofile unter dem angegebenen Abrechnungskonto.</span><span class="sxs-lookup"><span data-stu-id="38e2e-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="38e2e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="38e2e-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="38e2e-113">Holen Sie sich das Abrechnungsprofil mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="38e2e-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="38e2e-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="38e2e-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="38e2e-115">Erhalten Sie alle Abrechnungsprofile unter dem angegebenen Abrechnungskonto, und schließen Sie die Rechnungsabschnitte in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="38e2e-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="38e2e-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="38e2e-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="38e2e-117">Holen Sie sich das Abrechnungsprofil mit dem angegebenen Namen, und fügen Sie die Rechnungsabschnitte in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="38e2e-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="38e2e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38e2e-118">PARAMETERS</span></span>

### <span data-ttu-id="38e2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e2e-119">-DefaultProfile</span></span>
<span data-ttu-id="38e2e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="38e2e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38e2e-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="38e2e-121">-BillingAccountName</span></span>
<span data-ttu-id="38e2e-122">Der Name des jeweiligen Abrechnungskontos.</span><span class="sxs-lookup"><span data-stu-id="38e2e-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="38e2e-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="38e2e-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="38e2e-124">Fügen Sie die Abschnitte "Rechnungen" unter "Abrechnungsprofil" ein.</span><span class="sxs-lookup"><span data-stu-id="38e2e-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="38e2e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="38e2e-125">-Name</span></span>
<span data-ttu-id="38e2e-126">Der Name eines bestimmten Abrechnungsprofils.</span><span class="sxs-lookup"><span data-stu-id="38e2e-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="38e2e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e2e-127">CommonParameters</span></span>
<span data-ttu-id="38e2e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38e2e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e2e-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38e2e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e2e-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38e2e-130">INPUTS</span></span>

### <span data-ttu-id="38e2e-131">Keine</span><span class="sxs-lookup"><span data-stu-id="38e2e-131">None</span></span>

## <span data-ttu-id="38e2e-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38e2e-132">OUTPUTS</span></span>

### <span data-ttu-id="38e2e-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="38e2e-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="38e2e-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38e2e-134">NOTES</span></span>

## <span data-ttu-id="38e2e-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38e2e-135">RELATED LINKS</span></span>
