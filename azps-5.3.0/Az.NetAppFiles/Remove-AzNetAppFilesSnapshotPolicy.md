---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380608"
---
# <span data-ttu-id="9e9f7-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="9e9f7-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="9e9f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e9f7-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9f7-103">Löscht eine Azure NetApp Files (ANF)-Momentaufnahmerichtlinie.</span><span class="sxs-lookup"><span data-stu-id="9e9f7-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="9e9f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e9f7-104">SYNTAX</span></span>

### <span data-ttu-id="9e9f7-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e9f7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e9f7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e9f7-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e9f7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e9f7-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e9f7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e9f7-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e9f7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e9f7-109">DESCRIPTION</span></span>
<span data-ttu-id="9e9f7-110">Das **Cmdlet "Remove-AzNetAppFilesSnapshotPolicy"** löscht eine ANF-Momentaufnahmerichtlinie.</span><span class="sxs-lookup"><span data-stu-id="9e9f7-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="9e9f7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e9f7-111">EXAMPLES</span></span>

### <span data-ttu-id="9e9f7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e9f7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="9e9f7-113">Mit diesem Befehl wird die neue ANF-Sicherungsrichtlinie mit dem Namen "MyBackupPolicy" für das Konto "MyAccount" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9e9f7-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="9e9f7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e9f7-114">PARAMETERS</span></span>

### <span data-ttu-id="9e9f7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9e9f7-115">-AccountName</span></span>
<span data-ttu-id="9e9f7-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="9e9f7-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9e9f7-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="9e9f7-117">-AccountObject</span></span>
<span data-ttu-id="9e9f7-118">Das Konto für das neue Snapshotrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="9e9f7-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="9e9f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9f7-119">-DefaultProfile</span></span>
<span data-ttu-id="9e9f7-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e9f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e9f7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e9f7-121">-InputObject</span></span>
<span data-ttu-id="9e9f7-122">Das zu entfernende SnapshotPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e9f7-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9e9f7-123">-Name</span></span>
<span data-ttu-id="9e9f7-124">Der Name der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="9e9f7-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e9f7-125">-PassThru</span></span>
<span data-ttu-id="9e9f7-126">Rückgabe, ob das angegebene Konto erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="9e9f7-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="9e9f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e9f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e9f7-128">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="9e9f7-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9e9f7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e9f7-129">-ResourceId</span></span>
<span data-ttu-id="9e9f7-130">Die Ressourcen-ID der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="9e9f7-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="9e9f7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e9f7-131">-Confirm</span></span>
<span data-ttu-id="9e9f7-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e9f7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e9f7-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9e9f7-133">-WhatIf</span></span>
<span data-ttu-id="9e9f7-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e9f7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e9f7-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e9f7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e9f7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9f7-136">CommonParameters</span></span>
<span data-ttu-id="9e9f7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e9f7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9f7-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e9f7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9f7-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e9f7-139">INPUTS</span></span>

### <span data-ttu-id="9e9f7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9e9f7-140">System.String</span></span>

### <span data-ttu-id="9e9f7-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9e9f7-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="9e9f7-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="9e9f7-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="9e9f7-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e9f7-143">OUTPUTS</span></span>

### <span data-ttu-id="9e9f7-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="9e9f7-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="9e9f7-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e9f7-145">NOTES</span></span>

## <span data-ttu-id="9e9f7-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e9f7-146">RELATED LINKS</span></span>
