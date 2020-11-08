---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 851f9d52b3247fed0755b4567e3c463b1202c34b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004894"
---
# <span data-ttu-id="77c91-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77c91-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="77c91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77c91-102">SYNOPSIS</span></span>
<span data-ttu-id="77c91-103">Erstellt einen ASR-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="77c91-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="77c91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77c91-104">SYNTAX</span></span>

### <span data-ttu-id="77c91-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="77c91-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77c91-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="77c91-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77c91-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="77c91-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77c91-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77c91-108">DESCRIPTION</span></span>
<span data-ttu-id="77c91-109">Das Cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** erstellt eine Azure Site Recovery, einen Wiederherstellungsplan im Speicher für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="77c91-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="77c91-110">Ein Wiederherstellungsplan sammelt virtuelle Maschinen, die zu einer Anwendung gehören, zu einer Einheit, damit diese zusammen wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="77c91-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="77c91-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77c91-111">EXAMPLES</span></span>

### <span data-ttu-id="77c91-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77c91-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="77c91-113">Startet den Wiederherstellungsplan-Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77c91-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="77c91-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="77c91-114">PARAMETERS</span></span>

### <span data-ttu-id="77c91-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="77c91-115">-Azure</span></span>
<span data-ttu-id="77c91-116">Parameter Switch gibt das Szenario für Azure to Azure Disaster Recovery, Recovery Plan Creation an.</span><span class="sxs-lookup"><span data-stu-id="77c91-116">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="77c91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c91-117">-DefaultProfile</span></span>
<span data-ttu-id="77c91-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77c91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="77c91-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="77c91-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="77c91-120">Gibt das Failover-Bereitstellungsmodell (klassisch oder Ressourcen-Manager) der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sind.</span><span class="sxs-lookup"><span data-stu-id="77c91-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="77c91-121">-Name</span><span class="sxs-lookup"><span data-stu-id="77c91-121">-Name</span></span>
<span data-ttu-id="77c91-122">Name des Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="77c91-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c91-123">-Path</span><span class="sxs-lookup"><span data-stu-id="77c91-123">-Path</span></span>
<span data-ttu-id="77c91-124">Gibt den Pfad zur Definitions-JSON-Datei für den Wiederherstellungsplan an.</span><span class="sxs-lookup"><span data-stu-id="77c91-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="77c91-125">Eine Wiederherstellungsplan-Definition JSON kann verwendet werden, um den Wiederherstellungsplan zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77c91-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="77c91-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="77c91-126">-PrimaryFabric</span></span>
<span data-ttu-id="77c91-127">Gibt das ASR-Fabric-Objekt für die primäre ASR-Struktur der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="77c91-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c91-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="77c91-128">-RecoveryFabric</span></span>
<span data-ttu-id="77c91-129">Gibt das ASR-Fabric-Objekt für die Wiederherstellungs-ASR-Struktur der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="77c91-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="77c91-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77c91-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="77c91-131">Die Liste der durch die Replikation geschützten Elemente, die der ersten Gruppe des Wiederherstellungsplans hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77c91-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="77c91-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77c91-132">-Confirm</span></span>
<span data-ttu-id="77c91-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77c91-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77c91-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77c91-134">-WhatIf</span></span>
<span data-ttu-id="77c91-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77c91-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77c91-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77c91-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77c91-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c91-137">CommonParameters</span></span>
<span data-ttu-id="77c91-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77c91-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c91-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77c91-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c91-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77c91-140">INPUTS</span></span>

### <span data-ttu-id="77c91-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="77c91-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="77c91-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77c91-142">OUTPUTS</span></span>

### <span data-ttu-id="77c91-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="77c91-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="77c91-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="77c91-144">NOTES</span></span>

## <span data-ttu-id="77c91-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77c91-145">RELATED LINKS</span></span>

[<span data-ttu-id="77c91-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77c91-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="77c91-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77c91-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="77c91-148">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77c91-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


