---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: e9edfb1654e623b023a075cb462fedfbd9442756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481014"
---
# <span data-ttu-id="073e3-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="073e3-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="073e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="073e3-102">SYNOPSIS</span></span>
<span data-ttu-id="073e3-103">Erstellt einen ASR-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="073e3-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="073e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="073e3-104">SYNTAX</span></span>

### <span data-ttu-id="073e3-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="073e3-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="073e3-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="073e3-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="073e3-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="073e3-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="073e3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="073e3-108">DESCRIPTION</span></span>
<span data-ttu-id="073e3-109">Das Cmdlet **New-AzureRmRecoveryServicesAsrRecoveryPlan** erstellt einen Azure Site Recovery-Wiederherstellungsplan im Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="073e3-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="073e3-110">Ein Wiederherstellungsplan sammelt virtuelle Maschinen, die zu einer Anwendung gehören, zu einer Einheit, damit diese zusammen wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="073e3-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="073e3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="073e3-111">EXAMPLES</span></span>

### <span data-ttu-id="073e3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="073e3-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="073e3-113">Startet den Wiederherstellungsplan-Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="073e3-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="073e3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="073e3-114">PARAMETERS</span></span>

### <span data-ttu-id="073e3-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="073e3-115">-Azure</span></span>
<span data-ttu-id="073e3-116">Parameter wechseln, um anzugeben, dass der Wiederherstellungsspeicherort für den Wiederherstellungsplan Azure ist.</span><span class="sxs-lookup"><span data-stu-id="073e3-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="073e3-117">-Confirm</span></span>
<span data-ttu-id="073e3-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="073e3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073e3-119">-DefaultProfile</span></span>
<span data-ttu-id="073e3-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="073e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="073e3-121">-FailoverDeploymentModel</span></span>
<span data-ttu-id="073e3-122">Gibt das Failover-Bereitstellungsmodell (klassisch oder Ressourcen-Manager) der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sind.</span><span class="sxs-lookup"><span data-stu-id="073e3-122">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="073e3-123">-Name</span></span>
<span data-ttu-id="073e3-124">Name des Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="073e3-124">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-125">-Path</span><span class="sxs-lookup"><span data-stu-id="073e3-125">-Path</span></span>
<span data-ttu-id="073e3-126">Gibt den Pfad zur Definitions-JSON-Datei für den Wiederherstellungsplan an.</span><span class="sxs-lookup"><span data-stu-id="073e3-126">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="073e3-127">Eine Wiederherstellungsplan-Definition JSON kann verwendet werden, um den Wiederherstellungsplan zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="073e3-127">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-128">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="073e3-128">-PrimaryFabric</span></span>
<span data-ttu-id="073e3-129">Gibt das ASR-Fabric-Objekt für die primäre ASR-Struktur der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="073e3-129">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="073e3-130">-RecoveryFabric</span></span>
<span data-ttu-id="073e3-131">Gibt das ASR-Fabric-Objekt für die Wiederherstellungs-ASR-Struktur der Replikations geschützten Elemente an, die Bestandteil dieses Wiederherstellungsplans sein werden.</span><span class="sxs-lookup"><span data-stu-id="073e3-131">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-132">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="073e3-132">-ReplicationProtectedItem</span></span>
<span data-ttu-id="073e3-133">Die Liste der durch die Replikation geschützten Elemente, die der ersten Gruppe des Wiederherstellungsplans hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="073e3-133">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="073e3-134">-WhatIf</span></span>
<span data-ttu-id="073e3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="073e3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="073e3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="073e3-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073e3-137">CommonParameters</span></span>
<span data-ttu-id="073e3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="073e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073e3-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="073e3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073e3-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="073e3-140">INPUTS</span></span>

### <span data-ttu-id="073e3-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="073e3-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="073e3-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="073e3-142">OUTPUTS</span></span>

### <span data-ttu-id="073e3-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="073e3-143">System.Object</span></span>

## <span data-ttu-id="073e3-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="073e3-144">NOTES</span></span>

## <span data-ttu-id="073e3-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="073e3-145">RELATED LINKS</span></span>

[<span data-ttu-id="073e3-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="073e3-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="073e3-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="073e3-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="073e3-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="073e3-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


