---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005404"
---
# <span data-ttu-id="0d7cb-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="0d7cb-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="0d7cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d7cb-102">SYNOPSIS</span></span>


## <span data-ttu-id="0d7cb-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d7cb-103">SYNTAX</span></span>

### <span data-ttu-id="0d7cb-104">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d7cb-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0d7cb-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d7cb-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d7cb-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d7cb-106">DESCRIPTION</span></span>


## <span data-ttu-id="0d7cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d7cb-107">EXAMPLES</span></span>

### <span data-ttu-id="0d7cb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d7cb-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="0d7cb-109">Löschen des angegebenen Mandanten Abonnements</span><span class="sxs-lookup"><span data-stu-id="0d7cb-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="0d7cb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d7cb-110">PARAMETERS</span></span>

### <span data-ttu-id="0d7cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7cb-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="0d7cb-112">-Force</span><span class="sxs-lookup"><span data-stu-id="0d7cb-112">-Force</span></span>


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

### <span data-ttu-id="0d7cb-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d7cb-113">-InputObject</span></span>
<span data-ttu-id="0d7cb-114">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d7cb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d7cb-115">-PassThru</span></span>


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

### <span data-ttu-id="0d7cb-116">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0d7cb-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="0d7cb-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d7cb-117">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="0d7cb-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d7cb-118">-Confirm</span></span>
<span data-ttu-id="0d7cb-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d7cb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7cb-120">-WhatIf</span></span>
<span data-ttu-id="0d7cb-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d7cb-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d7cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7cb-123">CommonParameters</span></span>
<span data-ttu-id="0d7cb-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7cb-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d7cb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7cb-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d7cb-126">INPUTS</span></span>

### <span data-ttu-id="0d7cb-127">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0d7cb-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="0d7cb-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d7cb-128">OUTPUTS</span></span>

### <span data-ttu-id="0d7cb-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d7cb-129">System.Boolean</span></span>

<span data-ttu-id="0d7cb-130">Aliase</span><span class="sxs-lookup"><span data-stu-id="0d7cb-130">ALIASES</span></span>

## <span data-ttu-id="0d7cb-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d7cb-131">NOTES</span></span>

<span data-ttu-id="0d7cb-132">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d7cb-133">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0d7cb-134">Inputobject <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="0d7cb-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="0d7cb-135">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="0d7cb-136">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="0d7cb-137">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="0d7cb-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d7cb-138">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="0d7cb-139">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="0d7cb-140">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="0d7cb-141">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="0d7cb-142">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="0d7cb-143">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="0d7cb-144">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d7cb-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="0d7cb-145">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="0d7cb-146">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="0d7cb-147">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0d7cb-148">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="0d7cb-149">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="0d7cb-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d7cb-150">RELATED LINKS</span></span>

