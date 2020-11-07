---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 21a46346c681a6f184033d4f50d65e6c9a019844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663849"
---
# <span data-ttu-id="77852-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77852-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="77852-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77852-102">SYNOPSIS</span></span>
<span data-ttu-id="77852-103">Aktualisiert den Inhalt eines Azure Site Recovery-Plans.</span><span class="sxs-lookup"><span data-stu-id="77852-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77852-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77852-104">SYNTAX</span></span>

### <span data-ttu-id="77852-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="77852-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77852-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="77852-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77852-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77852-107">DESCRIPTION</span></span>
<span data-ttu-id="77852-108">Das Cmdlet **Update-AzureRmRecoveryServicesAsrRecoveryPlan** aktualisiert den Inhalt eines Wiederherstellungsplans unter Verwendung des Inhalts des angegebenen ASR-Wiederherstellungsplan Objekts oder der JSON-Datei für die ASR-Wiederherstellungsplan Definition.</span><span class="sxs-lookup"><span data-stu-id="77852-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="77852-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77852-109">EXAMPLES</span></span>

### <span data-ttu-id="77852-110">Beispiel 1: Aktualisieren eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="77852-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="77852-111">Starten Sie den Vorgang zum Aktualisieren eines Wiederherstellungsplans mithilfe des Inhalts des angegebenen ASR-Wiederherstellungsplan Objekts, und geben Sie den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77852-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="77852-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="77852-112">PARAMETERS</span></span>

### <span data-ttu-id="77852-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77852-113">-InputObject</span></span>
<span data-ttu-id="77852-114">Eingabeobjekt für das Cmdlet: gibt ein ASR-Wiederherstellungsplan-Objekt an, dessen Inhalt zum Aktualisieren des Wiederherstellungsplans verwendet wird, auf den das Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="77852-114">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77852-115">-Path</span><span class="sxs-lookup"><span data-stu-id="77852-115">-Path</span></span>
<span data-ttu-id="77852-116">Gibt den Pfad der JSON-Datei für die Wiederherstellungsplan Definition an, mit der der Wiederherstellungsplan aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="77852-116">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77852-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77852-117">-Confirm</span></span>
<span data-ttu-id="77852-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77852-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77852-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77852-119">-WhatIf</span></span>
<span data-ttu-id="77852-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77852-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77852-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77852-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77852-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77852-122">CommonParameters</span></span>
<span data-ttu-id="77852-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77852-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77852-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77852-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77852-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77852-125">INPUTS</span></span>

### <span data-ttu-id="77852-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77852-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="77852-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77852-127">OUTPUTS</span></span>

### <span data-ttu-id="77852-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="77852-128">System.Object</span></span>

## <span data-ttu-id="77852-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="77852-129">NOTES</span></span>

## <span data-ttu-id="77852-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77852-130">RELATED LINKS</span></span>

[<span data-ttu-id="77852-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77852-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="77852-132">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77852-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="77852-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="77852-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)


