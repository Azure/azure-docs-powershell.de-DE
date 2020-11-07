---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 3a28545958e353c5a5523e24baf20ac6bff21ef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663867"
---
# <span data-ttu-id="d76da-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="d76da-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="d76da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d76da-102">SYNOPSIS</span></span>
<span data-ttu-id="d76da-103">Ruft Informationen zu den Netzwerken ab, die von der Websitewiederherstellung für den aktuellen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="d76da-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d76da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d76da-104">SYNTAX</span></span>

### <span data-ttu-id="d76da-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="d76da-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="d76da-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d76da-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="d76da-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d76da-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="d76da-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d76da-108">DESCRIPTION</span></span>
<span data-ttu-id="d76da-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrNetwork** " Ruft Informationen zu Azure Site Recovery Networks für das aktuelle Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="d76da-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d76da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d76da-110">EXAMPLES</span></span>

### <span data-ttu-id="d76da-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d76da-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="d76da-112">Ruft alle bekannten Netzwerke im angegebenen Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="d76da-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="d76da-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d76da-113">PARAMETERS</span></span>

### <span data-ttu-id="d76da-114">-Stoff</span><span class="sxs-lookup"><span data-stu-id="d76da-114">-Fabric</span></span>
<span data-ttu-id="d76da-115">ASR-Fabric-Objekt</span><span class="sxs-lookup"><span data-stu-id="d76da-115">ASR fabric object</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d76da-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d76da-116">-FriendlyName</span></span>
<span data-ttu-id="d76da-117">Anzeigename des Network ASR-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d76da-117">Friendly name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d76da-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d76da-118">-Name</span></span>
<span data-ttu-id="d76da-119">Name des Network ASR-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d76da-119">Name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d76da-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76da-120">CommonParameters</span></span>
<span data-ttu-id="d76da-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76da-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76da-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d76da-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76da-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d76da-123">INPUTS</span></span>

### <span data-ttu-id="d76da-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d76da-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d76da-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d76da-125">OUTPUTS</span></span>

### <span data-ttu-id="d76da-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d76da-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d76da-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d76da-127">NOTES</span></span>

## <span data-ttu-id="d76da-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d76da-128">RELATED LINKS</span></span>

