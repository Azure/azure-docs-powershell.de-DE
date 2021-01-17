---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359833"
---
# <span data-ttu-id="6d127-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6d127-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="6d127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d127-102">SYNOPSIS</span></span>
<span data-ttu-id="6d127-103">Löscht eine Azure NetApp Files (ANF)-Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6d127-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="6d127-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d127-104">SYNTAX</span></span>

### <span data-ttu-id="6d127-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d127-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d127-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d127-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d127-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d127-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d127-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d127-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d127-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d127-109">DESCRIPTION</span></span>
<span data-ttu-id="6d127-110">Das **Cmdlet "Remove-AzNetAppFilesBackupPolicy"** löscht eine ANF-Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6d127-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="6d127-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d127-111">EXAMPLES</span></span>

### <span data-ttu-id="6d127-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d127-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="6d127-113">Mit diesem Befehl wird die neue ANF-Sicherungsrichtlinie mit dem Namen "MyBackupPolicy" für das Konto "MyAccount" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6d127-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="6d127-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d127-114">PARAMETERS</span></span>

### <span data-ttu-id="6d127-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d127-115">-AccountName</span></span>
<span data-ttu-id="6d127-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="6d127-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="6d127-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6d127-117">-AccountObject</span></span>
<span data-ttu-id="6d127-118">Das Kontoobjekt mit der zu entfernenden Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="6d127-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="6d127-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d127-119">-DefaultProfile</span></span>
<span data-ttu-id="6d127-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d127-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d127-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d127-121">-InputObject</span></span>
<span data-ttu-id="6d127-122">Das zu entfernende "BackupPolicy"-Objekt</span><span class="sxs-lookup"><span data-stu-id="6d127-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="6d127-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6d127-123">-Name</span></span>
<span data-ttu-id="6d127-124">Der Name der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="6d127-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="6d127-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d127-125">-PassThru</span></span>
<span data-ttu-id="6d127-126">Zurückgeben, ob die angegebene Sicherungsrichtlinie erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="6d127-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="6d127-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d127-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d127-128">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="6d127-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="6d127-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d127-129">-ResourceId</span></span>
<span data-ttu-id="6d127-130">Die Ressourcen-ID der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="6d127-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="6d127-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d127-131">-Confirm</span></span>
<span data-ttu-id="6d127-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d127-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d127-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6d127-133">-WhatIf</span></span>
<span data-ttu-id="6d127-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d127-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d127-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d127-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d127-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d127-136">CommonParameters</span></span>
<span data-ttu-id="6d127-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d127-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d127-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d127-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d127-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d127-139">INPUTS</span></span>

### <span data-ttu-id="6d127-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6d127-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="6d127-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6d127-141">System.String</span></span>

### <span data-ttu-id="6d127-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6d127-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="6d127-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d127-143">OUTPUTS</span></span>

### <span data-ttu-id="6d127-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6d127-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="6d127-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6d127-145">NOTES</span></span>

## <span data-ttu-id="6d127-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6d127-146">RELATED LINKS</span></span>
