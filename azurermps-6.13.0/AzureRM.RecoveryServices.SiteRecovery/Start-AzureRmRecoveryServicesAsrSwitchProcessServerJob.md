---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 49e775fcb4dce90989bb03673319a8cd1bd1683a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477778"
---
# <span data-ttu-id="79484-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="79484-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="79484-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79484-102">SYNOPSIS</span></span>
<span data-ttu-id="79484-103">Wechseln Sie die Replikation von einem Prozess Server zu einem anderen für den Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="79484-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79484-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79484-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79484-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79484-105">DESCRIPTION</span></span>
<span data-ttu-id="79484-106">Die **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** wechselt die Verschiebung der Replikationsdaten für die angegebenen virtuellen Computer oder einen angegebenen Prozess Server auf den angegebenen Zielprozess Server.</span><span class="sxs-lookup"><span data-stu-id="79484-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="79484-107">Wird zum Lastenausgleich oder zum Wechseln der Replikation zwischen Prozess Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="79484-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="79484-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79484-108">EXAMPLES</span></span>

### <span data-ttu-id="79484-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79484-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="79484-110">Auftrag zum Nachvollziehen des Umschaltens des Prozess Servers für alle durch die Replikation geschützten Elemente von der Quelle zum Zielprozess Server</span><span class="sxs-lookup"><span data-stu-id="79484-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="79484-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79484-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="79484-112">Job zum Nachvollziehen des wechselnden Prozess Servers für übergebenes Replikations geschütztes Element von der Quelle zum Zielprozess Server.</span><span class="sxs-lookup"><span data-stu-id="79484-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="79484-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="79484-113">PARAMETERS</span></span>

### <span data-ttu-id="79484-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79484-114">-DefaultProfile</span></span>
<span data-ttu-id="79484-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79484-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79484-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="79484-116">-Fabric</span></span>
<span data-ttu-id="79484-117">Fabric für die Websitewiederherstellung, die dem Konfigurations Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="79484-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="79484-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="79484-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="79484-119">Liste des Replikations geschützten Elements, dessen Prozess Server gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="79484-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="79484-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="79484-120">-SourceProcessServer</span></span>
<span data-ttu-id="79484-121">Der Prozess Server, aus dem die Replikation gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="79484-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="79484-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="79484-122">-TargetProcessServer</span></span>
<span data-ttu-id="79484-123">Der Prozess Server, in den die Replikation gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="79484-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="79484-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79484-124">-Confirm</span></span>
<span data-ttu-id="79484-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79484-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79484-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79484-126">-WhatIf</span></span>
<span data-ttu-id="79484-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79484-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79484-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79484-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79484-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79484-129">CommonParameters</span></span>
<span data-ttu-id="79484-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79484-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79484-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79484-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79484-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79484-132">INPUTS</span></span>

### <span data-ttu-id="79484-133">Keine</span><span class="sxs-lookup"><span data-stu-id="79484-133">None</span></span>

## <span data-ttu-id="79484-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79484-134">OUTPUTS</span></span>

### <span data-ttu-id="79484-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="79484-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="79484-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="79484-136">NOTES</span></span>

## <span data-ttu-id="79484-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79484-137">RELATED LINKS</span></span>
