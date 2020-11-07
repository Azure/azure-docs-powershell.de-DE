---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663865"
---
# <span data-ttu-id="53fe8-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="53fe8-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="53fe8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="53fe8-103">Ruft ASR-Speicher Klassifikations Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="53fe8-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53fe8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53fe8-104">SYNTAX</span></span>

### <span data-ttu-id="53fe8-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="53fe8-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="53fe8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="53fe8-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="53fe8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53fe8-107">DESCRIPTION</span></span>
<span data-ttu-id="53fe8-108">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** " Ruft die Details einer ASR-Speicher Klassifikations Zuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="53fe8-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="53fe8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53fe8-109">EXAMPLES</span></span>

### <span data-ttu-id="53fe8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53fe8-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="53fe8-111">Listet alle Speicher Klassifikations Zuordnungen auf, die der angegebenen speicherklassifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="53fe8-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="53fe8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="53fe8-112">PARAMETERS</span></span>

### <span data-ttu-id="53fe8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="53fe8-113">-Name</span></span>
<span data-ttu-id="53fe8-114">Gibt den Namen der abzurufenden Speicher Klassifikations Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="53fe8-114">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="53fe8-115">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="53fe8-115">-StorageClassification</span></span>
<span data-ttu-id="53fe8-116">Gibt ein ASR-Speicher Klassifikations Objekt an.</span><span class="sxs-lookup"><span data-stu-id="53fe8-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="53fe8-117">Das Cmdlet ruft ASR-Speicher Klassifikations Zuordnungen ab, die der angegebenen speicherklassifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="53fe8-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53fe8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53fe8-118">CommonParameters</span></span>
<span data-ttu-id="53fe8-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53fe8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53fe8-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53fe8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53fe8-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53fe8-121">INPUTS</span></span>

### <span data-ttu-id="53fe8-122">Keine</span><span class="sxs-lookup"><span data-stu-id="53fe8-122">None</span></span>

## <span data-ttu-id="53fe8-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53fe8-123">OUTPUTS</span></span>

### <span data-ttu-id="53fe8-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="53fe8-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="53fe8-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="53fe8-125">NOTES</span></span>

## <span data-ttu-id="53fe8-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53fe8-126">RELATED LINKS</span></span>

[<span data-ttu-id="53fe8-127">Neu – AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="53fe8-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="53fe8-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="53fe8-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
