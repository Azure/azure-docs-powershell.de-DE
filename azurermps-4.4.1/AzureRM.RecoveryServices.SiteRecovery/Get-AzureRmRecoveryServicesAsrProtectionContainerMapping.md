---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503986"
---
# <span data-ttu-id="60168-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="60168-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="60168-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60168-102">SYNOPSIS</span></span>
<span data-ttu-id="60168-103">Ruft Azure Site Recovery Protection-Container Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="60168-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60168-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60168-104">SYNTAX</span></span>

### <span data-ttu-id="60168-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="60168-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="60168-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="60168-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="60168-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60168-107">DESCRIPTION</span></span>
<span data-ttu-id="60168-108">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** " Ruft Informationen über den Schutzcontainer für Replikationsrichtlinien Zuordnungen (Association) im Tresor für den angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="60168-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="60168-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60168-109">EXAMPLES</span></span>

### <span data-ttu-id="60168-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60168-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="60168-111">Ruft alle Schutzcontainer Zuordnungen für den angegebenen Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="60168-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="60168-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="60168-112">PARAMETERS</span></span>

### <span data-ttu-id="60168-113">-Name</span><span class="sxs-lookup"><span data-stu-id="60168-113">-Name</span></span>
<span data-ttu-id="60168-114">Gibt den Namen der abzurufenden Schutzcontainer Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="60168-114">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="60168-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="60168-115">-ProtectionContainer</span></span>
<span data-ttu-id="60168-116">Erhalten Sie Schutzcontainer Zuordnungen, die dem angegebenen ASR-Schutzcontainer Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="60168-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="60168-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60168-117">CommonParameters</span></span>
<span data-ttu-id="60168-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60168-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60168-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60168-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60168-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60168-120">INPUTS</span></span>

### <span data-ttu-id="60168-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="60168-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="60168-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60168-122">OUTPUTS</span></span>

### <span data-ttu-id="60168-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="60168-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="60168-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="60168-124">NOTES</span></span>

## <span data-ttu-id="60168-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60168-125">RELATED LINKS</span></span>

[<span data-ttu-id="60168-126">Neu – AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="60168-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="60168-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="60168-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
