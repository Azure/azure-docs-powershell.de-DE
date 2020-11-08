---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: c3fd190fb033a685bcb0d5087c544298681e47c5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006936"
---
# <span data-ttu-id="fcd8b-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="fcd8b-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="fcd8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcd8b-102">SYNOPSIS</span></span>


## <span data-ttu-id="fcd8b-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcd8b-103">SYNTAX</span></span>

### <span data-ttu-id="fcd8b-104">Lautstärke (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcd8b-104">Volume (Default)</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetScaleUnit <String> -TargetVolumeLabel <String> -Disks <IDisk[]>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd8b-105">Freigeben</span><span class="sxs-lookup"><span data-stu-id="fcd8b-105">Share</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetShare <String> -Disks <IDisk[]> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fcd8b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcd8b-106">DESCRIPTION</span></span>


## <span data-ttu-id="fcd8b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcd8b-107">EXAMPLES</span></span>

### <span data-ttu-id="fcd8b-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="fcd8b-108">Example 1:</span></span>
```powershell
PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

CreationTime : 2/26/2020 10:56:32 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestJob1
Location     : redmond
MigrationId  : TestJob1
Name         : redmond/TestJob1
StartTime    : 
Status       : Pending
Subtask      : {53ee3665-00e4-4c69-a067-524058905ead, d551734f-0370-4851-9704-c7cec80b34c5}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_2
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="fcd8b-109">Erstellen Sie einen Datenträger Migrationsauftrag zum Migrieren von Datenträgern zur Ziel Skalierungseinheit und-Lautstärke.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-109">Create a disk migration job to migrate disks to the target scale unit and volume.</span></span>

### <span data-ttu-id="fcd8b-110">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="fcd8b-110">Example 2:</span></span> 
```powershell
PS C:\> PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob2 -TargetShare \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3 -Disks $disks
WARNING: TargetShare parameter will be deprecated in a future release, please use Volume instead.

CreationTime : 2/26/2020 11:02:48 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob2
Location     : redmond
MigrationId  : TestJob2
Name         : redmond/TestJob2
StartTime    : 
Status       : Pending
Subtask      : {0cfd8d29-1ca4-42db-a490-9198814abc50, 89c9b15e-47c6-4321-a390-611fc190cfad}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

```

<span data-ttu-id="fcd8b-111">Erstellen Sie einen Datenträger Migrationsauftrag zum Migrieren von Datenträgern zur Zielfreigabe.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-111">Create a disk migration job to migrate disks to the target share.</span></span>

## <span data-ttu-id="fcd8b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcd8b-112">PARAMETERS</span></span>

### <span data-ttu-id="fcd8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd8b-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcd8b-114">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="fcd8b-114">-Disks</span></span>
<span data-ttu-id="fcd8b-115">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Datenträgereigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-115">To construct, see NOTES section for DISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fcd8b-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="fcd8b-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcd8b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fcd8b-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcd8b-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fcd8b-118">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcd8b-119">-TargetScaleUnit</span><span class="sxs-lookup"><span data-stu-id="fcd8b-119">-TargetScaleUnit</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcd8b-120">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="fcd8b-120">-TargetShare</span></span>


```yaml
Type: System.String
Parameter Sets: Share
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcd8b-121">-TargetVolumeLabel</span><span class="sxs-lookup"><span data-stu-id="fcd8b-121">-TargetVolumeLabel</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcd8b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcd8b-122">-Confirm</span></span>
<span data-ttu-id="fcd8b-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcd8b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd8b-124">-WhatIf</span></span>
<span data-ttu-id="fcd8b-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcd8b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcd8b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd8b-127">CommonParameters</span></span>
<span data-ttu-id="fcd8b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd8b-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcd8b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd8b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcd8b-130">INPUTS</span></span>

### <span data-ttu-id="fcd8b-131">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. iDisk []</span><span class="sxs-lookup"><span data-stu-id="fcd8b-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]</span></span>

## <span data-ttu-id="fcd8b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcd8b-132">OUTPUTS</span></span>

### <span data-ttu-id="fcd8b-133">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="fcd8b-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



### <span data-ttu-id="fcd8b-134">Start-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="fcd8b-134">Start-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="fcd8b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcd8b-135">NOTES</span></span>

<span data-ttu-id="fcd8b-136">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fcd8b-137">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fcd8b-138">Datenträger <iDisk [] >:</span><span class="sxs-lookup"><span data-stu-id="fcd8b-138">DISKS <IDisk[]>:</span></span> 
  - <span data-ttu-id="fcd8b-139">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-139">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="fcd8b-140">`[DiskId <String>]`: Die Datenträger-ID.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-140">`[DiskId <String>]`: The disk id.</span></span>
  - <span data-ttu-id="fcd8b-141">`[SharePath <String>]`: Der Datenträgerfreigabe Pfad.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-141">`[SharePath <String>]`: The disk share path.</span></span>
  - <span data-ttu-id="fcd8b-142">`[Status <DiskState?>]`: Der Datenträgerstatus.</span><span class="sxs-lookup"><span data-stu-id="fcd8b-142">`[Status <DiskState?>]`: The disk status.</span></span>

## <span data-ttu-id="fcd8b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcd8b-143">RELATED LINKS</span></span>

