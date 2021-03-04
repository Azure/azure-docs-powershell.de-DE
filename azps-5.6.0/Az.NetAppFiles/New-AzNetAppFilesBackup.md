---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 6b4527430fa74efa09aa07fd120d0acf8de0edfd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926856"
---
# <span data-ttu-id="90ccd-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="90ccd-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="90ccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="90ccd-103">Erstellt eine neue Azure NetApp Files (ANF)-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="90ccd-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="90ccd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90ccd-104">SYNTAX</span></span>

### <span data-ttu-id="90ccd-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="90ccd-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ccd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90ccd-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90ccd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90ccd-107">DESCRIPTION</span></span>
<span data-ttu-id="90ccd-108">Das **Cmdlet New-AzNetAppFilesBackup** erstellt eine Sicherung für ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="90ccd-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="90ccd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90ccd-109">EXAMPLES</span></span>

### <span data-ttu-id="90ccd-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90ccd-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="90ccd-111">Mit diesem Befehl wird die neue ANF-Sicherung für das Volumenkonto "MyVolume" erstellt.</span><span class="sxs-lookup"><span data-stu-id="90ccd-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="90ccd-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="90ccd-112">PARAMETERS</span></span>

### <span data-ttu-id="90ccd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="90ccd-113">-AccountName</span></span>
<span data-ttu-id="90ccd-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="90ccd-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="90ccd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ccd-115">-DefaultProfile</span></span>
<span data-ttu-id="90ccd-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90ccd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90ccd-117">-Label</span><span class="sxs-lookup"><span data-stu-id="90ccd-117">-Label</span></span>
<span data-ttu-id="90ccd-118">Bezeichnung für die Sicherung</span><span class="sxs-lookup"><span data-stu-id="90ccd-118">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ccd-119">-Location</span><span class="sxs-lookup"><span data-stu-id="90ccd-119">-Location</span></span>
<span data-ttu-id="90ccd-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="90ccd-120">The location of the resource</span></span>

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

### <span data-ttu-id="90ccd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="90ccd-121">-Name</span></span>
<span data-ttu-id="90ccd-122">Der Name der ANF-Sicherung</span><span class="sxs-lookup"><span data-stu-id="90ccd-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ccd-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="90ccd-123">-PoolName</span></span>
<span data-ttu-id="90ccd-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="90ccd-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="90ccd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ccd-125">-ResourceGroupName</span></span>
<span data-ttu-id="90ccd-126">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="90ccd-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="90ccd-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="90ccd-127">-VolumeName</span></span>
<span data-ttu-id="90ccd-128">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="90ccd-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="90ccd-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="90ccd-129">-VolumeObject</span></span>
<span data-ttu-id="90ccd-130">Das Volume für das neue Sicherungsobjekt</span><span class="sxs-lookup"><span data-stu-id="90ccd-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="90ccd-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90ccd-131">-Confirm</span></span>
<span data-ttu-id="90ccd-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90ccd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90ccd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ccd-133">-WhatIf</span></span>
<span data-ttu-id="90ccd-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90ccd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ccd-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90ccd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90ccd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ccd-136">CommonParameters</span></span>
<span data-ttu-id="90ccd-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ccd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ccd-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90ccd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ccd-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90ccd-139">INPUTS</span></span>

### <span data-ttu-id="90ccd-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="90ccd-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="90ccd-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90ccd-141">OUTPUTS</span></span>

### <span data-ttu-id="90ccd-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="90ccd-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="90ccd-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="90ccd-143">NOTES</span></span>

## <span data-ttu-id="90ccd-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="90ccd-144">RELATED LINKS</span></span>
