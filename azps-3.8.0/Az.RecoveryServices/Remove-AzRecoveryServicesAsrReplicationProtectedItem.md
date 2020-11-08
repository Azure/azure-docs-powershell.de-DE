---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997340"
---
# <span data-ttu-id="acd0b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="acd0b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="acd0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="acd0b-102">SYNOPSIS</span></span>
<span data-ttu-id="acd0b-103">Beendet/deaktiviert die Replikation für ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="acd0b-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="acd0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="acd0b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acd0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acd0b-105">DESCRIPTION</span></span>
<span data-ttu-id="acd0b-106">Das Cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** deaktiviert die Replikation des angegebenen geschützten Elements für die Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="acd0b-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="acd0b-107">Dieser Vorgang bewirkt, dass die Replikation für das geschützte Element beendet wird.</span><span class="sxs-lookup"><span data-stu-id="acd0b-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="acd0b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="acd0b-108">EXAMPLES</span></span>

### <span data-ttu-id="acd0b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="acd0b-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="acd0b-110">Startet den deaktivierten Replikationsvorgang für das angegebene Replikations geschützte Element und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="acd0b-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="acd0b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="acd0b-111">PARAMETERS</span></span>

### <span data-ttu-id="acd0b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd0b-112">-DefaultProfile</span></span>
<span data-ttu-id="acd0b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="acd0b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd0b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="acd0b-114">-Force</span></span>
<span data-ttu-id="acd0b-115">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="acd0b-115">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd0b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="acd0b-116">-InputObject</span></span>
<span data-ttu-id="acd0b-117">Das Eingabeobjekt für das Cmdlet: das für die ASR-Replikation geschützte Element Objekt, das dem Replikations geschützten Element entspricht, für das die Replikation deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="acd0b-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acd0b-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="acd0b-118">-WaitForCompletion</span></span>
<span data-ttu-id="acd0b-119">Gibt an, dass das Cmdlet warten muss, bis der Vorgang abgeschlossen ist, bevor Sie zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="acd0b-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd0b-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="acd0b-120">-Confirm</span></span>
<span data-ttu-id="acd0b-121">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="acd0b-121">Specify if confirmation is required.</span></span> <span data-ttu-id="acd0b-122">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="acd0b-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd0b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd0b-123">-WhatIf</span></span>
<span data-ttu-id="acd0b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="acd0b-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd0b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd0b-125">CommonParameters</span></span>
<span data-ttu-id="acd0b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd0b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd0b-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acd0b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd0b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="acd0b-128">INPUTS</span></span>

### <span data-ttu-id="acd0b-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="acd0b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="acd0b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="acd0b-130">OUTPUTS</span></span>

### <span data-ttu-id="acd0b-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="acd0b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="acd0b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="acd0b-132">NOTES</span></span>

## <span data-ttu-id="acd0b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="acd0b-133">RELATED LINKS</span></span>

[<span data-ttu-id="acd0b-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="acd0b-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="acd0b-135">Neu – AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="acd0b-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="acd0b-136">Satz-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="acd0b-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
