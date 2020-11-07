---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 2d172c440163d70ef388c7de190371492767b2e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664996"
---
# <span data-ttu-id="98b11-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98b11-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="98b11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98b11-102">SYNOPSIS</span></span>
<span data-ttu-id="98b11-103">Verläßt den angegebenen ASR-Wiederherstellungsplan aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="98b11-103">Delets the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98b11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98b11-104">SYNTAX</span></span>

### <span data-ttu-id="98b11-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="98b11-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98b11-106">ByName</span><span class="sxs-lookup"><span data-stu-id="98b11-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b11-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98b11-107">DESCRIPTION</span></span>
<span data-ttu-id="98b11-108">Das Cmdlet **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** löscht den angegebenen Wiederherstellungsplan aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="98b11-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="98b11-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98b11-109">EXAMPLES</span></span>

### <span data-ttu-id="98b11-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98b11-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="98b11-111">Startet den Löschvorgang des angegebenen Wiederherstellungsplans und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98b11-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="98b11-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="98b11-112">PARAMETERS</span></span>

### <span data-ttu-id="98b11-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98b11-113">-InputObject</span></span>
<span data-ttu-id="98b11-114">Das Eingabeobjekt für das Cmdlet: das ASR-Wiederherstellungsplan Objekt, das dem Wiederherstellungsplan entspricht, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="98b11-114">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b11-115">-Name</span><span class="sxs-lookup"><span data-stu-id="98b11-115">-Name</span></span>
<span data-ttu-id="98b11-116">Gibt den Namen des Wiederherstellungsplans an, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="98b11-116">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="98b11-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="98b11-117">-Confirm</span></span>
<span data-ttu-id="98b11-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98b11-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b11-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b11-119">-WhatIf</span></span>
<span data-ttu-id="98b11-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98b11-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98b11-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98b11-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b11-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b11-122">CommonParameters</span></span>
<span data-ttu-id="98b11-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b11-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b11-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b11-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b11-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98b11-125">INPUTS</span></span>

### <span data-ttu-id="98b11-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98b11-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="98b11-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98b11-127">OUTPUTS</span></span>

### <span data-ttu-id="98b11-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="98b11-128">System.Object</span></span>

## <span data-ttu-id="98b11-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="98b11-129">NOTES</span></span>

## <span data-ttu-id="98b11-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98b11-130">RELATED LINKS</span></span>

[<span data-ttu-id="98b11-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98b11-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="98b11-132">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98b11-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="98b11-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98b11-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


