---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476545"
---
# <span data-ttu-id="43ec6-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="43ec6-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="43ec6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="43ec6-103">Startet das ungeplante Failover für eine Standort Wiederherstellungs Schutzeinheit oder einen Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="43ec6-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43ec6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43ec6-104">SYNTAX</span></span>

### <span data-ttu-id="43ec6-105">ByPEObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="43ec6-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43ec6-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="43ec6-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43ec6-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="43ec6-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43ec6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43ec6-108">DESCRIPTION</span></span>
<span data-ttu-id="43ec6-109">Mit dem Cmdlet **Start-AzureRmSiteRecoveryUnplannedFailoverJob** wird das ungeplante Failover einer Azure Site Recovery Protection-Entität oder eines Wiederherstellungsplans gestartet.</span><span class="sxs-lookup"><span data-stu-id="43ec6-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="43ec6-110">Mithilfe des Get-AzureRmSiteRecoveryJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="43ec6-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="43ec6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43ec6-111">EXAMPLES</span></span>

## <span data-ttu-id="43ec6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="43ec6-112">PARAMETERS</span></span>

### <span data-ttu-id="43ec6-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="43ec6-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="43ec6-114">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="43ec6-114">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ec6-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="43ec6-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="43ec6-116">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="43ec6-116">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ec6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ec6-117">-DefaultProfile</span></span>
<span data-ttu-id="43ec6-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43ec6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43ec6-119">-Richtung</span><span class="sxs-lookup"><span data-stu-id="43ec6-119">-Direction</span></span>
<span data-ttu-id="43ec6-120">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="43ec6-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="43ec6-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="43ec6-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43ec6-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="43ec6-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="43ec6-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="43ec6-123">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ec6-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="43ec6-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="43ec6-125">Gibt an, dass die Aktion Quellwebsite Vorgänge ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="43ec6-125">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ec6-126">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="43ec6-126">-ProtectionEntity</span></span>
<span data-ttu-id="43ec6-127">Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="43ec6-127">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43ec6-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="43ec6-128">-RecoveryPlan</span></span>
<span data-ttu-id="43ec6-129">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="43ec6-129">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43ec6-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43ec6-130">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43ec6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ec6-131">CommonParameters</span></span>
<span data-ttu-id="43ec6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ec6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ec6-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ec6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ec6-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43ec6-134">INPUTS</span></span>

### <span data-ttu-id="43ec6-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="43ec6-135">ASRProtectionEntity</span></span>
<span data-ttu-id="43ec6-136">Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="43ec6-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="43ec6-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="43ec6-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="43ec6-138">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="43ec6-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="43ec6-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43ec6-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="43ec6-140">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="43ec6-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="43ec6-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43ec6-141">OUTPUTS</span></span>

### <span data-ttu-id="43ec6-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="43ec6-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43ec6-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="43ec6-143">NOTES</span></span>

## <span data-ttu-id="43ec6-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43ec6-144">RELATED LINKS</span></span>

[<span data-ttu-id="43ec6-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="43ec6-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


