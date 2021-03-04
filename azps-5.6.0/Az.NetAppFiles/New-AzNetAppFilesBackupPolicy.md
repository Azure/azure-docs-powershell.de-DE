---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 18fa19b4f173dd3539277e0a1c226afbee0de381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926848"
---
# <span data-ttu-id="82877-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="82877-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="82877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82877-102">SYNOPSIS</span></span>
<span data-ttu-id="82877-103">Erstellt eine neue Azure NetApp Files (ANF)-Sicherungsrichtlinie für ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="82877-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="82877-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82877-104">SYNTAX</span></span>

### <span data-ttu-id="82877-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="82877-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82877-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82877-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82877-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82877-107">DESCRIPTION</span></span>
<span data-ttu-id="82877-108">Das **Cmdlet New-AzNetAppFilesActiveDirectory** erstellt eine neue Sicherungsrichtlinie für ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="82877-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="82877-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82877-109">EXAMPLES</span></span>

### <span data-ttu-id="82877-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82877-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="82877-111">Mit diesem Befehl wird die neue ANF-Sicherungsrichtlinie für das ANF-Konto mit dem Namen "MyAccount" erstellt.</span><span class="sxs-lookup"><span data-stu-id="82877-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="82877-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82877-112">PARAMETERS</span></span>

### <span data-ttu-id="82877-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82877-113">-AccountName</span></span>
<span data-ttu-id="82877-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="82877-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="82877-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="82877-115">-AccountObject</span></span>
<span data-ttu-id="82877-116">Das Kontoobjekt für die neue Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="82877-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="82877-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="82877-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="82877-118">Tägliche Sicherungen zählen zu behalten</span><span class="sxs-lookup"><span data-stu-id="82877-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="82877-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82877-119">-DefaultProfile</span></span>
<span data-ttu-id="82877-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82877-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82877-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="82877-121">-Enabled</span></span>
<span data-ttu-id="82877-122">Die Zu entscheidende Eigenschaft der Richtlinie ist aktiviert oder nicht</span><span class="sxs-lookup"><span data-stu-id="82877-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="82877-123">-Location</span><span class="sxs-lookup"><span data-stu-id="82877-123">-Location</span></span>
<span data-ttu-id="82877-124">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="82877-124">The location of the resource</span></span>

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

### <span data-ttu-id="82877-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="82877-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="82877-126">Anzahl der monatlichen Sicherungen, die sie behalten müssen</span><span class="sxs-lookup"><span data-stu-id="82877-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="82877-127">-Name</span><span class="sxs-lookup"><span data-stu-id="82877-127">-Name</span></span>
<span data-ttu-id="82877-128">Der Name der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="82877-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82877-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82877-129">-ResourceGroupName</span></span>
<span data-ttu-id="82877-130">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="82877-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="82877-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="82877-131">-Tag</span></span>
<span data-ttu-id="82877-132">Ein Hashtablearray, das Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="82877-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="82877-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="82877-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="82877-134">Anzahl der wöchentlichen Sicherungen, die sie behalten müssen</span><span class="sxs-lookup"><span data-stu-id="82877-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="82877-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="82877-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="82877-136">Anzahl der jährlichen Sicherungen, die sie behalten müssen</span><span class="sxs-lookup"><span data-stu-id="82877-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="82877-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="82877-137">-Confirm</span></span>
<span data-ttu-id="82877-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82877-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82877-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82877-139">-WhatIf</span></span>
<span data-ttu-id="82877-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82877-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82877-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82877-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82877-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82877-142">CommonParameters</span></span>
<span data-ttu-id="82877-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82877-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82877-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82877-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82877-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82877-145">INPUTS</span></span>

### <span data-ttu-id="82877-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="82877-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="82877-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82877-147">OUTPUTS</span></span>

### <span data-ttu-id="82877-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="82877-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="82877-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82877-149">NOTES</span></span>

## <span data-ttu-id="82877-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82877-150">RELATED LINKS</span></span>
