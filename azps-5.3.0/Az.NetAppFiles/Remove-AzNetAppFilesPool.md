---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473501"
---
# <span data-ttu-id="3aa26-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3aa26-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="3aa26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aa26-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa26-103">Löscht einen Azure NetApp Files (ANF)-Pool.</span><span class="sxs-lookup"><span data-stu-id="3aa26-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="3aa26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3aa26-104">SYNTAX</span></span>

### <span data-ttu-id="3aa26-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3aa26-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa26-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aa26-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa26-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aa26-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa26-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aa26-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aa26-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3aa26-109">DESCRIPTION</span></span>
<span data-ttu-id="3aa26-110">Das **Cmdlet "Remove-AzNetAppFilesPool"** löscht einen ANF-Pool.</span><span class="sxs-lookup"><span data-stu-id="3aa26-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="3aa26-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3aa26-111">EXAMPLES</span></span>

### <span data-ttu-id="3aa26-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3aa26-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="3aa26-113">Mit diesem Befehl wird der ANF-Pool "MyAnfPool" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3aa26-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="3aa26-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3aa26-114">PARAMETERS</span></span>

### <span data-ttu-id="3aa26-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3aa26-115">-AccountName</span></span>
<span data-ttu-id="3aa26-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="3aa26-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="3aa26-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="3aa26-117">-AccountObject</span></span>
<span data-ttu-id="3aa26-118">Das Kontoobjekt, das den zu entfernenden Pool enthält</span><span class="sxs-lookup"><span data-stu-id="3aa26-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="3aa26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa26-119">-DefaultProfile</span></span>
<span data-ttu-id="3aa26-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3aa26-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aa26-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aa26-121">-InputObject</span></span>
<span data-ttu-id="3aa26-122">Das zu entfernende Poolobjekt</span><span class="sxs-lookup"><span data-stu-id="3aa26-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa26-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3aa26-123">-Name</span></span>
<span data-ttu-id="3aa26-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="3aa26-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa26-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3aa26-125">-PassThru</span></span>
<span data-ttu-id="3aa26-126">Zurückgeben, ob der angegebene Pool erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="3aa26-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="3aa26-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa26-127">-ResourceGroupName</span></span>
<span data-ttu-id="3aa26-128">Die Ressourcengruppe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="3aa26-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="3aa26-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa26-129">-ResourceId</span></span>
<span data-ttu-id="3aa26-130">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="3aa26-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="3aa26-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3aa26-131">-Confirm</span></span>
<span data-ttu-id="3aa26-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3aa26-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa26-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3aa26-133">-WhatIf</span></span>
<span data-ttu-id="3aa26-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3aa26-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aa26-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3aa26-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aa26-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa26-136">CommonParameters</span></span>
<span data-ttu-id="3aa26-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa26-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa26-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3aa26-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa26-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3aa26-139">INPUTS</span></span>

### <span data-ttu-id="3aa26-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3aa26-140">System.String</span></span>

### <span data-ttu-id="3aa26-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3aa26-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="3aa26-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3aa26-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="3aa26-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3aa26-143">OUTPUTS</span></span>

### <span data-ttu-id="3aa26-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3aa26-144">System.Boolean</span></span>

## <span data-ttu-id="3aa26-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3aa26-145">NOTES</span></span>

## <span data-ttu-id="3aa26-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3aa26-146">RELATED LINKS</span></span>
