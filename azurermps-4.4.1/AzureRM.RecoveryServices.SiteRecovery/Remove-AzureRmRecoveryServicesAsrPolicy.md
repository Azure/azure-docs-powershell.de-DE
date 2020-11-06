---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481678"
---
# <span data-ttu-id="d8a6d-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d8a6d-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="d8a6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a6d-103">Löscht die angegebene ASR-Replikationsrichtlinie aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8a6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8a6d-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8a6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a6d-106">Das Cmdlet " **Remove-AzureRmRecoveryServicesAsrPolicy** " hat die angegebene Replikationsrichtlinie aus dem Vault für Wiederherstellungsdienste gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="d8a6d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8a6d-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a6d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8a6d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="d8a6d-109">Startet das Löschen der angegebenen Replikationsrichtlinie und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d8a6d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8a6d-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a6d-111">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8a6d-111">-InputObject</span></span>
<span data-ttu-id="d8a6d-112">Das Eingabeobjekt für das Cmdlet: das ASR-Replikationsrichtlinien Objekt, das der zu löschenden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-112">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a6d-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8a6d-113">-Confirm</span></span>
<span data-ttu-id="d8a6d-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8a6d-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8a6d-115">-WhatIf</span></span>
<span data-ttu-id="d8a6d-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8a6d-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8a6d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a6d-118">CommonParameters</span></span>
<span data-ttu-id="d8a6d-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a6d-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a6d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a6d-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8a6d-121">INPUTS</span></span>

### <span data-ttu-id="d8a6d-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d8a6d-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="d8a6d-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8a6d-123">OUTPUTS</span></span>

### <span data-ttu-id="d8a6d-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="d8a6d-124">System.Object</span></span>

## <span data-ttu-id="d8a6d-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8a6d-125">NOTES</span></span>

## <span data-ttu-id="d8a6d-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8a6d-126">RELATED LINKS</span></span>

[<span data-ttu-id="d8a6d-127">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d8a6d-127">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="d8a6d-128">Neu – AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d8a6d-128">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
