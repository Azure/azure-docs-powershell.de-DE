---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: 95b7ad2ea93f1e1b22eafe3fbaae811dc33f24d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926680"
---
# <span data-ttu-id="070a2-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="070a2-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="070a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="070a2-102">SYNOPSIS</span></span>
<span data-ttu-id="070a2-103">Aktualisiert eine Azure NetApp Files (ANF)-Sicherung auf die optionalen Modifizierer, die bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="070a2-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="070a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="070a2-104">SYNTAX</span></span>

### <span data-ttu-id="070a2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="070a2-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="070a2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="070a2-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="070a2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="070a2-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="070a2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="070a2-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="070a2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="070a2-109">DESCRIPTION</span></span>
<span data-ttu-id="070a2-110">Das **Update-AzNetAppFilesBackup-Cmdlet** ändert eine ANF-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="070a2-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="070a2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="070a2-111">EXAMPLES</span></span>

### <span data-ttu-id="070a2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="070a2-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="070a2-113">Dieser Befehl führt eine Aktualisierung der angegebenen Sicherung durch, um den Benutzernamen an die angegebene Zusicherung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="070a2-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="070a2-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="070a2-114">PARAMETERS</span></span>

### <span data-ttu-id="070a2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="070a2-115">-AccountName</span></span>
<span data-ttu-id="070a2-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="070a2-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="070a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="070a2-117">-DefaultProfile</span></span>
<span data-ttu-id="070a2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="070a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="070a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="070a2-119">-InputObject</span></span>
<span data-ttu-id="070a2-120">Das zu entfernende Snapshotobjekt</span><span class="sxs-lookup"><span data-stu-id="070a2-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="070a2-121">-Label</span><span class="sxs-lookup"><span data-stu-id="070a2-121">-Label</span></span>
<span data-ttu-id="070a2-122">Bezeichnung für die Sicherung</span><span class="sxs-lookup"><span data-stu-id="070a2-122">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070a2-123">-Location</span><span class="sxs-lookup"><span data-stu-id="070a2-123">-Location</span></span>
<span data-ttu-id="070a2-124">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="070a2-124">The location of the resource</span></span>

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

### <span data-ttu-id="070a2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="070a2-125">-Name</span></span>
<span data-ttu-id="070a2-126">Der Name der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="070a2-126">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070a2-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="070a2-127">-PoolName</span></span>
<span data-ttu-id="070a2-128">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="070a2-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="070a2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="070a2-129">-ResourceGroupName</span></span>
<span data-ttu-id="070a2-130">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="070a2-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="070a2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="070a2-131">-ResourceId</span></span>
<span data-ttu-id="070a2-132">Die Ressourcen-ID der ANF-Sicherung</span><span class="sxs-lookup"><span data-stu-id="070a2-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="070a2-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="070a2-133">-Tag</span></span>
<span data-ttu-id="070a2-134">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="070a2-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="070a2-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="070a2-135">-VolumeName</span></span>
<span data-ttu-id="070a2-136">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="070a2-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="070a2-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="070a2-137">-VolumeObject</span></span>
<span data-ttu-id="070a2-138">Das Volumeobjekt, das die zurückzukehrende Sicherung enthält</span><span class="sxs-lookup"><span data-stu-id="070a2-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="070a2-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="070a2-139">-Confirm</span></span>
<span data-ttu-id="070a2-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="070a2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="070a2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="070a2-141">-WhatIf</span></span>
<span data-ttu-id="070a2-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="070a2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="070a2-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="070a2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="070a2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="070a2-144">CommonParameters</span></span>
<span data-ttu-id="070a2-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="070a2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="070a2-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="070a2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="070a2-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="070a2-147">INPUTS</span></span>

### <span data-ttu-id="070a2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="070a2-148">System.String</span></span>

### <span data-ttu-id="070a2-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="070a2-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="070a2-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="070a2-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="070a2-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="070a2-151">OUTPUTS</span></span>

### <span data-ttu-id="070a2-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="070a2-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="070a2-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="070a2-153">NOTES</span></span>

## <span data-ttu-id="070a2-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="070a2-154">RELATED LINKS</span></span>
