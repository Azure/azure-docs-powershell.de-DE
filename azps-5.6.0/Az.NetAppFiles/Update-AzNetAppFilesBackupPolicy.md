---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 14c2a58c40aa29f1b48902be5d82911f70a71cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926675"
---
# <span data-ttu-id="929c1-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="929c1-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="929c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="929c1-102">SYNOPSIS</span></span>
<span data-ttu-id="929c1-103">Aktualisiert eine Azure NetApp Files (ANF)-Sicherungsrichtlinie auf die optionalen bereitgestellten Modifikatoren.</span><span class="sxs-lookup"><span data-stu-id="929c1-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="929c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="929c1-104">SYNTAX</span></span>

### <span data-ttu-id="929c1-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="929c1-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="929c1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="929c1-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="929c1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="929c1-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="929c1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="929c1-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="929c1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="929c1-109">DESCRIPTION</span></span>
<span data-ttu-id="929c1-110">Das **Cmdlet Update-AzNetAppFilesBackupPolicy** ändert eine ANF-Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="929c1-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="929c1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="929c1-111">EXAMPLES</span></span>

### <span data-ttu-id="929c1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="929c1-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="929c1-113">Mit diesem Befehl wird die ANF-Sicherungsrichtlinie "MyBackupPolicy" so geändert, dass die angegebene DailyBackupsToKeep-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="929c1-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="929c1-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="929c1-114">PARAMETERS</span></span>

### <span data-ttu-id="929c1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="929c1-115">-AccountName</span></span>
<span data-ttu-id="929c1-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="929c1-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="929c1-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="929c1-117">-AccountObject</span></span>
<span data-ttu-id="929c1-118">Das Kontoobjekt, das die zu aktualisierende Sicherungsrichtlinie enthält</span><span class="sxs-lookup"><span data-stu-id="929c1-118">The Account object containing the Backup Policy to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="929c1-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="929c1-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="929c1-120">Tägliche Sicherungen zählen zu behalten</span><span class="sxs-lookup"><span data-stu-id="929c1-120">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929c1-121">-DefaultProfile</span></span>
<span data-ttu-id="929c1-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="929c1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="929c1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="929c1-123">-InputObject</span></span>
<span data-ttu-id="929c1-124">Das zu entfernende BackupPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="929c1-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="929c1-125">-Location</span><span class="sxs-lookup"><span data-stu-id="929c1-125">-Location</span></span>
<span data-ttu-id="929c1-126">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="929c1-126">The location of the resource</span></span>

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

### <span data-ttu-id="929c1-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="929c1-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="929c1-128">Anzahl der monatlichen Sicherungen, die sie behalten müssen</span><span class="sxs-lookup"><span data-stu-id="929c1-128">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929c1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="929c1-129">-Name</span></span>
<span data-ttu-id="929c1-130">Der Name der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="929c1-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="929c1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="929c1-131">-ResourceGroupName</span></span>
<span data-ttu-id="929c1-132">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="929c1-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="929c1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="929c1-133">-ResourceId</span></span>
<span data-ttu-id="929c1-134">Die Ressourcen-ID der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="929c1-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="929c1-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="929c1-135">-Tag</span></span>
<span data-ttu-id="929c1-136">Ein Hashtablearray, das Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="929c1-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="929c1-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="929c1-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="929c1-138">Anzahl der wöchentlichen Sicherungen, die sie behalten müssen</span><span class="sxs-lookup"><span data-stu-id="929c1-138">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929c1-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="929c1-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="929c1-140">Anzahl der jährlichen Sicherungen, die sie behalten müssen</span><span class="sxs-lookup"><span data-stu-id="929c1-140">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929c1-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="929c1-141">-Confirm</span></span>
<span data-ttu-id="929c1-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="929c1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="929c1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="929c1-143">-WhatIf</span></span>
<span data-ttu-id="929c1-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="929c1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="929c1-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="929c1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="929c1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929c1-146">CommonParameters</span></span>
<span data-ttu-id="929c1-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="929c1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929c1-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="929c1-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929c1-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="929c1-149">INPUTS</span></span>

### <span data-ttu-id="929c1-150">System.String</span><span class="sxs-lookup"><span data-stu-id="929c1-150">System.String</span></span>

### <span data-ttu-id="929c1-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="929c1-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="929c1-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="929c1-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="929c1-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="929c1-153">OUTPUTS</span></span>

### <span data-ttu-id="929c1-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="929c1-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="929c1-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="929c1-155">NOTES</span></span>

## <span data-ttu-id="929c1-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="929c1-156">RELATED LINKS</span></span>
