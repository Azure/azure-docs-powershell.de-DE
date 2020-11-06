---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504789"
---
# <span data-ttu-id="b7c14-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b7c14-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="b7c14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7c14-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c14-103">Ruft die Eigenschaften von geschützten Elementen einer Azure Site Recovery-Replikation ab.</span><span class="sxs-lookup"><span data-stu-id="b7c14-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7c14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c14-104">SYNTAX</span></span>

### <span data-ttu-id="b7c14-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7c14-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="b7c14-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b7c14-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="b7c14-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b7c14-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="b7c14-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="b7c14-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## <span data-ttu-id="b7c14-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7c14-109">DESCRIPTION</span></span>
<span data-ttu-id="b7c14-110">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** " Ruft die Eigenschaften aller oder des angegebenen ASR-Replikations geschützten Elements aus dem angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="b7c14-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="b7c14-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7c14-111">EXAMPLES</span></span>

### <span data-ttu-id="b7c14-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7c14-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="b7c14-113">Listet alle durch die Replikation geschützten Elemente im angegebenen ASR-Schutzcontainer auf.</span><span class="sxs-lookup"><span data-stu-id="b7c14-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="b7c14-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7c14-114">PARAMETERS</span></span>

### <span data-ttu-id="b7c14-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b7c14-115">-FriendlyName</span></span>
<span data-ttu-id="b7c14-116">Gibt den Anzeigenamen des abzurufenden Replikations geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="b7c14-116">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="b7c14-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b7c14-117">-Name</span></span>
<span data-ttu-id="b7c14-118">Gibt den Namen des abzurufenden Replikations geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="b7c14-118">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="b7c14-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b7c14-119">-ProtectableItem</span></span>
<span data-ttu-id="b7c14-120">Gibt ein geschütztes ASR-Element Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b7c14-120">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="b7c14-121">Das Cmdlet ruft das geschützte ASR-Replikations Element ab, das dem angegebenen ASR-Schutzelement entspricht, wenn das Element geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="b7c14-121">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

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

### <span data-ttu-id="b7c14-122">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b7c14-122">-ProtectionContainer</span></span>
<span data-ttu-id="b7c14-123">Gibt das ASR-Schutzcontainer Objekt des ASR-Schutz Containers an, das dem geschützten Replikat Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="b7c14-123">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

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

### <span data-ttu-id="b7c14-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c14-124">CommonParameters</span></span>
<span data-ttu-id="b7c14-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c14-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c14-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c14-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c14-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7c14-127">INPUTS</span></span>

### <span data-ttu-id="b7c14-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b7c14-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="b7c14-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b7c14-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="b7c14-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7c14-130">OUTPUTS</span></span>

### <span data-ttu-id="b7c14-131">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b7c14-131">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b7c14-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7c14-132">NOTES</span></span>

## <span data-ttu-id="b7c14-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7c14-133">RELATED LINKS</span></span>

[<span data-ttu-id="b7c14-134">Neu – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b7c14-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="b7c14-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b7c14-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="b7c14-136">Satz-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b7c14-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
