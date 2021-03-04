---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 41d023abbb1eb4453b295e64d1ccfc3b146fb197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935555"
---
# <span data-ttu-id="db874-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db874-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="db874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db874-102">SYNOPSIS</span></span>
<span data-ttu-id="db874-103">Erstellt einen ASR-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="db874-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="db874-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db874-104">SYNTAX</span></span>

### <span data-ttu-id="db874-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="db874-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db874-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="db874-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db874-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="db874-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db874-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="db874-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db874-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db874-109">DESCRIPTION</span></span>
<span data-ttu-id="db874-110">Das **Cmdlet New-AzRecoveryServicesAsrRecoveryPlan** erstellt einen Azure Websitewiederherstellungsplan im Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="db874-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="db874-111">Ein Wiederherstellungsplan sammelt virtuelle Computer, die zu einer Anwendung gehören, in einer Einheit, damit sie gemeinsam wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="db874-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="db874-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db874-112">EXAMPLES</span></span>

### <span data-ttu-id="db874-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db874-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="db874-114">Startet den Erstellungsvorgang des Wiederherstellungsplans mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db874-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="db874-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="db874-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="db874-116">Startet den Erstellungsvorgang für den Wiederherstellungsplan für azure zone, um replizierte Elemente zu zonen, und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db874-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="db874-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="db874-117">PARAMETERS</span></span>

### <span data-ttu-id="db874-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="db874-118">-Azure</span></span>
<span data-ttu-id="db874-119">Der Parameter Switch gibt das Szenario für Azure zu Azure Disaster Recovery, Erstellung des Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="db874-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="db874-120">-AzureZoneToZone</span></span>
<span data-ttu-id="db874-121">Der Parameter Switch gibt an, dass das replizierte Element in azure zone to zone szenario erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="db874-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db874-122">-DefaultProfile</span></span>
<span data-ttu-id="db874-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db874-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="db874-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="db874-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="db874-125">Gibt das Failoverbereitstellungsmodell (Klassisch oder Ressourcen-Manager) der replikationsgeschützten Elemente an, die Teil dieses Wiederherstellungsplans sind.</span><span class="sxs-lookup"><span data-stu-id="db874-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-126">-Name</span><span class="sxs-lookup"><span data-stu-id="db874-126">-Name</span></span>
<span data-ttu-id="db874-127">Name des Wiederherstellungsplans.</span><span class="sxs-lookup"><span data-stu-id="db874-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-128">-Path</span><span class="sxs-lookup"><span data-stu-id="db874-128">-Path</span></span>
<span data-ttu-id="db874-129">Gibt den Pfad zur Jsondatei für die Wiederherstellungsplandefinition an.</span><span class="sxs-lookup"><span data-stu-id="db874-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="db874-130">Ein Wiederherstellungsplandefinitions-Json kann zum Erstellen des Wiederherstellungsplans verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db874-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="db874-131">-PrimaryFabric</span></span>
<span data-ttu-id="db874-132">Gibt das ASR-Fabricobjekt für die primäre ASR-Fabric der replikationsgeschützten Elemente an, die Teil dieses Wiederherstellungsplans sind.</span><span class="sxs-lookup"><span data-stu-id="db874-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="db874-133">-PrimaryZone</span></span>
<span data-ttu-id="db874-134">Gibt die primäre Verfügbarkeitszone der replikationsgeschützten Elemente an, die Teil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="db874-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="db874-135">-RecoveryFabric</span></span>
<span data-ttu-id="db874-136">Gibt das ASR-Fabricobjekt für die Wiederherstellungs-ASR-Fabric der replikationsgeschützten Elemente an, die Teil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="db874-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="db874-137">-RecoveryZone</span></span>
<span data-ttu-id="db874-138">Gibt die primäre Verfügbarkeitszone der replikationsgeschützten Elemente an, die Teil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="db874-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db874-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="db874-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="db874-140">Die Liste der replikationsgeschützten Elemente, die der ersten Gruppe des Wiederherstellungsplans hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="db874-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db874-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="db874-141">-Confirm</span></span>
<span data-ttu-id="db874-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db874-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db874-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db874-143">-WhatIf</span></span>
<span data-ttu-id="db874-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db874-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db874-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db874-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db874-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db874-146">CommonParameters</span></span>
<span data-ttu-id="db874-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db874-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db874-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db874-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db874-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db874-149">INPUTS</span></span>

### <span data-ttu-id="db874-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="db874-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="db874-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db874-151">OUTPUTS</span></span>

### <span data-ttu-id="db874-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="db874-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="db874-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="db874-153">NOTES</span></span>

## <span data-ttu-id="db874-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="db874-154">RELATED LINKS</span></span>

[<span data-ttu-id="db874-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db874-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="db874-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db874-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="db874-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db874-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


