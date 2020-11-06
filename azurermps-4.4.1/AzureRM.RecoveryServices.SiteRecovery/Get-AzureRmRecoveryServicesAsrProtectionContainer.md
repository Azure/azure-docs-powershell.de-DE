---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504793"
---
# <span data-ttu-id="274d8-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="274d8-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="274d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="274d8-102">SYNOPSIS</span></span>
<span data-ttu-id="274d8-103">Ruft ASR-Schutzcontainer im Speicher für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="274d8-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="274d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="274d8-104">SYNTAX</span></span>

### <span data-ttu-id="274d8-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="274d8-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="274d8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="274d8-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="274d8-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="274d8-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="274d8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="274d8-108">DESCRIPTION</span></span>
<span data-ttu-id="274d8-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrProtectionContainer** " ruft Azure Site Recovery Protection-Container im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="274d8-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="274d8-110">Ein Schutzcontainer ist ein logischer Container für schützende (erkannte) und geschützte Objekte wie virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="274d8-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="274d8-111">Replikationsrichtlinien definieren Replikationseinstellungen für geschützte Elemente und können einem Schutzcontainer zugeordnet und auf ein geschütztes Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="274d8-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="274d8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="274d8-112">EXAMPLES</span></span>

### <span data-ttu-id="274d8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="274d8-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="274d8-114">Ruft alle ASR-Schutzcontainer im angegebenen ASR-Fabric ab (die Pipelineeingabe im obigen Beispiel).</span><span class="sxs-lookup"><span data-stu-id="274d8-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="274d8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="274d8-115">PARAMETERS</span></span>

### <span data-ttu-id="274d8-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="274d8-116">-Fabric</span></span>
<span data-ttu-id="274d8-117">Suchen Sie im angegebenen ASR-Fabric nach dem Schutzcontainer.</span><span class="sxs-lookup"><span data-stu-id="274d8-117">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="274d8-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="274d8-118">-FriendlyName</span></span>
<span data-ttu-id="274d8-119">Gibt den Anzeigenamen des ASR-Schutz Containers an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="274d8-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="274d8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="274d8-120">-Name</span></span>
<span data-ttu-id="274d8-121">Gibt den Namen des ASR-Schutz Containers an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="274d8-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="274d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274d8-122">CommonParameters</span></span>
<span data-ttu-id="274d8-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="274d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274d8-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="274d8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274d8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="274d8-125">INPUTS</span></span>

### <span data-ttu-id="274d8-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="274d8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="274d8-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="274d8-127">OUTPUTS</span></span>

### <span data-ttu-id="274d8-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="274d8-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="274d8-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="274d8-129">NOTES</span></span>

## <span data-ttu-id="274d8-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="274d8-130">RELATED LINKS</span></span>

