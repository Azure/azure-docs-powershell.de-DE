---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverycommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 839855b9b56e4ecc73552af310af7221c9b7b2d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502342"
---
# <span data-ttu-id="fd295-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="fd295-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="fd295-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd295-102">SYNOPSIS</span></span>
<span data-ttu-id="fd295-103">Startet die Commit-Failover-Aktion für ein Website Wiederherstellungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="fd295-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd295-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd295-104">SYNTAX</span></span>

### <span data-ttu-id="fd295-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd295-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd295-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="fd295-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd295-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="fd295-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd295-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd295-108">DESCRIPTION</span></span>
<span data-ttu-id="fd295-109">Mit dem Cmdlet " **Start-AzureRmSiteRecoveryCommitFailoverJob** " wird der Commit-Failoverprozess für ein Azure Site Recovery-Objekt nach einem Failover-Vorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="fd295-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="fd295-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd295-110">EXAMPLES</span></span>

## <span data-ttu-id="fd295-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd295-111">PARAMETERS</span></span>

### <span data-ttu-id="fd295-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd295-112">-DefaultProfile</span></span>
<span data-ttu-id="fd295-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd295-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd295-114">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="fd295-114">-ProtectionEntity</span></span>
<span data-ttu-id="fd295-115">Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="fd295-115">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="fd295-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd295-116">-RecoveryPlan</span></span>
<span data-ttu-id="fd295-117">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fd295-117">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="fd295-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fd295-118">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="fd295-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd295-119">CommonParameters</span></span>
<span data-ttu-id="fd295-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd295-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd295-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd295-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd295-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd295-122">INPUTS</span></span>

### <span data-ttu-id="fd295-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="fd295-123">ASRProtectionEntity</span></span>
<span data-ttu-id="fd295-124">Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd295-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="fd295-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd295-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="fd295-126">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd295-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="fd295-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fd295-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="fd295-128">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd295-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="fd295-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd295-129">OUTPUTS</span></span>

### <span data-ttu-id="fd295-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fd295-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fd295-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd295-131">NOTES</span></span>

## <span data-ttu-id="fd295-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd295-132">RELATED LINKS</span></span>

