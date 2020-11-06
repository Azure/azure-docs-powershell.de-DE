---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 90b615edefe860e084de0040a13c1ba5a1ff39ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481018"
---
# <span data-ttu-id="d39d4-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d39d4-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="d39d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d39d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d39d4-103">Ruft die Eigenschaften von geschützten Elementen einer Azure Site Recovery-Replikation ab.</span><span class="sxs-lookup"><span data-stu-id="d39d4-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d39d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d39d4-104">SYNTAX</span></span>

### <span data-ttu-id="d39d4-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="d39d4-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d39d4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d39d4-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d39d4-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d39d4-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d39d4-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="d39d4-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d39d4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d39d4-109">DESCRIPTION</span></span>
<span data-ttu-id="d39d4-110">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** " Ruft die Eigenschaften aller oder des angegebenen ASR-Replikations geschützten Elements aus dem angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="d39d4-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="d39d4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d39d4-111">EXAMPLES</span></span>

### <span data-ttu-id="d39d4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d39d4-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="d39d4-113">Listet alle durch die Replikation geschützten Elemente im angegebenen ASR-Schutzcontainer auf.</span><span class="sxs-lookup"><span data-stu-id="d39d4-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="d39d4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d39d4-114">PARAMETERS</span></span>

### <span data-ttu-id="d39d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39d4-115">-DefaultProfile</span></span>
<span data-ttu-id="d39d4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d39d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="d39d4-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d39d4-117">-FriendlyName</span></span>
<span data-ttu-id="d39d4-118">Gibt den Anzeigenamen des abzurufenden Replikations geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="d39d4-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39d4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d39d4-119">-Name</span></span>
<span data-ttu-id="d39d4-120">Gibt den Namen des abzurufenden Replikations geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="d39d4-120">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39d4-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d39d4-121">-ProtectableItem</span></span>
<span data-ttu-id="d39d4-122">Gibt ein geschütztes ASR-Element Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d39d4-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="d39d4-123">Das Cmdlet ruft das geschützte ASR-Replikations Element ab, das dem angegebenen ASR-Schutzelement entspricht, wenn das Element geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="d39d4-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d39d4-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d39d4-124">-ProtectionContainer</span></span>
<span data-ttu-id="d39d4-125">Gibt das ASR-Schutzcontainer Objekt des ASR-Schutz Containers an, das dem geschützten Replikat Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="d39d4-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d39d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39d4-126">CommonParameters</span></span>
<span data-ttu-id="d39d4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d39d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39d4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d39d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39d4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d39d4-129">INPUTS</span></span>

### <span data-ttu-id="d39d4-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d39d4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="d39d4-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d39d4-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="d39d4-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d39d4-132">OUTPUTS</span></span>

### <span data-ttu-id="d39d4-133">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d39d4-133">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d39d4-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d39d4-134">NOTES</span></span>

## <span data-ttu-id="d39d4-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d39d4-135">RELATED LINKS</span></span>

[<span data-ttu-id="d39d4-136">Neu – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d39d4-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d39d4-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d39d4-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d39d4-138">Satz-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d39d4-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
