---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291862"
---
# <span data-ttu-id="a3905-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="a3905-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="a3905-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3905-102">SYNOPSIS</span></span>
<span data-ttu-id="a3905-103">Startet die erneute Synchronisierung der Replikation.</span><span class="sxs-lookup"><span data-stu-id="a3905-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="a3905-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3905-104">SYNTAX</span></span>

### <span data-ttu-id="a3905-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3905-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3905-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3905-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3905-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3905-107">DESCRIPTION</span></span>
<span data-ttu-id="a3905-108">Das **Cmdlet "Start-AzRecoveryServicesAsrResynchronizeReplicationJob"** startet die Resynchronisierung der Replikation für das angegebene geschützte Element, wenn sich der geschützte Zustand im erforderlichen Zustand der Resynchronisierung befindet.</span><span class="sxs-lookup"><span data-stu-id="a3905-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="a3905-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3905-109">EXAMPLES</span></span>

### <span data-ttu-id="a3905-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3905-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="a3905-111">Startet den Auftrag zum erneuten Synchronisierungsreplikation für übergebene, replikationsgeschützte Elemente.</span><span class="sxs-lookup"><span data-stu-id="a3905-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="a3905-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3905-112">PARAMETERS</span></span>

### <span data-ttu-id="a3905-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3905-113">-DefaultProfile</span></span>
<span data-ttu-id="a3905-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3905-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3905-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a3905-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a3905-116">AsR replication protected item to resynchronize replication for.</span><span class="sxs-lookup"><span data-stu-id="a3905-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3905-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3905-117">-ResourceId</span></span>
<span data-ttu-id="a3905-118">Ressourcen-ID des replikationsgeschützten Elements zum Resynchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a3905-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3905-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3905-119">-Confirm</span></span>
<span data-ttu-id="a3905-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3905-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3905-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a3905-121">-WhatIf</span></span>
<span data-ttu-id="a3905-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3905-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3905-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3905-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3905-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3905-124">CommonParameters</span></span>
<span data-ttu-id="a3905-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3905-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3905-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3905-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3905-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3905-127">INPUTS</span></span>

### <span data-ttu-id="a3905-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a3905-128">System.String</span></span>

### <span data-ttu-id="a3905-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a3905-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a3905-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3905-130">OUTPUTS</span></span>

### <span data-ttu-id="a3905-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a3905-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a3905-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3905-132">NOTES</span></span>

## <span data-ttu-id="a3905-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3905-133">RELATED LINKS</span></span>
