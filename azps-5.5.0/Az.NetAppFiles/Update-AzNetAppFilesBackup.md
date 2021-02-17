---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: a2cab03bb88d5b642a95142030eb646b2a5abef4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147196"
---
# <span data-ttu-id="3666f-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="3666f-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="3666f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3666f-102">SYNOPSIS</span></span>
<span data-ttu-id="3666f-103">Aktualisiert eine Azure NetApp Files (ANF)-Sicherung auf die optionalen Zusatzmodifizierer.</span><span class="sxs-lookup"><span data-stu-id="3666f-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="3666f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3666f-104">SYNTAX</span></span>

### <span data-ttu-id="3666f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3666f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3666f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3666f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3666f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3666f-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3666f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3666f-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3666f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3666f-109">DESCRIPTION</span></span>
<span data-ttu-id="3666f-110">Das **Cmdlet "Update-AzNetAppFilesBackup"** ändert eine ANF-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="3666f-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="3666f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3666f-111">EXAMPLES</span></span>

### <span data-ttu-id="3666f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3666f-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="3666f-113">Dieser Befehl führt eine Aktualisierung für die angegebene Sicherung durch und ändert den Benutzernamen so, dass er bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3666f-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="3666f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3666f-114">PARAMETERS</span></span>

### <span data-ttu-id="3666f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3666f-115">-AccountName</span></span>
<span data-ttu-id="3666f-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="3666f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="3666f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3666f-117">-DefaultProfile</span></span>
<span data-ttu-id="3666f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3666f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3666f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3666f-119">-InputObject</span></span>
<span data-ttu-id="3666f-120">Das zu entfernende Momentaufnahmeobjekt</span><span class="sxs-lookup"><span data-stu-id="3666f-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="3666f-121">-Label</span><span class="sxs-lookup"><span data-stu-id="3666f-121">-Label</span></span>
<span data-ttu-id="3666f-122">Bezeichnung für Sicherungskopien</span><span class="sxs-lookup"><span data-stu-id="3666f-122">Label for backup</span></span>

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

### <span data-ttu-id="3666f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="3666f-123">-Location</span></span>
<span data-ttu-id="3666f-124">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="3666f-124">The location of the resource</span></span>

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

### <span data-ttu-id="3666f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3666f-125">-Name</span></span>
<span data-ttu-id="3666f-126">Der Name der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3666f-126">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="3666f-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="3666f-127">-PoolName</span></span>
<span data-ttu-id="3666f-128">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="3666f-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="3666f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3666f-129">-ResourceGroupName</span></span>
<span data-ttu-id="3666f-130">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="3666f-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3666f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3666f-131">-ResourceId</span></span>
<span data-ttu-id="3666f-132">Die Ressourcen-ID der ANF-Sicherung</span><span class="sxs-lookup"><span data-stu-id="3666f-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="3666f-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="3666f-133">-Tag</span></span>
<span data-ttu-id="3666f-134">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="3666f-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="3666f-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="3666f-135">-VolumeName</span></span>
<span data-ttu-id="3666f-136">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="3666f-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="3666f-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="3666f-137">-VolumeObject</span></span>
<span data-ttu-id="3666f-138">Das Volumeobjekt mit der zurückzukehrenden Sicherung</span><span class="sxs-lookup"><span data-stu-id="3666f-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="3666f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3666f-139">-Confirm</span></span>
<span data-ttu-id="3666f-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3666f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3666f-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3666f-141">-WhatIf</span></span>
<span data-ttu-id="3666f-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3666f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3666f-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3666f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3666f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3666f-144">CommonParameters</span></span>
<span data-ttu-id="3666f-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3666f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3666f-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3666f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3666f-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3666f-147">INPUTS</span></span>

### <span data-ttu-id="3666f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3666f-148">System.String</span></span>

### <span data-ttu-id="3666f-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3666f-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="3666f-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="3666f-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="3666f-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3666f-151">OUTPUTS</span></span>

### <span data-ttu-id="3666f-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3666f-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="3666f-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3666f-153">NOTES</span></span>

## <span data-ttu-id="3666f-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3666f-154">RELATED LINKS</span></span>
