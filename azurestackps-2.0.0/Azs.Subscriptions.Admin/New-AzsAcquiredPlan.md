---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005352"
---
# <span data-ttu-id="6b269-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="6b269-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="6b269-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b269-102">SYNOPSIS</span></span>


## <span data-ttu-id="6b269-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b269-103">SYNTAX</span></span>

### <span data-ttu-id="6b269-104">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b269-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6b269-105">Erstellen</span><span class="sxs-lookup"><span data-stu-id="6b269-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6b269-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b269-106">DESCRIPTION</span></span>


## <span data-ttu-id="6b269-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b269-107">EXAMPLES</span></span>

### <span data-ttu-id="6b269-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b269-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="6b269-109">Erstellen Sie einen Abonnementplan.</span><span class="sxs-lookup"><span data-stu-id="6b269-109">Create a subscription plan.</span></span>

## <span data-ttu-id="6b269-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b269-110">PARAMETERS</span></span>

### <span data-ttu-id="6b269-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="6b269-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="6b269-112">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für ACQUIREDPLANDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6b269-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6b269-113">-Erwerbszeitpunkt</span><span class="sxs-lookup"><span data-stu-id="6b269-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6b269-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b269-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="6b269-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="6b269-115">-ExternalReferenceId</span></span>


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

### <span data-ttu-id="6b269-116">-ID</span><span class="sxs-lookup"><span data-stu-id="6b269-116">-Id</span></span>


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

### <span data-ttu-id="6b269-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="6b269-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6b269-118">-Plan-Nr.</span><span class="sxs-lookup"><span data-stu-id="6b269-118">-PlanId</span></span>


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

### <span data-ttu-id="6b269-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="6b269-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6b269-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6b269-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="6b269-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b269-121">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="6b269-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b269-122">-Confirm</span></span>
<span data-ttu-id="6b269-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b269-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b269-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b269-124">-WhatIf</span></span>
<span data-ttu-id="6b269-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b269-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b269-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b269-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b269-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b269-127">CommonParameters</span></span>
<span data-ttu-id="6b269-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b269-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b269-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b269-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b269-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b269-130">INPUTS</span></span>

### <span data-ttu-id="6b269-131">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="6b269-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="6b269-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b269-132">OUTPUTS</span></span>

### <span data-ttu-id="6b269-133">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="6b269-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="6b269-134">Aliase</span><span class="sxs-lookup"><span data-stu-id="6b269-134">ALIASES</span></span>

<span data-ttu-id="6b269-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="6b269-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="6b269-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b269-136">NOTES</span></span>

<span data-ttu-id="6b269-137">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b269-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b269-138">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="6b269-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6b269-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="6b269-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="6b269-140">`[AcquisitionId <String>]`: Akquisitions-ID.</span><span class="sxs-lookup"><span data-stu-id="6b269-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="6b269-141">`[AcquisitionTime <DateTime?>]`: Erwerbszeit.</span><span class="sxs-lookup"><span data-stu-id="6b269-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="6b269-142">`[ExternalReferenceId <String>]`: Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6b269-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="6b269-143">`[Id <String>]`: Bezeichner im Kontext des Mandanten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="6b269-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="6b269-144">`[PlanId <String>]`: Planen Sie den Bezeichner im Mandanten Abonnement Kontext.</span><span class="sxs-lookup"><span data-stu-id="6b269-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="6b269-145">`[ProvisioningState <ProvisioningState?>]`: Zustand der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6b269-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="6b269-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b269-146">RELATED LINKS</span></span>

