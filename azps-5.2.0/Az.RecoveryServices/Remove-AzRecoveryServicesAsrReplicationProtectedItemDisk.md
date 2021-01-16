---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295685"
---
# <span data-ttu-id="a6d44-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="a6d44-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="a6d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6d44-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d44-103">Entfernt Datenträger für replikationsgeschützte Elemente.</span><span class="sxs-lookup"><span data-stu-id="a6d44-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="a6d44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6d44-104">SYNTAX</span></span>

### <span data-ttu-id="a6d44-105">AzureToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6d44-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6d44-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a6d44-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6d44-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6d44-107">DESCRIPTION</span></span>
<span data-ttu-id="a6d44-108">Das **Cmdlet "Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk"** entfernt den Datenträger aus dem geschützten ASR-Replikationselement.</span><span class="sxs-lookup"><span data-stu-id="a6d44-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="a6d44-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6d44-109">EXAMPLES</span></span>

### <span data-ttu-id="a6d44-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6d44-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="a6d44-111">Starten Sie den Vorgang zum Entfernen eines angegebenen Datenträgers von der Schutz-VM für nicht verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a6d44-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="a6d44-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a6d44-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="a6d44-113">Starten Sie den Vorgang zum Entfernen eines angegebenen Datenträgers von der Schutz-VM für verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a6d44-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="a6d44-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a6d44-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="a6d44-115">Startet den Vorgang zum Entfernen des angegebenen Datenträgers und gibt den ASR-Auftrag zurück, mit dem der Vorgang zum Entfernen des geschützten Datenträgers nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="a6d44-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="a6d44-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6d44-116">PARAMETERS</span></span>

### <span data-ttu-id="a6d44-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6d44-117">-Confirm</span></span>
<span data-ttu-id="a6d44-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6d44-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6d44-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d44-119">-DefaultProfile</span></span>
<span data-ttu-id="a6d44-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6d44-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d44-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="a6d44-121">-DiskId</span></span>
<span data-ttu-id="a6d44-122">Gibt die Liste der verwalteten Datenträger-IDs an.</span><span class="sxs-lookup"><span data-stu-id="a6d44-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d44-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6d44-123">-InputObject</span></span>
<span data-ttu-id="a6d44-124">Das Eingabeobjekt für das Cmdlet: Das asR-replikationsgeschützte Elementobjekt, das dem Datenträger entspricht, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6d44-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d44-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="a6d44-125">-VhdUri</span></span>
<span data-ttu-id="a6d44-126">Gibt die Liste der vhd-URIs an.</span><span class="sxs-lookup"><span data-stu-id="a6d44-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d44-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a6d44-127">-WaitForCompletion</span></span>
<span data-ttu-id="a6d44-128">Warten auf den Abschluss</span><span class="sxs-lookup"><span data-stu-id="a6d44-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d44-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a6d44-129">-WhatIf</span></span>
<span data-ttu-id="a6d44-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6d44-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6d44-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6d44-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6d44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d44-132">CommonParameters</span></span>
<span data-ttu-id="a6d44-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6d44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d44-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6d44-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d44-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6d44-135">INPUTS</span></span>

### <span data-ttu-id="a6d44-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a6d44-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a6d44-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6d44-137">OUTPUTS</span></span>

### <span data-ttu-id="a6d44-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a6d44-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a6d44-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a6d44-139">NOTES</span></span>

## <span data-ttu-id="a6d44-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a6d44-140">RELATED LINKS</span></span>
