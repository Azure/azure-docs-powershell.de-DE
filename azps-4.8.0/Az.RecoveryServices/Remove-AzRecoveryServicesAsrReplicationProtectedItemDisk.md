---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166884"
---
# <span data-ttu-id="71cc7-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="71cc7-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="71cc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="71cc7-103">Entfernt Datenträger zum Replikations geschützten Element.</span><span class="sxs-lookup"><span data-stu-id="71cc7-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="71cc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71cc7-104">SYNTAX</span></span>

### <span data-ttu-id="71cc7-105">AzureToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="71cc7-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71cc7-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="71cc7-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71cc7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71cc7-107">DESCRIPTION</span></span>
<span data-ttu-id="71cc7-108">Das Cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** entfernt den Datenträger aus dem geschützten Element der ASR-Replikation.</span><span class="sxs-lookup"><span data-stu-id="71cc7-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="71cc7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71cc7-109">EXAMPLES</span></span>

### <span data-ttu-id="71cc7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71cc7-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="71cc7-111">Starten Sie den Vorgang, um den angegebenen Datenträger aus dem Schutz-VM für nicht verwalteten Datenträger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="71cc7-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="71cc7-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="71cc7-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="71cc7-113">Starten Sie den Vorgang, um den angegebenen Datenträger aus dem Schutz VM für verwalteten Datenträger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="71cc7-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="71cc7-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="71cc7-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="71cc7-115">Startet den Vorgang, um den angegebenen Datenträger zu entfernen, und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des geschützten Datenträger Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71cc7-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="71cc7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="71cc7-116">PARAMETERS</span></span>

### <span data-ttu-id="71cc7-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71cc7-117">-Confirm</span></span>
<span data-ttu-id="71cc7-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71cc7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71cc7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cc7-119">-DefaultProfile</span></span>
<span data-ttu-id="71cc7-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71cc7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71cc7-121">-Datenträger-Nr</span><span class="sxs-lookup"><span data-stu-id="71cc7-121">-DiskId</span></span>
<span data-ttu-id="71cc7-122">Gibt die Liste der verwalteten Datenträger-IDs an.</span><span class="sxs-lookup"><span data-stu-id="71cc7-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="71cc7-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="71cc7-123">-InputObject</span></span>
<span data-ttu-id="71cc7-124">Das Eingabeobjekt für das Cmdlet: das Objekt der ASR-Replikations geschützten Elemente, das dem zu entfernenden Datenträger entspricht.</span><span class="sxs-lookup"><span data-stu-id="71cc7-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="71cc7-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="71cc7-125">-VhdUri</span></span>
<span data-ttu-id="71cc7-126">Gibt die Liste der VHD-URIs an.</span><span class="sxs-lookup"><span data-stu-id="71cc7-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="71cc7-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="71cc7-127">-WaitForCompletion</span></span>
<span data-ttu-id="71cc7-128">Auf Abschluss warten</span><span class="sxs-lookup"><span data-stu-id="71cc7-128">Wait For Completion</span></span>

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

### <span data-ttu-id="71cc7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71cc7-129">-WhatIf</span></span>
<span data-ttu-id="71cc7-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71cc7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71cc7-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71cc7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71cc7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cc7-132">CommonParameters</span></span>
<span data-ttu-id="71cc7-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71cc7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cc7-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71cc7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cc7-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71cc7-135">INPUTS</span></span>

### <span data-ttu-id="71cc7-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71cc7-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="71cc7-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71cc7-137">OUTPUTS</span></span>

### <span data-ttu-id="71cc7-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="71cc7-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71cc7-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="71cc7-139">NOTES</span></span>

## <span data-ttu-id="71cc7-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71cc7-140">RELATED LINKS</span></span>
