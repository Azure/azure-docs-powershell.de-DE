---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 4f926b88214a60cc05b6eb9666e10fa8ed7bf3ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825204"
---
# <span data-ttu-id="8c248-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="8c248-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="8c248-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c248-102">SYNOPSIS</span></span>
<span data-ttu-id="8c248-103">Wechseln Sie die Replikation von einem Prozess Server zu einem anderen für den Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="8c248-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="8c248-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c248-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c248-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c248-105">DESCRIPTION</span></span>
<span data-ttu-id="8c248-106">Die **Start-AzRecoveryServicesAsrSwitchProcessServerJob** wechselt die Verschiebung der Replikationsdaten für die angegebenen virtuellen Computer oder einen angegebenen Prozess Server auf den angegebenen Zielprozess Server.</span><span class="sxs-lookup"><span data-stu-id="8c248-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="8c248-107">Wird zum Lastenausgleich oder zum Wechseln der Replikation zwischen Prozess Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c248-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="8c248-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c248-108">EXAMPLES</span></span>

### <span data-ttu-id="8c248-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c248-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="8c248-110">Auftrag zum Nachvollziehen des Umschaltens des Prozess Servers für alle durch die Replikation geschützten Elemente von der Quelle zum Zielprozess Server</span><span class="sxs-lookup"><span data-stu-id="8c248-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="8c248-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8c248-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="8c248-112">Job zum Nachvollziehen des wechselnden Prozess Servers für übergebenes Replikations geschütztes Element von der Quelle zum Zielprozess Server.</span><span class="sxs-lookup"><span data-stu-id="8c248-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="8c248-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c248-113">PARAMETERS</span></span>

### <span data-ttu-id="8c248-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c248-114">-DefaultProfile</span></span>
<span data-ttu-id="8c248-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c248-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c248-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="8c248-116">-Fabric</span></span>
<span data-ttu-id="8c248-117">Fabric für die Websitewiederherstellung, die dem Konfigurations Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="8c248-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c248-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8c248-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8c248-119">Liste des Replikations geschützten Elements, dessen Prozess Server gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c248-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c248-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="8c248-120">-SourceProcessServer</span></span>
<span data-ttu-id="8c248-121">Der Prozess Server, aus dem die Replikation gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c248-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c248-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="8c248-122">-TargetProcessServer</span></span>
<span data-ttu-id="8c248-123">Der Prozess Server, in den die Replikation gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c248-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c248-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c248-124">-Confirm</span></span>
<span data-ttu-id="8c248-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c248-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c248-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c248-126">-WhatIf</span></span>
<span data-ttu-id="8c248-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c248-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c248-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c248-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c248-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c248-129">CommonParameters</span></span>
<span data-ttu-id="8c248-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c248-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c248-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c248-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c248-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c248-132">INPUTS</span></span>

### <span data-ttu-id="8c248-133">Keine</span><span class="sxs-lookup"><span data-stu-id="8c248-133">None</span></span>

## <span data-ttu-id="8c248-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c248-134">OUTPUTS</span></span>

### <span data-ttu-id="8c248-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8c248-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8c248-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c248-136">NOTES</span></span>

## <span data-ttu-id="8c248-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c248-137">RELATED LINKS</span></span>
