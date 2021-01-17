---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359917"
---
# <span data-ttu-id="ed9fe-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ed9fe-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ed9fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9fe-103">Erstellt eine neue Azure NetApp Files (ANF)-Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="ed9fe-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="ed9fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed9fe-104">SYNTAX</span></span>

### <span data-ttu-id="ed9fe-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed9fe-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed9fe-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed9fe-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed9fe-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed9fe-107">DESCRIPTION</span></span>
<span data-ttu-id="ed9fe-108">Das **Cmdlet "New-AzNetAppFilesSnapshot"** erstellt eine ANF-Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="ed9fe-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="ed9fe-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed9fe-109">EXAMPLES</span></span>

### <span data-ttu-id="ed9fe-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed9fe-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="ed9fe-111">Mit diesem Befehl wird die neue ANF-Momentaufnahme "MyAnfSnapshot" im Volumen "MyAnfVolume" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed9fe-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="ed9fe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed9fe-112">PARAMETERS</span></span>

### <span data-ttu-id="ed9fe-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed9fe-113">-AccountName</span></span>
<span data-ttu-id="ed9fe-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="ed9fe-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9fe-115">-DefaultProfile</span></span>
<span data-ttu-id="ed9fe-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed9fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed9fe-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="ed9fe-117">-FileSystemId</span></span>
<span data-ttu-id="ed9fe-118">Die Dateisystem-ID</span><span class="sxs-lookup"><span data-stu-id="ed9fe-118">The file system id</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ed9fe-119">-Location</span></span>
<span data-ttu-id="ed9fe-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="ed9fe-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ed9fe-121">-Name</span></span>
<span data-ttu-id="ed9fe-122">Der Name der ANF-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="ed9fe-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ed9fe-123">-PoolName</span></span>
<span data-ttu-id="ed9fe-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="ed9fe-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9fe-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed9fe-126">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="ed9fe-126">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed9fe-127">-Tag</span></span>
<span data-ttu-id="ed9fe-128">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="ed9fe-128">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="ed9fe-129">-VolumeName</span></span>
<span data-ttu-id="ed9fe-130">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="ed9fe-130">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="ed9fe-131">-VolumeObject</span></span>
<span data-ttu-id="ed9fe-132">Das Volumen für das neue Momentaufnahmeobjekt</span><span class="sxs-lookup"><span data-stu-id="ed9fe-132">The volume for the new snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fe-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed9fe-133">-Confirm</span></span>
<span data-ttu-id="ed9fe-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed9fe-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed9fe-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed9fe-135">-WhatIf</span></span>
<span data-ttu-id="ed9fe-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed9fe-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed9fe-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed9fe-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed9fe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9fe-138">CommonParameters</span></span>
<span data-ttu-id="ed9fe-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed9fe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9fe-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed9fe-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9fe-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed9fe-141">INPUTS</span></span>

### <span data-ttu-id="ed9fe-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ed9fe-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ed9fe-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed9fe-143">OUTPUTS</span></span>

### <span data-ttu-id="ed9fe-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ed9fe-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ed9fe-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed9fe-145">NOTES</span></span>

## <span data-ttu-id="ed9fe-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed9fe-146">RELATED LINKS</span></span>
