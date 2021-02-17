---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159284"
---
# <span data-ttu-id="aad2d-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="aad2d-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="aad2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad2d-102">SYNOPSIS</span></span>
<span data-ttu-id="aad2d-103">Löscht eine Azure NetApp Files (ANF)-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="aad2d-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="aad2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aad2d-104">SYNTAX</span></span>

### <span data-ttu-id="aad2d-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aad2d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad2d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aad2d-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad2d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aad2d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad2d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aad2d-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad2d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aad2d-109">DESCRIPTION</span></span>
<span data-ttu-id="aad2d-110">Das **Cmdlet "Remove-AzNetAppFilesBackup"** löscht ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="aad2d-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="aad2d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aad2d-111">EXAMPLES</span></span>

### <span data-ttu-id="aad2d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aad2d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="aad2d-113">Mit diesem Befehl wird die neue ANF-Sicherung mit dem Namen "MyBackup" für "MyVolume" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="aad2d-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="aad2d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aad2d-114">PARAMETERS</span></span>

### <span data-ttu-id="aad2d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aad2d-115">-AccountName</span></span>
<span data-ttu-id="aad2d-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="aad2d-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="aad2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad2d-117">-DefaultProfile</span></span>
<span data-ttu-id="aad2d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aad2d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aad2d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aad2d-119">-InputObject</span></span>
<span data-ttu-id="aad2d-120">Das zu entfernende Momentaufnahmeobjekt</span><span class="sxs-lookup"><span data-stu-id="aad2d-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aad2d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="aad2d-121">-Name</span></span>
<span data-ttu-id="aad2d-122">Der Name der ANF-Sicherung</span><span class="sxs-lookup"><span data-stu-id="aad2d-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad2d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aad2d-123">-PassThru</span></span>
<span data-ttu-id="aad2d-124">Zurückgeben, ob die angegebene Sicherung erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="aad2d-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="aad2d-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="aad2d-125">-PoolName</span></span>
<span data-ttu-id="aad2d-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="aad2d-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="aad2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="aad2d-128">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="aad2d-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="aad2d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aad2d-129">-ResourceId</span></span>
<span data-ttu-id="aad2d-130">Die Ressourcen-ID der ANF-Sicherung</span><span class="sxs-lookup"><span data-stu-id="aad2d-130">The resource id of the ANF Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad2d-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="aad2d-131">-VolumeName</span></span>
<span data-ttu-id="aad2d-132">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="aad2d-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="aad2d-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="aad2d-133">-VolumeObject</span></span>
<span data-ttu-id="aad2d-134">Das Volumeobjekt mit der zurückzukehrenden Sicherung</span><span class="sxs-lookup"><span data-stu-id="aad2d-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="aad2d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aad2d-135">-Confirm</span></span>
<span data-ttu-id="aad2d-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aad2d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aad2d-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aad2d-137">-WhatIf</span></span>
<span data-ttu-id="aad2d-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aad2d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad2d-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aad2d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aad2d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad2d-140">CommonParameters</span></span>
<span data-ttu-id="aad2d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad2d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad2d-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aad2d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad2d-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aad2d-143">INPUTS</span></span>

### <span data-ttu-id="aad2d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="aad2d-144">System.String</span></span>

### <span data-ttu-id="aad2d-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="aad2d-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="aad2d-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="aad2d-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="aad2d-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aad2d-147">OUTPUTS</span></span>

### <span data-ttu-id="aad2d-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="aad2d-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="aad2d-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aad2d-149">NOTES</span></span>

## <span data-ttu-id="aad2d-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aad2d-150">RELATED LINKS</span></span>
