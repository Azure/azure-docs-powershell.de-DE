---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503982"
---
# <span data-ttu-id="3d02e-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="3d02e-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="3d02e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d02e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d02e-103">Ruft die verfügbaren (gefundenen) ASR-Speicher Klassifikationen im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="3d02e-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d02e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d02e-104">SYNTAX</span></span>

### <span data-ttu-id="3d02e-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d02e-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="3d02e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3d02e-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="3d02e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3d02e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="3d02e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d02e-108">DESCRIPTION</span></span>
<span data-ttu-id="3d02e-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrStorageClassification** " ruft Details der erkannten ASR-Speicher Klassifikationen im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="3d02e-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="3d02e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d02e-110">EXAMPLES</span></span>

### <span data-ttu-id="3d02e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d02e-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="3d02e-112">Listen Sie die ermittelten Speicher Klassifikationen auf, die dem angegebenen ASR-Fabric entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3d02e-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="3d02e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d02e-113">PARAMETERS</span></span>

### <span data-ttu-id="3d02e-114">-Stoff</span><span class="sxs-lookup"><span data-stu-id="3d02e-114">-Fabric</span></span>
<span data-ttu-id="3d02e-115">Gibt ein ASR-Fabric-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3d02e-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="3d02e-116">Das Cmdlet ruft die Details der erkannten Speicher Klassifizierungen ab, die dem angegebenen ASR-Fabric entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3d02e-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="3d02e-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3d02e-117">-FriendlyName</span></span>
<span data-ttu-id="3d02e-118">Gibt den Anzeigenamen des abzurufenden Speicher Klassifizierungs Objekts an.</span><span class="sxs-lookup"><span data-stu-id="3d02e-118">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="3d02e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3d02e-119">-Name</span></span>
<span data-ttu-id="3d02e-120">Gibt den Namen des abzurufenden Speicher Klassifizierungs Objekts an.</span><span class="sxs-lookup"><span data-stu-id="3d02e-120">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="3d02e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d02e-121">CommonParameters</span></span>
<span data-ttu-id="3d02e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d02e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d02e-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d02e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d02e-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d02e-124">INPUTS</span></span>

### <span data-ttu-id="3d02e-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3d02e-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3d02e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d02e-126">OUTPUTS</span></span>

### <span data-ttu-id="3d02e-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3d02e-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3d02e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d02e-128">NOTES</span></span>

## <span data-ttu-id="3d02e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d02e-129">RELATED LINKS</span></span>

