---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295691"
---
# <span data-ttu-id="5c01a-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c01a-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="5c01a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c01a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c01a-103">Beendet/deaktiviert die Replikation für ein geschütztes Element der Azure-Websitewiederherstellungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="5c01a-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="5c01a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c01a-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c01a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c01a-105">DESCRIPTION</span></span>
<span data-ttu-id="5c01a-106">Das **Cmdlet "Remove-AzRecoveryServicesAsrReplicationProtectedItem"** deaktiviert die Replikation des angegebenen geschützten Azure Site Recovery-Replikationselements.</span><span class="sxs-lookup"><span data-stu-id="5c01a-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="5c01a-107">Dieser Vorgang bewirkt, dass die Replikation für das geschützte Element beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c01a-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="5c01a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c01a-108">EXAMPLES</span></span>

### <span data-ttu-id="5c01a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c01a-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="5c01a-110">Startet den Replikationsvorgang zum Deaktivieren für das angegebene replikationsgeschützte Element und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="5c01a-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5c01a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c01a-111">PARAMETERS</span></span>

### <span data-ttu-id="5c01a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c01a-112">-DefaultProfile</span></span>
<span data-ttu-id="5c01a-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c01a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5c01a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5c01a-114">-Force</span></span>
<span data-ttu-id="5c01a-115">Erzwingen Sie die Ausführung des Befehls, ohne eine zusätzliche Warnung bereitstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5c01a-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="5c01a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c01a-116">-InputObject</span></span>
<span data-ttu-id="5c01a-117">Das Eingabeobjekt für das Cmdlet: Das asR-replikationsgeschützte Elementobjekt, das dem replikationsgeschützten Element entspricht, für das die Replikation deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c01a-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="5c01a-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5c01a-118">-WaitForCompletion</span></span>
<span data-ttu-id="5c01a-119">Gibt an, dass das Cmdlet warten soll, bis der Vorgang abgeschlossen ist, bevor es zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="5c01a-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="5c01a-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c01a-120">-Confirm</span></span>
<span data-ttu-id="5c01a-121">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5c01a-121">Specify if confirmation is required.</span></span> <span data-ttu-id="5c01a-122">Legen Sie den Wert des Bestätigungsparameters auf "$false, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="5c01a-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="5c01a-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5c01a-123">-WhatIf</span></span>
<span data-ttu-id="5c01a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5c01a-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="5c01a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c01a-125">CommonParameters</span></span>
<span data-ttu-id="5c01a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c01a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c01a-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c01a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c01a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c01a-128">INPUTS</span></span>

### <span data-ttu-id="5c01a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c01a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5c01a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c01a-130">OUTPUTS</span></span>

### <span data-ttu-id="5c01a-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5c01a-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5c01a-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c01a-132">NOTES</span></span>

## <span data-ttu-id="5c01a-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c01a-133">RELATED LINKS</span></span>

[<span data-ttu-id="5c01a-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c01a-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="5c01a-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c01a-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="5c01a-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c01a-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
