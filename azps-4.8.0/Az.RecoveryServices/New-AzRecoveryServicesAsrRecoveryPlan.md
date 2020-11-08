---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008277"
---
# <span data-ttu-id="8cc7a-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8cc7a-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="8cc7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cc7a-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc7a-103">Erstellt einen ASR-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="8cc7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc7a-104">SYNTAX</span></span>

### <span data-ttu-id="8cc7a-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="8cc7a-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc7a-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="8cc7a-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc7a-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="8cc7a-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc7a-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="8cc7a-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc7a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cc7a-109">DESCRIPTION</span></span>
<span data-ttu-id="8cc7a-110">Das Cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** erstellt eine Azure Site Recovery, einen Wiederherstellungsplan im Speicher für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="8cc7a-111">Ein Wiederherstellungsplan sammelt virtuelle Maschinen, die zu einer Anwendung gehören, zu einer Einheit, damit diese zusammen wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="8cc7a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cc7a-112">EXAMPLES</span></span>

### <span data-ttu-id="8cc7a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cc7a-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="8cc7a-114">Startet den Wiederherstellungsplan-Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8cc7a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8cc7a-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="8cc7a-116">Startet den Wiederherstellungsplan-Erstellungsvorgang für Azure Zone, um replizierte Elemente zu Zonen und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8cc7a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cc7a-117">PARAMETERS</span></span>

### <span data-ttu-id="8cc7a-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="8cc7a-118">-Azure</span></span>
<span data-ttu-id="8cc7a-119">Parameter Switch gibt das Szenario für Azure to Azure Disaster Recovery, Recovery Plan Creation an.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="8cc7a-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="8cc7a-120">-AzureZoneToZone</span></span>
<span data-ttu-id="8cc7a-121">Parameter Switch gibt an, dass das replizierte Element im Azure Zone to Zone-Szenario erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="8cc7a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc7a-122">-DefaultProfile</span></span>
<span data-ttu-id="8cc7a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8cc7a-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="8cc7a-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="8cc7a-125">Gibt das Failover-Bereitstellungsmodell (klassisch oder Ressourcen-Manager) der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sind.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="8cc7a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8cc7a-126">-Name</span></span>
<span data-ttu-id="8cc7a-127">Name des Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="8cc7a-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="8cc7a-128">-Path</span><span class="sxs-lookup"><span data-stu-id="8cc7a-128">-Path</span></span>
<span data-ttu-id="8cc7a-129">Gibt den Pfad zur Definitions-JSON-Datei für den Wiederherstellungsplan an.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="8cc7a-130">Eine Wiederherstellungsplan-Definition JSON kann verwendet werden, um den Wiederherstellungsplan zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="8cc7a-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="8cc7a-131">-PrimaryFabric</span></span>
<span data-ttu-id="8cc7a-132">Gibt das ASR-Fabric-Objekt für die primäre ASR-Struktur der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="8cc7a-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="8cc7a-133">-PrimaryZone</span></span>
<span data-ttu-id="8cc7a-134">Gibt die primäre Verfügbarkeit Zone der Replikations geschützten Elemente an, die Teil dieses Wiederherstellungsplans sind.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="8cc7a-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="8cc7a-135">-RecoveryFabric</span></span>
<span data-ttu-id="8cc7a-136">Gibt das ASR-Fabric-Objekt für die Wiederherstellungs-ASR-Struktur der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="8cc7a-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="8cc7a-137">-RecoveryZone</span></span>
<span data-ttu-id="8cc7a-138">Gibt die primäre Verfügbarkeit Zone der Replikations geschützten Elemente an, die Teil dieses Wiederherstellungsplans sind.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="8cc7a-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8cc7a-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8cc7a-140">Die Liste der durch die Replikation geschützten Elemente, die der ersten Gruppe des Wiederherstellungsplans hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="8cc7a-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cc7a-141">-Confirm</span></span>
<span data-ttu-id="8cc7a-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc7a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc7a-143">-WhatIf</span></span>
<span data-ttu-id="8cc7a-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cc7a-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc7a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc7a-146">CommonParameters</span></span>
<span data-ttu-id="8cc7a-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc7a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc7a-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cc7a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc7a-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cc7a-149">INPUTS</span></span>

### <span data-ttu-id="8cc7a-150">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="8cc7a-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="8cc7a-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cc7a-151">OUTPUTS</span></span>

### <span data-ttu-id="8cc7a-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8cc7a-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8cc7a-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cc7a-153">NOTES</span></span>

## <span data-ttu-id="8cc7a-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cc7a-154">RELATED LINKS</span></span>

[<span data-ttu-id="8cc7a-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8cc7a-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8cc7a-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8cc7a-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8cc7a-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8cc7a-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


