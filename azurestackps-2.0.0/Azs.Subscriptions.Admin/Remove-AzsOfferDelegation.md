---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: e9de73f68501071bceb87c115c2c9882fc5ea988
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005321"
---
# <span data-ttu-id="336dc-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="336dc-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="336dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="336dc-102">SYNOPSIS</span></span>
<span data-ttu-id="336dc-103">Löschen der angegebenen Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="336dc-103">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="336dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="336dc-104">SYNTAX</span></span>

### <span data-ttu-id="336dc-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="336dc-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="336dc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="336dc-106">DeleteViaIdentity</span></span>
```
Remove-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="336dc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="336dc-107">DESCRIPTION</span></span>
<span data-ttu-id="336dc-108">Löschen der angegebenen Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="336dc-108">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="336dc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="336dc-109">EXAMPLES</span></span>

### <span data-ttu-id="336dc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="336dc-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1

{{ Add output here }}
```

<span data-ttu-id="336dc-111">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="336dc-111">Removes the offer delegation</span></span>

## <span data-ttu-id="336dc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="336dc-112">PARAMETERS</span></span>

### <span data-ttu-id="336dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336dc-113">-DefaultProfile</span></span>
<span data-ttu-id="336dc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="336dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="336dc-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="336dc-115">-InputObject</span></span>
<span data-ttu-id="336dc-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="336dc-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="336dc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="336dc-117">-Name</span></span>
<span data-ttu-id="336dc-118">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="336dc-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="336dc-119">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="336dc-119">-OfferName</span></span>
<span data-ttu-id="336dc-120">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="336dc-120">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="336dc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="336dc-121">-PassThru</span></span>
<span data-ttu-id="336dc-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="336dc-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="336dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="336dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="336dc-124">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="336dc-124">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="336dc-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="336dc-125">-SubscriptionId</span></span>
<span data-ttu-id="336dc-126">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="336dc-126">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="336dc-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="336dc-127">-Confirm</span></span>
<span data-ttu-id="336dc-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="336dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="336dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="336dc-129">-WhatIf</span></span>
<span data-ttu-id="336dc-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="336dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="336dc-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="336dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="336dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336dc-132">CommonParameters</span></span>
<span data-ttu-id="336dc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="336dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336dc-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="336dc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336dc-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="336dc-135">INPUTS</span></span>

### <span data-ttu-id="336dc-136">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="336dc-136">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="336dc-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="336dc-137">OUTPUTS</span></span>

### <span data-ttu-id="336dc-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="336dc-138">System.Boolean</span></span>

<span data-ttu-id="336dc-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="336dc-139">ALIASES</span></span>

## <span data-ttu-id="336dc-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="336dc-140">NOTES</span></span>

<span data-ttu-id="336dc-141">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="336dc-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="336dc-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="336dc-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="336dc-143">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="336dc-143">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="336dc-144">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="336dc-144">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="336dc-145">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="336dc-145">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="336dc-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="336dc-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="336dc-147">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="336dc-147">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="336dc-148">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="336dc-148">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="336dc-149">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="336dc-149">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="336dc-150">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="336dc-150">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="336dc-151">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="336dc-151">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="336dc-152">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="336dc-152">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="336dc-153">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="336dc-153">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="336dc-154">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="336dc-154">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="336dc-155">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="336dc-155">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="336dc-156">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="336dc-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="336dc-157">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="336dc-157">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="336dc-158">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="336dc-158">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="336dc-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="336dc-159">RELATED LINKS</span></span>

