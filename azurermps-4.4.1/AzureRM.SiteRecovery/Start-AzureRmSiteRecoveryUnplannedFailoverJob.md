---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: a0a6ee7f0430453aef343ba971126cd9aff63f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478913"
---
# <span data-ttu-id="1718a-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1718a-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="1718a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1718a-102">SYNOPSIS</span></span>
<span data-ttu-id="1718a-103">Startet das ungeplante Failover für eine Standort Wiederherstellungs Schutzeinheit oder einen Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="1718a-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1718a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1718a-104">SYNTAX</span></span>

### <span data-ttu-id="1718a-105">ByPEObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="1718a-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1718a-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1718a-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1718a-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="1718a-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1718a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1718a-108">DESCRIPTION</span></span>
<span data-ttu-id="1718a-109">Mit dem Cmdlet **Start-AzureRmSiteRecoveryUnplannedFailoverJob** wird das ungeplante Failover einer Azure Site Recovery Protection-Entität oder eines Wiederherstellungsplans gestartet.</span><span class="sxs-lookup"><span data-stu-id="1718a-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="1718a-110">Mithilfe des Get-AzureRmSiteRecoveryJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1718a-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="1718a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1718a-111">EXAMPLES</span></span>

## <span data-ttu-id="1718a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1718a-112">PARAMETERS</span></span>

### <span data-ttu-id="1718a-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1718a-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1718a-114">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="1718a-114">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1718a-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1718a-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1718a-116">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="1718a-116">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1718a-117">-Richtung</span><span class="sxs-lookup"><span data-stu-id="1718a-117">-Direction</span></span>
<span data-ttu-id="1718a-118">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="1718a-118">Specifies the direction of the failover.</span></span>
<span data-ttu-id="1718a-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1718a-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1718a-120">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1718a-120">PrimaryToRecovery</span></span>
- <span data-ttu-id="1718a-121">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1718a-121">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1718a-122">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="1718a-122">-PerformSourceSideActions</span></span>
<span data-ttu-id="1718a-123">Gibt an, dass die Aktion Quellwebsite Vorgänge ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="1718a-123">Indicates that the action can perform source site operations.</span></span>

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

### <span data-ttu-id="1718a-124">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1718a-124">-ProtectionEntity</span></span>
<span data-ttu-id="1718a-125">Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="1718a-125">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1718a-126">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1718a-126">-RecoveryPlan</span></span>
<span data-ttu-id="1718a-127">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1718a-127">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1718a-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1718a-128">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1718a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1718a-129">-DefaultProfile</span></span>
<span data-ttu-id="1718a-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1718a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1718a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1718a-131">CommonParameters</span></span>
<span data-ttu-id="1718a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1718a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1718a-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1718a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1718a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1718a-134">INPUTS</span></span>

### <span data-ttu-id="1718a-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1718a-135">ASRProtectionEntity</span></span>
<span data-ttu-id="1718a-136">Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1718a-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="1718a-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1718a-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="1718a-138">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1718a-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="1718a-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1718a-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="1718a-140">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1718a-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="1718a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1718a-141">OUTPUTS</span></span>

### <span data-ttu-id="1718a-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1718a-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1718a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="1718a-143">NOTES</span></span>

## <span data-ttu-id="1718a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1718a-144">RELATED LINKS</span></span>

[<span data-ttu-id="1718a-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1718a-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


