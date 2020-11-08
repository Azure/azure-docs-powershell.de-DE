---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplan
schema: 2.0.0
ms.openlocfilehash: fca0ab39b587bea05228da3a053fd1575b3e7e98
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007134"
---
# <span data-ttu-id="20b50-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="20b50-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="20b50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20b50-102">SYNOPSIS</span></span>
<span data-ttu-id="20b50-103">Löschen Sie den angegebenen Plan.</span><span class="sxs-lookup"><span data-stu-id="20b50-103">Delete the specified plan.</span></span>

## <span data-ttu-id="20b50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20b50-104">SYNTAX</span></span>

### <span data-ttu-id="20b50-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="20b50-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20b50-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20b50-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20b50-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20b50-107">DESCRIPTION</span></span>
<span data-ttu-id="20b50-108">Löschen Sie den angegebenen Plan.</span><span class="sxs-lookup"><span data-stu-id="20b50-108">Delete the specified plan.</span></span>

## <span data-ttu-id="20b50-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20b50-109">EXAMPLES</span></span>

### <span data-ttu-id="20b50-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20b50-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

```

<span data-ttu-id="20b50-111">Löschen des angegebenen Plans</span><span class="sxs-lookup"><span data-stu-id="20b50-111">Delete the specified plan</span></span>

## <span data-ttu-id="20b50-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="20b50-112">PARAMETERS</span></span>

### <span data-ttu-id="20b50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b50-113">-DefaultProfile</span></span>
<span data-ttu-id="20b50-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20b50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b50-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="20b50-115">-InputObject</span></span>
<span data-ttu-id="20b50-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="20b50-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20b50-117">-Name</span><span class="sxs-lookup"><span data-stu-id="20b50-117">-Name</span></span>
<span data-ttu-id="20b50-118">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="20b50-118">Name of the plan.</span></span>

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

### <span data-ttu-id="20b50-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20b50-119">-PassThru</span></span>
<span data-ttu-id="20b50-120">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="20b50-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="20b50-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b50-121">-ResourceGroupName</span></span>
<span data-ttu-id="20b50-122">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="20b50-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="20b50-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="20b50-123">-SubscriptionId</span></span>
<span data-ttu-id="20b50-124">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="20b50-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="20b50-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20b50-125">-Confirm</span></span>
<span data-ttu-id="20b50-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20b50-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b50-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b50-127">-WhatIf</span></span>
<span data-ttu-id="20b50-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20b50-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b50-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20b50-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b50-130">CommonParameters</span></span>
<span data-ttu-id="20b50-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b50-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20b50-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b50-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20b50-133">INPUTS</span></span>

### <span data-ttu-id="20b50-134">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="20b50-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="20b50-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20b50-135">OUTPUTS</span></span>

### <span data-ttu-id="20b50-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20b50-136">System.Boolean</span></span>

<span data-ttu-id="20b50-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="20b50-137">ALIASES</span></span>

## <span data-ttu-id="20b50-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="20b50-138">NOTES</span></span>

<span data-ttu-id="20b50-139">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="20b50-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20b50-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="20b50-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="20b50-141">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="20b50-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20b50-142">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="20b50-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="20b50-143">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="20b50-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="20b50-144">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="20b50-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20b50-145">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="20b50-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="20b50-146">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="20b50-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="20b50-147">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="20b50-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="20b50-148">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="20b50-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="20b50-149">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="20b50-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="20b50-150">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="20b50-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="20b50-151">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="20b50-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="20b50-152">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="20b50-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="20b50-153">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="20b50-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="20b50-154">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="20b50-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="20b50-155">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="20b50-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="20b50-156">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="20b50-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="20b50-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20b50-157">RELATED LINKS</span></span>

