---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473271"
---
# <span data-ttu-id="43041-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="43041-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="43041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43041-102">SYNOPSIS</span></span>
<span data-ttu-id="43041-103">Abrechnungskonten erhalten.</span><span class="sxs-lookup"><span data-stu-id="43041-103">Get billing accounts.</span></span>

## <span data-ttu-id="43041-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43041-104">SYNTAX</span></span>

### <span data-ttu-id="43041-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="43041-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43041-106">Single</span><span class="sxs-lookup"><span data-stu-id="43041-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43041-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43041-107">DESCRIPTION</span></span>
<span data-ttu-id="43041-108">Das **Get-AzBillingAccount-Cmdlet** erhält Abrechnungskonten, auf die der Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="43041-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="43041-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43041-109">EXAMPLES</span></span>

### <span data-ttu-id="43041-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43041-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="43041-111">Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="43041-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="43041-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="43041-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="43041-113">Holen Sie sich das Abrechnungskonto mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="43041-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="43041-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="43041-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="43041-115">Holen Sie sich alle Abrechnungskonten, auf die der Benutzer Zugriff hat, und geben Sie die Adresse in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="43041-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="43041-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="43041-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="43041-117">Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und schließen Sie die Abrechnungsprofile in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="43041-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="43041-118">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="43041-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="43041-119">Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und schließen Sie die Abrechnungsprofile und Rechnungsabschnitte darunter in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="43041-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="43041-120">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="43041-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="43041-121">Holen Sie sich das Abrechnungskonto mit dem angegebenen Namen, und fügen Sie die Adresse, die Abrechnungsprofile und die Rechnungsabschnitte darunter in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="43041-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="43041-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43041-122">PARAMETERS</span></span>

### <span data-ttu-id="43041-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43041-123">-DefaultProfile</span></span>
<span data-ttu-id="43041-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="43041-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43041-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="43041-125">-IncludeAddress</span></span>
<span data-ttu-id="43041-126">Geben Sie die Adresse des Abrechnungskontos an.</span><span class="sxs-lookup"><span data-stu-id="43041-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="43041-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="43041-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="43041-128">Schließen Sie die Abrechnungsprofile unter dem Abrechnungskonto ein.</span><span class="sxs-lookup"><span data-stu-id="43041-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="43041-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="43041-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="43041-130">Fügen Sie die Abrechnungsprofile unter den Abschnitten "Abrechnungskonto" und "Rechnungen" darunter ein.</span><span class="sxs-lookup"><span data-stu-id="43041-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="43041-131">-Name</span><span class="sxs-lookup"><span data-stu-id="43041-131">-Name</span></span>
<span data-ttu-id="43041-132">Der Name eines bestimmten Abrechnungskontos.</span><span class="sxs-lookup"><span data-stu-id="43041-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="43041-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="43041-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="43041-134">Listen Sie die Abrechnungsentitäten unter "Abrechnungskonto" auf, die als Eingabe zum Erstellen eines Abonnements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="43041-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="43041-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43041-135">CommonParameters</span></span>
<span data-ttu-id="43041-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43041-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43041-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43041-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43041-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43041-138">INPUTS</span></span>

### <span data-ttu-id="43041-139">Keine</span><span class="sxs-lookup"><span data-stu-id="43041-139">None</span></span>

## <span data-ttu-id="43041-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43041-140">OUTPUTS</span></span>

### <span data-ttu-id="43041-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="43041-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="43041-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="43041-142">NOTES</span></span>

## <span data-ttu-id="43041-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="43041-143">RELATED LINKS</span></span>
