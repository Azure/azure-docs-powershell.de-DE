---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459736"
---
# <span data-ttu-id="db78e-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="db78e-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="db78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db78e-102">SYNOPSIS</span></span>
<span data-ttu-id="db78e-103">Fügen Sie den Datenträger zum Schutz für den bereits geschützten virtuellen Azure-Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="db78e-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="db78e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db78e-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db78e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db78e-105">DESCRIPTION</span></span>
<span data-ttu-id="db78e-106">Das **Cmdlet "Add-AzRecoveryServicesAsrReplicationProtectedItemDisk"** fügt den Datenträger zum Schutz für den bereits geschützten virtuellen Azure-Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="db78e-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="db78e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db78e-107">EXAMPLES</span></span>

### <span data-ttu-id="db78e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db78e-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="db78e-109">Starten Sie den Vorgang, um die angegebene Datenträgerkonfiguration zu Ihrem Schutz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="db78e-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="db78e-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="db78e-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="db78e-111">Starten Sie den Vorgang, um die angegebene Datenträgerkonfiguration zu Ihrem Schutz hinzuzufügen. Durch die Pipette geschütztes Element für die Eingabereplikation.</span><span class="sxs-lookup"><span data-stu-id="db78e-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="db78e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db78e-112">PARAMETERS</span></span>

### <span data-ttu-id="db78e-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="db78e-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="db78e-114">Gibt die Datenträgerkonfiguration an, die für den Datenträgerschutz für das Notfallwiederherstellungsszenario von Azure zu Azure verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db78e-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db78e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db78e-115">-DefaultProfile</span></span>
<span data-ttu-id="db78e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db78e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db78e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db78e-117">-InputObject</span></span>
<span data-ttu-id="db78e-118">Das Eingabeobjekt für das Cmdlet: Das asR-replikationsgeschützte Elementobjekt, das dem neuen Datenträger entspricht, der geschützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="db78e-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="db78e-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="db78e-119">-WaitForCompletion</span></span>
<span data-ttu-id="db78e-120">Warten auf den Abschluss</span><span class="sxs-lookup"><span data-stu-id="db78e-120">Wait For Completion</span></span>

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

### <span data-ttu-id="db78e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db78e-121">-Confirm</span></span>
<span data-ttu-id="db78e-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db78e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db78e-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="db78e-123">-WhatIf</span></span>
<span data-ttu-id="db78e-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db78e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db78e-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db78e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db78e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db78e-126">CommonParameters</span></span>
<span data-ttu-id="db78e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db78e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db78e-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db78e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db78e-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db78e-129">INPUTS</span></span>

### <span data-ttu-id="db78e-130">Keine</span><span class="sxs-lookup"><span data-stu-id="db78e-130">None</span></span>

## <span data-ttu-id="db78e-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db78e-131">OUTPUTS</span></span>

### <span data-ttu-id="db78e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="db78e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="db78e-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="db78e-133">NOTES</span></span>

## <span data-ttu-id="db78e-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="db78e-134">RELATED LINKS</span></span>
