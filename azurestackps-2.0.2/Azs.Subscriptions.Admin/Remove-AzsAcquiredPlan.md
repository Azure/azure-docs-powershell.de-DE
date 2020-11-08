---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007286"
---
# <span data-ttu-id="e3076-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="e3076-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="e3076-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3076-102">SYNOPSIS</span></span>
<span data-ttu-id="e3076-103">Löscht einen erworbenen Plan.</span><span class="sxs-lookup"><span data-stu-id="e3076-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="e3076-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3076-104">SYNTAX</span></span>

### <span data-ttu-id="e3076-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3076-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e3076-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3076-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3076-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3076-107">DESCRIPTION</span></span>
<span data-ttu-id="e3076-108">Löscht einen erworbenen Plan.</span><span class="sxs-lookup"><span data-stu-id="e3076-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="e3076-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3076-109">EXAMPLES</span></span>

### <span data-ttu-id="e3076-110">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="e3076-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="e3076-111">Löschen eines erworbenen Plans</span><span class="sxs-lookup"><span data-stu-id="e3076-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="e3076-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3076-112">PARAMETERS</span></span>

### <span data-ttu-id="e3076-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3076-113">-DefaultProfile</span></span>
<span data-ttu-id="e3076-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3076-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3076-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e3076-115">-InputObject</span></span>
<span data-ttu-id="e3076-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e3076-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3076-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3076-117">-PassThru</span></span>
<span data-ttu-id="e3076-118">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="e3076-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e3076-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="e3076-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="e3076-120">Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e3076-120">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="e3076-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e3076-121">-SubscriptionId</span></span>
<span data-ttu-id="e3076-122">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e3076-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e3076-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3076-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="e3076-124">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e3076-124">The target subscription ID.</span></span>

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

### <span data-ttu-id="e3076-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3076-125">-Confirm</span></span>
<span data-ttu-id="e3076-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3076-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3076-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3076-127">-WhatIf</span></span>
<span data-ttu-id="e3076-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3076-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3076-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3076-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3076-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3076-130">CommonParameters</span></span>
<span data-ttu-id="e3076-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3076-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3076-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3076-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3076-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3076-133">INPUTS</span></span>

### <span data-ttu-id="e3076-134">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e3076-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e3076-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3076-135">OUTPUTS</span></span>

### <span data-ttu-id="e3076-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3076-136">System.Boolean</span></span>

<span data-ttu-id="e3076-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="e3076-137">ALIASES</span></span>

### <span data-ttu-id="e3076-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="e3076-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="e3076-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3076-139">NOTES</span></span>

<span data-ttu-id="e3076-140">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e3076-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3076-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e3076-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e3076-142">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e3076-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3076-143">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e3076-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e3076-144">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="e3076-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e3076-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e3076-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3076-146">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="e3076-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e3076-147">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="e3076-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e3076-148">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="e3076-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e3076-149">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="e3076-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e3076-150">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="e3076-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e3076-151">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="e3076-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e3076-152">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e3076-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e3076-153">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="e3076-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e3076-154">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="e3076-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e3076-155">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e3076-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e3076-156">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e3076-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e3076-157">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="e3076-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e3076-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3076-158">RELATED LINKS</span></span>

