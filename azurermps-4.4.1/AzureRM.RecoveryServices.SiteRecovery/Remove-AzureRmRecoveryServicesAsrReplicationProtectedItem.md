---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 17836b900e56fdfd5d90211c9bceb79fce87c66e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664995"
---
# <span data-ttu-id="43b84-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43b84-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="43b84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43b84-102">SYNOPSIS</span></span>
<span data-ttu-id="43b84-103">Beendet/deaktiviert die Replikation für ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="43b84-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43b84-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43b84-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43b84-105">DESCRIPTION</span></span>
<span data-ttu-id="43b84-106">Das Cmdlet **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** deaktiviert die Replikation des angegebenen geschützten Elements für die Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="43b84-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="43b84-107">Dieser Vorgang bewirkt, dass die Replikation für das geschützte Element beendet wird.</span><span class="sxs-lookup"><span data-stu-id="43b84-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="43b84-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43b84-108">EXAMPLES</span></span>

### <span data-ttu-id="43b84-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43b84-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="43b84-110">Startet den deaktivierten Replikationsvorgang für das angegebene Replikations geschützte Element und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43b84-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="43b84-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="43b84-111">PARAMETERS</span></span>

### <span data-ttu-id="43b84-112">-Force</span><span class="sxs-lookup"><span data-stu-id="43b84-112">-Force</span></span>
<span data-ttu-id="43b84-113">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="43b84-113">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="43b84-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43b84-114">-InputObject</span></span>
<span data-ttu-id="43b84-115">Das Eingabeobjekt für das Cmdlet: das für die ASR-Replikation geschützte Element Objekt, das dem Replikations geschützten Element entspricht, für das die Replikation deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="43b84-115">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43b84-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="43b84-116">-WaitForCompletion</span></span>
<span data-ttu-id="43b84-117">Gibt an, dass das Cmdlet warten muss, bis der Vorgang abgeschlossen ist, bevor Sie zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="43b84-117">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="43b84-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43b84-118">-Confirm</span></span>
<span data-ttu-id="43b84-119">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="43b84-119">Specify if confirmation is required.</span></span> <span data-ttu-id="43b84-120">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="43b84-120">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="43b84-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b84-121">-WhatIf</span></span>
<span data-ttu-id="43b84-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="43b84-122">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="43b84-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b84-123">CommonParameters</span></span>
<span data-ttu-id="43b84-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b84-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b84-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b84-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b84-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43b84-126">INPUTS</span></span>

### <span data-ttu-id="43b84-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43b84-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="43b84-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43b84-128">OUTPUTS</span></span>

### <span data-ttu-id="43b84-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="43b84-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43b84-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="43b84-130">NOTES</span></span>

## <span data-ttu-id="43b84-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43b84-131">RELATED LINKS</span></span>

[<span data-ttu-id="43b84-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43b84-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="43b84-133">Neu – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43b84-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="43b84-134">Satz-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43b84-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
