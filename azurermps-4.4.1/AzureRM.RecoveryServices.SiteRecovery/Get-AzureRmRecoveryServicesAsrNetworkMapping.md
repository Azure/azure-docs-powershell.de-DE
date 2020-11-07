---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665003"
---
# <span data-ttu-id="67dfc-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67dfc-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="67dfc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="67dfc-103">Ruft Informationen zu den Netzwerkzuordnungen der Websitewiederherstellung für den aktuellen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="67dfc-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67dfc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67dfc-104">SYNTAX</span></span>

### <span data-ttu-id="67dfc-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="67dfc-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="67dfc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="67dfc-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="67dfc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67dfc-107">DESCRIPTION</span></span>
<span data-ttu-id="67dfc-108">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrNetworkMapping** " Ruft Informationen zu Azure Site Recovery Network-Zuordnungen für den Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="67dfc-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="67dfc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67dfc-109">EXAMPLES</span></span>

### <span data-ttu-id="67dfc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67dfc-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="67dfc-111">Ruft alle Netz Zuordnungen für das übergebene Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="67dfc-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="67dfc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="67dfc-112">PARAMETERS</span></span>

### <span data-ttu-id="67dfc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="67dfc-113">-Name</span></span>
<span data-ttu-id="67dfc-114">Der Name des abzurufenden ASR-Netzwerk Zuordnungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="67dfc-114">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="67dfc-115">-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="67dfc-115">-Network</span></span>
<span data-ttu-id="67dfc-116">Rufen Sie die ASR-Netzwerkzuordnungen ab, die dem angegebenen Netzwerk ASR-Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="67dfc-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67dfc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67dfc-117">CommonParameters</span></span>
<span data-ttu-id="67dfc-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67dfc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67dfc-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67dfc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67dfc-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67dfc-120">INPUTS</span></span>

### <span data-ttu-id="67dfc-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="67dfc-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="67dfc-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67dfc-122">OUTPUTS</span></span>

### <span data-ttu-id="67dfc-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="67dfc-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="67dfc-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="67dfc-124">NOTES</span></span>

## <span data-ttu-id="67dfc-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67dfc-125">RELATED LINKS</span></span>

[<span data-ttu-id="67dfc-126">Neu – AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67dfc-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="67dfc-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67dfc-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
