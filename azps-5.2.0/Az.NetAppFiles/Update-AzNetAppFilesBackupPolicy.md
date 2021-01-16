---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295397"
---
# <span data-ttu-id="f31d7-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f31d7-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f31d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f31d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f31d7-103">Aktualisiert eine Azure NetApp Files (ANF)-Sicherungsrichtlinie für die optionalen Zusatzmodifizierer.</span><span class="sxs-lookup"><span data-stu-id="f31d7-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="f31d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f31d7-104">SYNTAX</span></span>

### <span data-ttu-id="f31d7-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f31d7-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f31d7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f31d7-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f31d7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f31d7-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f31d7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f31d7-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f31d7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f31d7-109">DESCRIPTION</span></span>
<span data-ttu-id="f31d7-110">Das **Cmdlet "Update-AzNetAppFilesBackupPolicy"** ändert eine ANF-Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f31d7-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="f31d7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f31d7-111">EXAMPLES</span></span>

### <span data-ttu-id="f31d7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f31d7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="f31d7-113">Mit diesem Befehl wird die ANF-Sicherungsrichtlinie "MyBackupPolicy" so geändert, dass "DailyBackupsToKeep" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f31d7-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="f31d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f31d7-114">PARAMETERS</span></span>

### <span data-ttu-id="f31d7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f31d7-115">-AccountName</span></span>
<span data-ttu-id="f31d7-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="f31d7-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f31d7-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f31d7-117">-AccountObject</span></span>
<span data-ttu-id="f31d7-118">Das Kontoobjekt mit der zu aktualisierenden Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="f31d7-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="f31d7-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="f31d7-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="f31d7-120">Tägliche Sicherungen werden gezählt</span><span class="sxs-lookup"><span data-stu-id="f31d7-120">Daily backups count to keep</span></span>

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

### <span data-ttu-id="f31d7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31d7-121">-DefaultProfile</span></span>
<span data-ttu-id="f31d7-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f31d7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31d7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f31d7-123">-InputObject</span></span>
<span data-ttu-id="f31d7-124">Das zu entfernende "BackupPolicy"-Objekt</span><span class="sxs-lookup"><span data-stu-id="f31d7-124">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="f31d7-125">-Location</span><span class="sxs-lookup"><span data-stu-id="f31d7-125">-Location</span></span>
<span data-ttu-id="f31d7-126">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="f31d7-126">The location of the resource</span></span>

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

### <span data-ttu-id="f31d7-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="f31d7-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="f31d7-128">Anzahl zu behaltende monatliche Sicherungen</span><span class="sxs-lookup"><span data-stu-id="f31d7-128">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="f31d7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f31d7-129">-Name</span></span>
<span data-ttu-id="f31d7-130">Der Name der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="f31d7-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="f31d7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f31d7-131">-ResourceGroupName</span></span>
<span data-ttu-id="f31d7-132">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="f31d7-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f31d7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f31d7-133">-ResourceId</span></span>
<span data-ttu-id="f31d7-134">Die Ressourcen-ID der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="f31d7-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="f31d7-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f31d7-135">-Tag</span></span>
<span data-ttu-id="f31d7-136">Hashtablearray, das Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="f31d7-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="f31d7-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="f31d7-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="f31d7-138">Anzahl zu behaltende wöchentliche Sicherungen</span><span class="sxs-lookup"><span data-stu-id="f31d7-138">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="f31d7-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="f31d7-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="f31d7-140">Jährlich zu behaltende Sicherungen</span><span class="sxs-lookup"><span data-stu-id="f31d7-140">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="f31d7-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f31d7-141">-Confirm</span></span>
<span data-ttu-id="f31d7-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f31d7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f31d7-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f31d7-143">-WhatIf</span></span>
<span data-ttu-id="f31d7-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f31d7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f31d7-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f31d7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f31d7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31d7-146">CommonParameters</span></span>
<span data-ttu-id="f31d7-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31d7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31d7-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f31d7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31d7-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f31d7-149">INPUTS</span></span>

### <span data-ttu-id="f31d7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f31d7-150">System.String</span></span>

### <span data-ttu-id="f31d7-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f31d7-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f31d7-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f31d7-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f31d7-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f31d7-153">OUTPUTS</span></span>

### <span data-ttu-id="f31d7-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f31d7-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f31d7-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f31d7-155">NOTES</span></span>

## <span data-ttu-id="f31d7-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f31d7-156">RELATED LINKS</span></span>
