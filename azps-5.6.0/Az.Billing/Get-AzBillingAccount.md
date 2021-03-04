---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922507"
---
# <span data-ttu-id="956e8-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="956e8-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="956e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="956e8-102">SYNOPSIS</span></span>
<span data-ttu-id="956e8-103">Abrechnungskonten erhalten.</span><span class="sxs-lookup"><span data-stu-id="956e8-103">Get billing accounts.</span></span>

## <span data-ttu-id="956e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="956e8-104">SYNTAX</span></span>

### <span data-ttu-id="956e8-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="956e8-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="956e8-106">Single</span><span class="sxs-lookup"><span data-stu-id="956e8-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="956e8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="956e8-107">DESCRIPTION</span></span>
<span data-ttu-id="956e8-108">Das **Get-AzBillingAccount-Cmdlet** erhält Abrechnungskonten, auf die benutzer zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="956e8-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="956e8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="956e8-109">EXAMPLES</span></span>

### <span data-ttu-id="956e8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="956e8-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="956e8-111">Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="956e8-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="956e8-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="956e8-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="956e8-113">Holen Sie sich das Abrechnungskonto mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="956e8-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="956e8-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="956e8-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="956e8-115">Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und fügen Sie die Adresse in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="956e8-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="956e8-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="956e8-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="956e8-117">Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und fügen Sie die Abrechnungsprofile in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="956e8-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="956e8-118">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="956e8-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="956e8-119">Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und fügen Sie die darunter gegliederten Abrechnungsprofile und Rechnungsabschnitte in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="956e8-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="956e8-120">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="956e8-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="956e8-121">Holen Sie sich das Abrechnungskonto mit dem angegebenen Namen, und fügen Sie die darunter gegliederten Abschnitte Adresse, Abrechnungsprofile und Rechnungen in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="956e8-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="956e8-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="956e8-122">PARAMETERS</span></span>

### <span data-ttu-id="956e8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956e8-123">-DefaultProfile</span></span>
<span data-ttu-id="956e8-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="956e8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="956e8-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="956e8-125">-IncludeAddress</span></span>
<span data-ttu-id="956e8-126">Geben Sie die Adresse des Abrechnungskontos an.</span><span class="sxs-lookup"><span data-stu-id="956e8-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="956e8-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="956e8-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="956e8-128">Fügen Sie die Abrechnungsprofile unter dem Abrechnungskonto ein.</span><span class="sxs-lookup"><span data-stu-id="956e8-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="956e8-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="956e8-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="956e8-130">Fügen Sie die Abrechnungsprofile unter abrechnungskonto und rechnungsabschnitte darunter ein.</span><span class="sxs-lookup"><span data-stu-id="956e8-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="956e8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="956e8-131">-Name</span></span>
<span data-ttu-id="956e8-132">Name eines bestimmten Abrechnungskontos.</span><span class="sxs-lookup"><span data-stu-id="956e8-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="956e8-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="956e8-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="956e8-134">Listen Sie die Abrechnungsentitäten unter Abrechnungskonto auf, die als Eingabe zum Erstellen eines Abonnements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="956e8-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956e8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956e8-135">CommonParameters</span></span>
<span data-ttu-id="956e8-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956e8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956e8-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="956e8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956e8-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="956e8-138">INPUTS</span></span>

### <span data-ttu-id="956e8-139">Keine</span><span class="sxs-lookup"><span data-stu-id="956e8-139">None</span></span>

## <span data-ttu-id="956e8-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="956e8-140">OUTPUTS</span></span>

### <span data-ttu-id="956e8-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="956e8-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="956e8-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="956e8-142">NOTES</span></span>

## <span data-ttu-id="956e8-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="956e8-143">RELATED LINKS</span></span>
