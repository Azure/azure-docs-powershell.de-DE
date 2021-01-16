---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294952"
---
# <span data-ttu-id="c9935-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="c9935-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="c9935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9935-102">SYNOPSIS</span></span>
<span data-ttu-id="c9935-103">Löscht eine Gruppe des virtuellen Sql-Computers.</span><span class="sxs-lookup"><span data-stu-id="c9935-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="c9935-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9935-104">SYNTAX</span></span>

### <span data-ttu-id="c9935-105">ParamaterList (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9935-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9935-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c9935-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9935-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9935-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9935-108">Name</span><span class="sxs-lookup"><span data-stu-id="c9935-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9935-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9935-109">DESCRIPTION</span></span>
<span data-ttu-id="c9935-110">Das Remove-AzSqlVMGroup cmdlet löscht eine Gruppe des virtuellen Sql-Computers.</span><span class="sxs-lookup"><span data-stu-id="c9935-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="c9935-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c9935-111">EXAMPLES</span></span>

### <span data-ttu-id="c9935-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c9935-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="c9935-113">Löscht die Azure SQL Gruppe "Test"" des virtuellen Computers in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c9935-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="c9935-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9935-114">PARAMETERS</span></span>

### <span data-ttu-id="c9935-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9935-115">-AsJob</span></span>
<span data-ttu-id="c9935-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="c9935-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c9935-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9935-117">-DefaultProfile</span></span>
<span data-ttu-id="c9935-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9935-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9935-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9935-119">-InputObject</span></span>
<span data-ttu-id="c9935-120">SQL virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="c9935-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9935-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c9935-121">-Name</span></span>
<span data-ttu-id="c9935-122">SQL gruppenname des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c9935-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9935-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9935-123">-PassThru</span></span>
<span data-ttu-id="c9935-124">Gibt an, ob die gelöschte Ressource am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9935-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="c9935-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9935-125">-ResourceGroupName</span></span>
<span data-ttu-id="c9935-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c9935-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9935-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9935-127">-ResourceId</span></span>
<span data-ttu-id="c9935-128">SQL ressourcen-ID der Gruppe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c9935-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9935-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9935-129">-Confirm</span></span>
<span data-ttu-id="c9935-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9935-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9935-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c9935-131">-WhatIf</span></span>
<span data-ttu-id="c9935-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9935-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9935-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9935-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9935-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9935-134">CommonParameters</span></span>
<span data-ttu-id="c9935-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9935-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9935-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9935-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9935-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c9935-137">INPUTS</span></span>

### <span data-ttu-id="c9935-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="c9935-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="c9935-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c9935-139">System.String</span></span>

## <span data-ttu-id="c9935-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c9935-140">OUTPUTS</span></span>

### <span data-ttu-id="c9935-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="c9935-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="c9935-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c9935-142">NOTES</span></span>

## <span data-ttu-id="c9935-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c9935-143">RELATED LINKS</span></span>
