---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 48a17c0b2bd8c1d62de1b3ebd5eccc5171d65837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659807"
---
# <span data-ttu-id="cee93-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="cee93-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="cee93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cee93-102">SYNOPSIS</span></span>
<span data-ttu-id="cee93-103">Startet die erneute Synchronisierung der Replikation.</span><span class="sxs-lookup"><span data-stu-id="cee93-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="cee93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cee93-104">SYNTAX</span></span>

### <span data-ttu-id="cee93-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="cee93-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee93-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cee93-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee93-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cee93-107">DESCRIPTION</span></span>
<span data-ttu-id="cee93-108">Das **Start-AzRecoveryServicesAsrResynchronizeReplicationJob-** Cmdlet startet die erneute Synchronisierung der Replikation für das angegebene geschützte Element, wenn der geschützte Zustand für die erneute Synchronisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cee93-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="cee93-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cee93-109">EXAMPLES</span></span>

### <span data-ttu-id="cee93-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cee93-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="cee93-111">Startet den Auftrag, um die Replikation beim übergebenen Replikations geschützten Element erneut zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="cee93-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="cee93-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cee93-112">PARAMETERS</span></span>

### <span data-ttu-id="cee93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee93-113">-DefaultProfile</span></span>
<span data-ttu-id="cee93-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cee93-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cee93-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cee93-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="cee93-116">Geschütztes Element für ASR-Replikation, für das die Replikation erneut synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cee93-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="cee93-117">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cee93-117">-ResourceId</span></span>
<span data-ttu-id="cee93-118">Die Ressourcen-ID des Replikations geschützten Elements, das erneut synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cee93-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="cee93-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cee93-119">-Confirm</span></span>
<span data-ttu-id="cee93-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cee93-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cee93-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee93-121">-WhatIf</span></span>
<span data-ttu-id="cee93-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cee93-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cee93-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cee93-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cee93-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee93-124">CommonParameters</span></span>
<span data-ttu-id="cee93-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee93-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee93-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee93-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee93-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cee93-127">INPUTS</span></span>

### <span data-ttu-id="cee93-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cee93-128">System.String</span></span>

### <span data-ttu-id="cee93-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cee93-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="cee93-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cee93-130">OUTPUTS</span></span>

### <span data-ttu-id="cee93-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cee93-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cee93-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="cee93-132">NOTES</span></span>

## <span data-ttu-id="cee93-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cee93-133">RELATED LINKS</span></span>
