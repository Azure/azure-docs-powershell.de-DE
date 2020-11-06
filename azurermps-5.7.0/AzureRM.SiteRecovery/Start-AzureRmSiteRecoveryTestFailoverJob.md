---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverytestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 236ba6a3cbf65786af7d17e587ef5de0af86a296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478214"
---
# <span data-ttu-id="eea96-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="eea96-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="eea96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eea96-102">SYNOPSIS</span></span>
<span data-ttu-id="eea96-103">Startet ein testfailover für eine Website Wiederherstellungs Schutz Entität.</span><span class="sxs-lookup"><span data-stu-id="eea96-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eea96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eea96-104">SYNTAX</span></span>

### <span data-ttu-id="eea96-105">ByPEObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="eea96-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea96-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="eea96-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea96-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="eea96-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea96-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="eea96-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea96-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="eea96-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea96-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="eea96-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea96-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="eea96-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea96-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="eea96-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea96-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="eea96-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eea96-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eea96-114">DESCRIPTION</span></span>
<span data-ttu-id="eea96-115">Das Cmdlet **Start-AzureRmSiteRecoveryTestFailoverJob** startet das Test-Failover einer Azure Site Recovery Protection-Entität oder eines Wiederherstellungsplans.</span><span class="sxs-lookup"><span data-stu-id="eea96-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="eea96-116">Mithilfe des Get-AzureRmSiteRecoveryJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="eea96-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="eea96-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eea96-117">EXAMPLES</span></span>

## <span data-ttu-id="eea96-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="eea96-118">PARAMETERS</span></span>

### <span data-ttu-id="eea96-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="eea96-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="eea96-120">Gibt die Azure Virtual Network-ID an.</span><span class="sxs-lookup"><span data-stu-id="eea96-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea96-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="eea96-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="eea96-122">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="eea96-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="eea96-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="eea96-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="eea96-124">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="eea96-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="eea96-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea96-125">-DefaultProfile</span></span>
<span data-ttu-id="eea96-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eea96-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea96-127">-Richtung</span><span class="sxs-lookup"><span data-stu-id="eea96-127">-Direction</span></span>
<span data-ttu-id="eea96-128">Gibt die failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="eea96-128">Specifies the failover direction.</span></span>
<span data-ttu-id="eea96-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eea96-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eea96-130">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="eea96-130">PrimaryToRecovery</span></span>
- <span data-ttu-id="eea96-131">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="eea96-131">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="eea96-132">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="eea96-132">-ProtectionEntity</span></span>
<span data-ttu-id="eea96-133">Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="eea96-133">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eea96-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eea96-134">-RecoveryPlan</span></span>
<span data-ttu-id="eea96-135">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="eea96-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eea96-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="eea96-136">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eea96-137">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="eea96-137">-VMNetwork</span></span>
<span data-ttu-id="eea96-138">Gibt das Netzwerk der virtuellen Maschine für die Standortwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="eea96-138">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea96-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea96-139">CommonParameters</span></span>
<span data-ttu-id="eea96-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea96-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea96-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea96-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea96-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eea96-142">INPUTS</span></span>

### <span data-ttu-id="eea96-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="eea96-143">ASRProtectionEntity</span></span>
<span data-ttu-id="eea96-144">Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="eea96-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="eea96-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eea96-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="eea96-146">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="eea96-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="eea96-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="eea96-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="eea96-148">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="eea96-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="eea96-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eea96-149">OUTPUTS</span></span>

### <span data-ttu-id="eea96-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eea96-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eea96-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="eea96-151">NOTES</span></span>

## <span data-ttu-id="eea96-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eea96-152">RELATED LINKS</span></span>

[<span data-ttu-id="eea96-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="eea96-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
