---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663850"
---
# <span data-ttu-id="4c724-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4c724-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="4c724-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c724-102">SYNOPSIS</span></span>
<span data-ttu-id="4c724-103">Aktualisiert (Server aktualisieren) die Informationen, die vom Azure Site Recovery Services-Anbieter empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="4c724-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c724-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c724-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c724-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c724-105">DESCRIPTION</span></span>
<span data-ttu-id="4c724-106">Mit dem Cmdlet **Update-AzureRmRecoveryServicesAsrServicesProvider** werden die vom Azure Site Recovery Services-Anbieter empfangenen Informationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4c724-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="4c724-107">Mit diesem Cmdlet können Sie eine Aktualisierung der vom Wiederherstellungsdienste-Anbieter empfangenen Informationen auslösen.</span><span class="sxs-lookup"><span data-stu-id="4c724-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="4c724-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c724-108">EXAMPLES</span></span>

### <span data-ttu-id="4c724-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c724-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="4c724-110">Startet den Vorgang zum Aktualisieren der Informationen vom angegebenen ASR-Dienstanbieter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c724-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="4c724-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c724-111">PARAMETERS</span></span>

### <span data-ttu-id="4c724-112">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4c724-112">-InputObject</span></span>
<span data-ttu-id="4c724-113">Input-Objekt: gibt das ASR-Dienstanbieterobjekt an, das dem ASR-Dienstanbieter entspricht, der den Server identifiziert, für den Informationen aktualisiert werden sollen (aktualisiert).</span><span class="sxs-lookup"><span data-stu-id="4c724-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c724-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c724-114">-Confirm</span></span>
<span data-ttu-id="4c724-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c724-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c724-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c724-116">-WhatIf</span></span>
<span data-ttu-id="4c724-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c724-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c724-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c724-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c724-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c724-119">CommonParameters</span></span>
<span data-ttu-id="4c724-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c724-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c724-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c724-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c724-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c724-122">INPUTS</span></span>

### <span data-ttu-id="4c724-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4c724-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="4c724-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c724-124">OUTPUTS</span></span>

### <span data-ttu-id="4c724-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="4c724-125">System.Object</span></span>

## <span data-ttu-id="4c724-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c724-126">NOTES</span></span>

## <span data-ttu-id="4c724-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c724-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c724-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4c724-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="4c724-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4c724-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
