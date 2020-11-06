---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1df32bfcf049346b3f434b252a413eef020d0b77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482838"
---
# <span data-ttu-id="43aec-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43aec-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="43aec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43aec-102">SYNOPSIS</span></span>
<span data-ttu-id="43aec-103">Beendet/deaktiviert die Replikation für ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="43aec-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43aec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43aec-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43aec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43aec-105">DESCRIPTION</span></span>
<span data-ttu-id="43aec-106">Das Cmdlet **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** deaktiviert die Replikation des angegebenen geschützten Elements für die Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="43aec-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="43aec-107">Dieser Vorgang bewirkt, dass die Replikation für das geschützte Element beendet wird.</span><span class="sxs-lookup"><span data-stu-id="43aec-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="43aec-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43aec-108">EXAMPLES</span></span>

### <span data-ttu-id="43aec-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43aec-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="43aec-110">Startet den deaktivierten Replikationsvorgang für das angegebene Replikations geschützte Element und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43aec-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="43aec-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="43aec-111">PARAMETERS</span></span>

### <span data-ttu-id="43aec-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43aec-112">-Confirm</span></span>
<span data-ttu-id="43aec-113">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="43aec-113">Specify if confirmation is required.</span></span> <span data-ttu-id="43aec-114">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="43aec-114">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="43aec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43aec-115">-DefaultProfile</span></span>
<span data-ttu-id="43aec-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43aec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43aec-117">-Force</span><span class="sxs-lookup"><span data-stu-id="43aec-117">-Force</span></span>
<span data-ttu-id="43aec-118">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="43aec-118">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="43aec-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43aec-119">-InputObject</span></span>
<span data-ttu-id="43aec-120">Das Eingabeobjekt für das Cmdlet: das für die ASR-Replikation geschützte Element Objekt, das dem Replikations geschützten Element entspricht, für das die Replikation deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="43aec-120">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="43aec-121">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="43aec-121">-WaitForCompletion</span></span>
<span data-ttu-id="43aec-122">Gibt an, dass das Cmdlet warten muss, bis der Vorgang abgeschlossen ist, bevor Sie zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="43aec-122">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="43aec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43aec-123">-WhatIf</span></span>
<span data-ttu-id="43aec-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="43aec-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="43aec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43aec-125">CommonParameters</span></span>
<span data-ttu-id="43aec-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43aec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43aec-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43aec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43aec-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43aec-128">INPUTS</span></span>

### <span data-ttu-id="43aec-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43aec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="43aec-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43aec-130">OUTPUTS</span></span>

### <span data-ttu-id="43aec-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="43aec-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43aec-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="43aec-132">NOTES</span></span>

## <span data-ttu-id="43aec-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43aec-133">RELATED LINKS</span></span>

[<span data-ttu-id="43aec-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43aec-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="43aec-135">Neu – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43aec-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="43aec-136">Satz-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="43aec-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
