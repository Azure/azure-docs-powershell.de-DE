---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178239"
---
# <span data-ttu-id="5aa82-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="5aa82-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="5aa82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5aa82-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa82-103">Entfernt Datenträger zum Replikations geschützten Element.</span><span class="sxs-lookup"><span data-stu-id="5aa82-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="5aa82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aa82-104">SYNTAX</span></span>

### <span data-ttu-id="5aa82-105">AzureToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="5aa82-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5aa82-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="5aa82-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5aa82-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5aa82-107">DESCRIPTION</span></span>
<span data-ttu-id="5aa82-108">Das Cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** entfernt den Datenträger aus dem geschützten Element der ASR-Replikation.</span><span class="sxs-lookup"><span data-stu-id="5aa82-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="5aa82-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5aa82-109">EXAMPLES</span></span>

### <span data-ttu-id="5aa82-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5aa82-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="5aa82-111">Starten Sie den Vorgang, um den angegebenen Datenträger aus dem Schutz-VM für nicht verwalteten Datenträger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5aa82-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="5aa82-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5aa82-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="5aa82-113">Starten Sie den Vorgang, um den angegebenen Datenträger aus dem Schutz VM für verwalteten Datenträger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5aa82-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="5aa82-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5aa82-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="5aa82-115">Startet den Vorgang, um den angegebenen Datenträger zu entfernen, und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des geschützten Datenträger Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5aa82-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="5aa82-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aa82-116">PARAMETERS</span></span>

### <span data-ttu-id="5aa82-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5aa82-117">-Confirm</span></span>
<span data-ttu-id="5aa82-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5aa82-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aa82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa82-119">-DefaultProfile</span></span>
<span data-ttu-id="5aa82-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5aa82-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aa82-121">-Datenträger-Nr</span><span class="sxs-lookup"><span data-stu-id="5aa82-121">-DiskId</span></span>
<span data-ttu-id="5aa82-122">Gibt die Liste der verwalteten Datenträger-IDs an.</span><span class="sxs-lookup"><span data-stu-id="5aa82-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="5aa82-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5aa82-123">-InputObject</span></span>
<span data-ttu-id="5aa82-124">Das Eingabeobjekt für das Cmdlet: das Objekt der ASR-Replikations geschützten Elemente, das dem zu entfernenden Datenträger entspricht.</span><span class="sxs-lookup"><span data-stu-id="5aa82-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="5aa82-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="5aa82-125">-VhdUri</span></span>
<span data-ttu-id="5aa82-126">Gibt die Liste der VHD-URIs an.</span><span class="sxs-lookup"><span data-stu-id="5aa82-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="5aa82-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5aa82-127">-WaitForCompletion</span></span>
<span data-ttu-id="5aa82-128">Auf Abschluss warten</span><span class="sxs-lookup"><span data-stu-id="5aa82-128">Wait For Completion</span></span>

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

### <span data-ttu-id="5aa82-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aa82-129">-WhatIf</span></span>
<span data-ttu-id="5aa82-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5aa82-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa82-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5aa82-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aa82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa82-132">CommonParameters</span></span>
<span data-ttu-id="5aa82-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aa82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa82-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5aa82-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa82-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5aa82-135">INPUTS</span></span>

### <span data-ttu-id="5aa82-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5aa82-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5aa82-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5aa82-137">OUTPUTS</span></span>

### <span data-ttu-id="5aa82-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5aa82-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5aa82-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="5aa82-139">NOTES</span></span>

## <span data-ttu-id="5aa82-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5aa82-140">RELATED LINKS</span></span>
