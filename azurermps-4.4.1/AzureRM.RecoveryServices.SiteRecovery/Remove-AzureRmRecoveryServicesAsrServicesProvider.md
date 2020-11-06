---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5220271538903206876dd8d5c476824e1ac10874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504774"
---
# <span data-ttu-id="72761-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="72761-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="72761-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72761-102">SYNOPSIS</span></span>
<span data-ttu-id="72761-103">Löscht/hebt die Registrierung des angegebenen Azure Site Recovery Recovery Services-Anbieters aus dem Vault für Wiederherstellungsdienste auf.</span><span class="sxs-lookup"><span data-stu-id="72761-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72761-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72761-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72761-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72761-105">DESCRIPTION</span></span>
<span data-ttu-id="72761-106">Mit dem Cmdlet **Remove-AzureRmRecoveryServicesAsrServicesProvider** wird der angegebene Azure Site Recovery Recovery Services-Anbieter aus dem Tresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="72761-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="72761-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72761-107">EXAMPLES</span></span>

### <span data-ttu-id="72761-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72761-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="72761-109">Startet die Löschung/Aufhebung der Registrierung des angegebenen Azure Site Recovery Services-Anbieters und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72761-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="72761-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="72761-110">PARAMETERS</span></span>

### <span data-ttu-id="72761-111">-Force</span><span class="sxs-lookup"><span data-stu-id="72761-111">-Force</span></span>
<span data-ttu-id="72761-112">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="72761-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72761-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="72761-113">-InputObject</span></span>
<span data-ttu-id="72761-114">Das Eingabeobjekt für das Cmdlet: das Dienstanbieterobjekt für ASR-Wiederherstellungsdienste, das dem zu löschenden Dienstanbieter für ASR-Wiederherstellungsdienste entspricht.</span><span class="sxs-lookup"><span data-stu-id="72761-114">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="72761-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72761-115">-Confirm</span></span>
<span data-ttu-id="72761-116">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="72761-116">Specify if confirmation is required.</span></span> <span data-ttu-id="72761-117">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="72761-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="72761-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72761-118">-WhatIf</span></span>
<span data-ttu-id="72761-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="72761-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="72761-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72761-120">CommonParameters</span></span>
<span data-ttu-id="72761-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72761-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72761-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72761-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72761-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72761-123">INPUTS</span></span>

### <span data-ttu-id="72761-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="72761-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="72761-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72761-125">OUTPUTS</span></span>

### <span data-ttu-id="72761-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="72761-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="72761-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="72761-127">NOTES</span></span>

## <span data-ttu-id="72761-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72761-128">RELATED LINKS</span></span>

[<span data-ttu-id="72761-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="72761-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="72761-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="72761-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
