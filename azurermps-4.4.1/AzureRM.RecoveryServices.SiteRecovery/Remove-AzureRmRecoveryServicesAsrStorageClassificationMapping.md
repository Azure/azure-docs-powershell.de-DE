---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501678"
---
# <span data-ttu-id="8019e-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8019e-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="8019e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8019e-102">SYNOPSIS</span></span>
<span data-ttu-id="8019e-103">Löscht die angegebene Zuordnung der ASR-Speicher Klassifikation.</span><span class="sxs-lookup"><span data-stu-id="8019e-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8019e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8019e-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8019e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8019e-105">DESCRIPTION</span></span>
<span data-ttu-id="8019e-106">Das Cmdlet **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** löscht die angegebene Zuordnung der angegebenen Azure Site Recovery-Speicher Klassifikation.</span><span class="sxs-lookup"><span data-stu-id="8019e-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="8019e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8019e-107">EXAMPLES</span></span>

### <span data-ttu-id="8019e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8019e-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="8019e-109">Startet das Löschen der angegebenen Speicher Klassifikations Zuordnung und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8019e-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8019e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8019e-110">PARAMETERS</span></span>

### <span data-ttu-id="8019e-111">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8019e-111">-InputObject</span></span>
<span data-ttu-id="8019e-112">Das Eingabeobjekt für das Cmdlet: das ASR-Zuordnungsobjekt, das der zu löschenden ASR-Speicher Klassifikations Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="8019e-112">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8019e-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8019e-113">-Confirm</span></span>
<span data-ttu-id="8019e-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8019e-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8019e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8019e-115">-WhatIf</span></span>
<span data-ttu-id="8019e-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8019e-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8019e-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8019e-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8019e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8019e-118">CommonParameters</span></span>
<span data-ttu-id="8019e-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8019e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8019e-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8019e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8019e-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8019e-121">INPUTS</span></span>

### <span data-ttu-id="8019e-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8019e-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="8019e-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8019e-123">OUTPUTS</span></span>

### <span data-ttu-id="8019e-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8019e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8019e-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8019e-125">NOTES</span></span>

## <span data-ttu-id="8019e-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8019e-126">RELATED LINKS</span></span>

[<span data-ttu-id="8019e-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8019e-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="8019e-128">Neu – AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8019e-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
