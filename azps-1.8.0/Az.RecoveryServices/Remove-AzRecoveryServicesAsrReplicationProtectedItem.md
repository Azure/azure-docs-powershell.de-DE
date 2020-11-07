---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 19a10312046a4c52ed1fad29732347f719065b95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659844"
---
# <span data-ttu-id="97afb-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="97afb-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="97afb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97afb-102">SYNOPSIS</span></span>
<span data-ttu-id="97afb-103">Beendet/deaktiviert die Replikation für ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="97afb-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="97afb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97afb-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97afb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97afb-105">DESCRIPTION</span></span>
<span data-ttu-id="97afb-106">Das Cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** deaktiviert die Replikation des angegebenen geschützten Elements für die Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="97afb-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="97afb-107">Dieser Vorgang bewirkt, dass die Replikation für das geschützte Element beendet wird.</span><span class="sxs-lookup"><span data-stu-id="97afb-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="97afb-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97afb-108">EXAMPLES</span></span>

### <span data-ttu-id="97afb-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97afb-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="97afb-110">Startet den deaktivierten Replikationsvorgang für das angegebene Replikations geschützte Element und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97afb-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="97afb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="97afb-111">PARAMETERS</span></span>

### <span data-ttu-id="97afb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97afb-112">-DefaultProfile</span></span>
<span data-ttu-id="97afb-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97afb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="97afb-114">-Force</span><span class="sxs-lookup"><span data-stu-id="97afb-114">-Force</span></span>
<span data-ttu-id="97afb-115">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="97afb-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="97afb-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="97afb-116">-InputObject</span></span>
<span data-ttu-id="97afb-117">Das Eingabeobjekt für das Cmdlet: das für die ASR-Replikation geschützte Element Objekt, das dem Replikations geschützten Element entspricht, für das die Replikation deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="97afb-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="97afb-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="97afb-118">-WaitForCompletion</span></span>
<span data-ttu-id="97afb-119">Gibt an, dass das Cmdlet warten muss, bis der Vorgang abgeschlossen ist, bevor Sie zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="97afb-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="97afb-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="97afb-120">-Confirm</span></span>
<span data-ttu-id="97afb-121">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="97afb-121">Specify if confirmation is required.</span></span> <span data-ttu-id="97afb-122">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="97afb-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="97afb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97afb-123">-WhatIf</span></span>
<span data-ttu-id="97afb-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="97afb-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="97afb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97afb-125">CommonParameters</span></span>
<span data-ttu-id="97afb-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97afb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97afb-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97afb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97afb-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97afb-128">INPUTS</span></span>

### <span data-ttu-id="97afb-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="97afb-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="97afb-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97afb-130">OUTPUTS</span></span>

### <span data-ttu-id="97afb-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="97afb-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="97afb-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="97afb-132">NOTES</span></span>

## <span data-ttu-id="97afb-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97afb-133">RELATED LINKS</span></span>

[<span data-ttu-id="97afb-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="97afb-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="97afb-135">Neu – AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="97afb-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="97afb-136">Satz-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="97afb-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
