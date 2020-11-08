---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 8a3797006bb5006b1b4e715b45c5e12763c49f32
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007349"
---
# <span data-ttu-id="c1aa4-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c1aa4-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="c1aa4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="c1aa4-103">Erstellen oder aktualisieren Sie die Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="c1aa4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1aa4-104">SYNTAX</span></span>

### <span data-ttu-id="c1aa4-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1aa4-105">CreateExpanded (Default)</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-TargetSubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1aa4-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="c1aa4-106">Create</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1aa4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1aa4-107">DESCRIPTION</span></span>
<span data-ttu-id="c1aa4-108">Erstellen oder aktualisieren Sie die Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="c1aa4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1aa4-109">EXAMPLES</span></span>

### <span data-ttu-id="c1aa4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1aa4-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOfferDelegation -Name "testofferdelegation" -OfferName "testoffer" -ResourceGroupName "testrg" -TargetSubscriptionId "dbc27112-f67a-4690-ba12-730f71cba018"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer/offerDelegations/testofferdel
                 egation
Location       : redmond
Name           : testoffer/testofferdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cba018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="c1aa4-111">Erstellen Sie eine neue Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-111">Create a new offer delegation.</span></span>

## <span data-ttu-id="c1aa4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1aa4-112">PARAMETERS</span></span>

### <span data-ttu-id="c1aa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1aa4-113">-DefaultProfile</span></span>
<span data-ttu-id="c1aa4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1aa4-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="c1aa4-115">-Location</span></span>
<span data-ttu-id="c1aa4-116">Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="c1aa4-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1aa4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c1aa4-117">-Name</span></span>
<span data-ttu-id="c1aa4-118">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="c1aa4-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="c1aa4-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="c1aa4-120">Delegation anbieten.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-120">Offer delegation.</span></span>
<span data-ttu-id="c1aa4-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für OFFERDELEGATIONDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c1aa4-122">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="c1aa4-122">-OfferName</span></span>
<span data-ttu-id="c1aa4-123">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-123">Name of an offer.</span></span>

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

### <span data-ttu-id="c1aa4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1aa4-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1aa4-125">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-125">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c1aa4-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c1aa4-126">-SubscriptionId</span></span>
<span data-ttu-id="c1aa4-127">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1aa4-128">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1aa4-128">-TargetSubscriptionId</span></span>
<span data-ttu-id="c1aa4-129">Der Bezeichner des Abonnements, das das Delegierte Angebot erhält.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-129">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1aa4-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1aa4-130">-Confirm</span></span>
<span data-ttu-id="c1aa4-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1aa4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1aa4-132">-WhatIf</span></span>
<span data-ttu-id="c1aa4-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1aa4-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1aa4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1aa4-135">CommonParameters</span></span>
<span data-ttu-id="c1aa4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1aa4-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1aa4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1aa4-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1aa4-138">INPUTS</span></span>

### <span data-ttu-id="c1aa4-139">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c1aa4-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="c1aa4-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1aa4-140">OUTPUTS</span></span>

### <span data-ttu-id="c1aa4-141">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c1aa4-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="c1aa4-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="c1aa4-142">ALIASES</span></span>

## <span data-ttu-id="c1aa4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1aa4-143">NOTES</span></span>

<span data-ttu-id="c1aa4-144">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1aa4-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c1aa4-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="c1aa4-147">`[Location <String>]`: Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="c1aa4-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="c1aa4-148">`[SubscriptionId <String>]`: Bezeichner des Abonnements, das das Delegierte Angebot erhält.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="c1aa4-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1aa4-149">RELATED LINKS</span></span>

