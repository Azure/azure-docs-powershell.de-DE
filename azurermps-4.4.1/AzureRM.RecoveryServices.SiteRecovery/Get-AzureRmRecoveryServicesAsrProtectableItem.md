---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503993"
---
# <span data-ttu-id="f4cce-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f4cce-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="f4cce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4cce-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cce-103">Rufen Sie die geschützten Elemente in einem ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="f4cce-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4cce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4cce-104">SYNTAX</span></span>

### <span data-ttu-id="f4cce-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4cce-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="f4cce-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f4cce-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="f4cce-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f4cce-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="f4cce-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4cce-108">DESCRIPTION</span></span>
<span data-ttu-id="f4cce-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrProtectableItem** " Ruft die geschützten Elemente in einem Azure Site Recovery Protection-Container ab.</span><span class="sxs-lookup"><span data-stu-id="f4cce-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="f4cce-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4cce-110">EXAMPLES</span></span>

### <span data-ttu-id="f4cce-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4cce-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="f4cce-112">Ruft alle geschützten Elemente im angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="f4cce-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="f4cce-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4cce-113">PARAMETERS</span></span>

### <span data-ttu-id="f4cce-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f4cce-114">-FriendlyName</span></span>
<span data-ttu-id="f4cce-115">Gibt den Anzeigenamen des ASR-geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="f4cce-115">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="f4cce-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f4cce-116">-Name</span></span>
<span data-ttu-id="f4cce-117">Gibt den Namen des ASR-geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="f4cce-117">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="f4cce-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f4cce-118">-ProtectionContainer</span></span>
<span data-ttu-id="f4cce-119">Gibt das Azure Site Recovery Protection-Container Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f4cce-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4cce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cce-120">CommonParameters</span></span>
<span data-ttu-id="f4cce-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4cce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cce-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4cce-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cce-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4cce-123">INPUTS</span></span>

### <span data-ttu-id="f4cce-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f4cce-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="f4cce-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4cce-125">OUTPUTS</span></span>

### <span data-ttu-id="f4cce-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f4cce-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f4cce-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4cce-127">NOTES</span></span>

## <span data-ttu-id="f4cce-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4cce-128">RELATED LINKS</span></span>

[<span data-ttu-id="f4cce-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4cce-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="f4cce-130">Satz-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4cce-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
