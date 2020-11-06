---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481481"
---
# <span data-ttu-id="5e492-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="5e492-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="5e492-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e492-102">SYNOPSIS</span></span>
<span data-ttu-id="5e492-103">Aktualisiert den Quell-und Zielserver zum Schutz eines Website Wiederherstellungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="5e492-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e492-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e492-104">SYNTAX</span></span>

### <span data-ttu-id="5e492-105">ByPEObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e492-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e492-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5e492-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e492-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="5e492-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e492-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e492-108">DESCRIPTION</span></span>
<span data-ttu-id="5e492-109">Das Cmdlet **Update-AzureRmSiteRecoveryProtectionDirection** aktualisiert den Quell-und Zielserver zum Schutz eines Azure Site Recovery-Objekts nach Abschluss eines Commit-Failover-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5e492-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="5e492-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e492-110">EXAMPLES</span></span>

## <span data-ttu-id="5e492-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e492-111">PARAMETERS</span></span>

### <span data-ttu-id="5e492-112">-Richtung</span><span class="sxs-lookup"><span data-stu-id="5e492-112">-Direction</span></span>
<span data-ttu-id="5e492-113">Gibt die Richtung des Commits an.</span><span class="sxs-lookup"><span data-stu-id="5e492-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="5e492-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5e492-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e492-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5e492-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="5e492-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5e492-116">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="5e492-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e492-117">-ProtectionEntity</span></span>
<span data-ttu-id="5e492-118">Gibt das Schutz Entitätsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="5e492-118">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="5e492-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5e492-119">-RecoveryPlan</span></span>
<span data-ttu-id="5e492-120">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5e492-120">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="5e492-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e492-121">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="5e492-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e492-122">-DefaultProfile</span></span>
<span data-ttu-id="5e492-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e492-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e492-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e492-124">CommonParameters</span></span>
<span data-ttu-id="5e492-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e492-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e492-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e492-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e492-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e492-127">INPUTS</span></span>

### <span data-ttu-id="5e492-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e492-128">ASRProtectionEntity</span></span>
<span data-ttu-id="5e492-129">Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e492-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="5e492-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5e492-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="5e492-131">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e492-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="5e492-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e492-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="5e492-133">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e492-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="5e492-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e492-134">OUTPUTS</span></span>

### <span data-ttu-id="5e492-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5e492-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e492-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e492-136">NOTES</span></span>

## <span data-ttu-id="5e492-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e492-137">RELATED LINKS</span></span>

