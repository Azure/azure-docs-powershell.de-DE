---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005308"
---
# <span data-ttu-id="588ec-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="588ec-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="588ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="588ec-102">SYNOPSIS</span></span>
<span data-ttu-id="588ec-103">Erstellen oder aktualisieren Sie die Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="588ec-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="588ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="588ec-104">SYNTAX</span></span>

### <span data-ttu-id="588ec-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="588ec-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="588ec-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="588ec-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="588ec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="588ec-107">DESCRIPTION</span></span>
<span data-ttu-id="588ec-108">Erstellen oder aktualisieren Sie die Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="588ec-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="588ec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="588ec-109">EXAMPLES</span></span>

### <span data-ttu-id="588ec-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="588ec-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="588ec-111">Aktualisiert die Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="588ec-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="588ec-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="588ec-112">PARAMETERS</span></span>

### <span data-ttu-id="588ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588ec-113">-DefaultProfile</span></span>
<span data-ttu-id="588ec-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="588ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="588ec-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="588ec-115">-Location</span></span>
<span data-ttu-id="588ec-116">Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="588ec-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="588ec-117">-Name</span><span class="sxs-lookup"><span data-stu-id="588ec-117">-Name</span></span>
<span data-ttu-id="588ec-118">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="588ec-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="588ec-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="588ec-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="588ec-120">Delegation anbieten.</span><span class="sxs-lookup"><span data-stu-id="588ec-120">Offer delegation.</span></span>
<span data-ttu-id="588ec-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für OFFERDELEGATIONDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="588ec-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="588ec-122">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="588ec-122">-OfferName</span></span>
<span data-ttu-id="588ec-123">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="588ec-123">Name of an offer.</span></span>

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

### <span data-ttu-id="588ec-124">-PropertiesSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="588ec-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="588ec-125">Der Bezeichner des Abonnements, das das Delegierte Angebot erhält.</span><span class="sxs-lookup"><span data-stu-id="588ec-125">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="588ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="588ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="588ec-127">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="588ec-127">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="588ec-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="588ec-128">-SubscriptionId</span></span>
<span data-ttu-id="588ec-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="588ec-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="588ec-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="588ec-130">-Confirm</span></span>
<span data-ttu-id="588ec-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="588ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="588ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="588ec-132">-WhatIf</span></span>
<span data-ttu-id="588ec-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="588ec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="588ec-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="588ec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="588ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588ec-135">CommonParameters</span></span>
<span data-ttu-id="588ec-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="588ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588ec-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="588ec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588ec-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="588ec-138">INPUTS</span></span>

### <span data-ttu-id="588ec-139">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="588ec-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="588ec-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="588ec-140">OUTPUTS</span></span>

### <span data-ttu-id="588ec-141">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="588ec-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="588ec-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="588ec-142">ALIASES</span></span>

## <span data-ttu-id="588ec-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="588ec-143">NOTES</span></span>

<span data-ttu-id="588ec-144">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="588ec-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="588ec-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="588ec-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="588ec-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="588ec-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="588ec-147">`[Location <String>]`: Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="588ec-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="588ec-148">`[SubscriptionId <String>]`: Bezeichner des Abonnements, das das Delegierte Angebot erhält.</span><span class="sxs-lookup"><span data-stu-id="588ec-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="588ec-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="588ec-149">RELATED LINKS</span></span>

