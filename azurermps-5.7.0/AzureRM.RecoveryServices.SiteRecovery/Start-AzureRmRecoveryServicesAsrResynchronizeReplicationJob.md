---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 9c336602aebdb82e4860ee744fb99f3a6fbf5a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478294"
---
# <span data-ttu-id="33f92-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="33f92-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="33f92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33f92-102">SYNOPSIS</span></span>
<span data-ttu-id="33f92-103">Startet die erneute Synchronisierung der Replikation.</span><span class="sxs-lookup"><span data-stu-id="33f92-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33f92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33f92-104">SYNTAX</span></span>

### <span data-ttu-id="33f92-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="33f92-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33f92-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33f92-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33f92-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33f92-107">DESCRIPTION</span></span>
<span data-ttu-id="33f92-108">Das **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob-** Cmdlet startet die erneute Synchronisierung der Replikation für das angegebene geschützte Element, wenn der geschützte Zustand für die erneute Synchronisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="33f92-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="33f92-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33f92-109">EXAMPLES</span></span>

### <span data-ttu-id="33f92-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33f92-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="33f92-111">Startet den Auftrag, um die Replikation beim übergebenen Replikations geschützten Element erneut zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="33f92-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="33f92-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="33f92-112">PARAMETERS</span></span>

### <span data-ttu-id="33f92-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="33f92-113">-Confirm</span></span>
<span data-ttu-id="33f92-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="33f92-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33f92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f92-115">-DefaultProfile</span></span>
<span data-ttu-id="33f92-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33f92-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33f92-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="33f92-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="33f92-118">Geschütztes Element für ASR-Replikation, für das die Replikation erneut synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="33f92-118">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33f92-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="33f92-119">-ResourceId</span></span>
<span data-ttu-id="33f92-120">Die Ressourcen-ID des Replikations geschützten Elements, das erneut synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="33f92-120">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33f92-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f92-121">-WhatIf</span></span>
<span data-ttu-id="33f92-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33f92-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33f92-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33f92-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33f92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f92-124">CommonParameters</span></span>
<span data-ttu-id="33f92-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f92-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f92-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f92-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33f92-127">INPUTS</span></span>

### <span data-ttu-id="33f92-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="33f92-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="33f92-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33f92-129">OUTPUTS</span></span>

### <span data-ttu-id="33f92-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="33f92-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="33f92-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="33f92-131">NOTES</span></span>

## <span data-ttu-id="33f92-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33f92-132">RELATED LINKS</span></span>
