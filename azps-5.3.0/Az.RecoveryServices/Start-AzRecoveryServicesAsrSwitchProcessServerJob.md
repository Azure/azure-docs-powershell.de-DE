---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468628"
---
# <span data-ttu-id="8c63a-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="8c63a-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="8c63a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c63a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c63a-103">Wechseln der Replikation von einem Prozessserver zu einem anderen zum Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="8c63a-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="8c63a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c63a-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c63a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c63a-105">DESCRIPTION</span></span>
<span data-ttu-id="8c63a-106">**Der Start-AzRecoveryServicesAsrSwitchProcessServerJob** schaltet die Replikationsdatenbewegung für die angegebenen virtuellen Computer oder einen angegebenen Prozessserver auf den angegebenen Zielprozessserver um.</span><span class="sxs-lookup"><span data-stu-id="8c63a-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="8c63a-107">Wird für den Lastenausgleich oder das Wechseln der Replikation zwischen Prozessservern verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c63a-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="8c63a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c63a-108">EXAMPLES</span></span>

### <span data-ttu-id="8c63a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c63a-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="8c63a-110">Stellen Sie die Aufgabe zum Nachverfolgen des Wechselprozessservers für alle replikationsgeschützten Elemente von der Quelle zum Zielprozessserver.</span><span class="sxs-lookup"><span data-stu-id="8c63a-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="8c63a-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8c63a-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="8c63a-112">Aufgabe zum Nachverfolgen des Wechselprozessservers für das übergebene replikationsgeschützte Element von der Quelle zum Zielprozessserver.</span><span class="sxs-lookup"><span data-stu-id="8c63a-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="8c63a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c63a-113">PARAMETERS</span></span>

### <span data-ttu-id="8c63a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c63a-114">-DefaultProfile</span></span>
<span data-ttu-id="8c63a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c63a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c63a-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="8c63a-116">-Fabric</span></span>
<span data-ttu-id="8c63a-117">Site recovery fabric corresponding to the Configuration Server.</span><span class="sxs-lookup"><span data-stu-id="8c63a-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="8c63a-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8c63a-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8c63a-119">Liste des replikationsgeschützten Elements, dessen Prozessserver gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c63a-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="8c63a-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="8c63a-120">-SourceProcessServer</span></span>
<span data-ttu-id="8c63a-121">Der Prozessserver, von dem die Replikation entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c63a-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="8c63a-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="8c63a-122">-TargetProcessServer</span></span>
<span data-ttu-id="8c63a-123">Der Prozessserver, auf den die Replikation umschalten soll.</span><span class="sxs-lookup"><span data-stu-id="8c63a-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="8c63a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c63a-124">-Confirm</span></span>
<span data-ttu-id="8c63a-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c63a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c63a-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8c63a-126">-WhatIf</span></span>
<span data-ttu-id="8c63a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c63a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c63a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c63a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c63a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c63a-129">CommonParameters</span></span>
<span data-ttu-id="8c63a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c63a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c63a-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c63a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c63a-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c63a-132">INPUTS</span></span>

### <span data-ttu-id="8c63a-133">Keine</span><span class="sxs-lookup"><span data-stu-id="8c63a-133">None</span></span>

## <span data-ttu-id="8c63a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c63a-134">OUTPUTS</span></span>

### <span data-ttu-id="8c63a-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8c63a-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8c63a-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8c63a-136">NOTES</span></span>

## <span data-ttu-id="8c63a-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8c63a-137">RELATED LINKS</span></span>
