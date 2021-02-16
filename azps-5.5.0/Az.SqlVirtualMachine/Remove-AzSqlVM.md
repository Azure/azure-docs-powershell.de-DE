---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155164"
---
# <span data-ttu-id="3075d-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="3075d-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="3075d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3075d-102">SYNOPSIS</span></span>
<span data-ttu-id="3075d-103">Löscht einen virtuellen Sql-Computer.</span><span class="sxs-lookup"><span data-stu-id="3075d-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="3075d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3075d-104">SYNTAX</span></span>

### <span data-ttu-id="3075d-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="3075d-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3075d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3075d-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3075d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3075d-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3075d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3075d-108">DESCRIPTION</span></span>
<span data-ttu-id="3075d-109">Das Remove-AzSqlVM cmdlet löscht einen virtuellen Sql-Computer.</span><span class="sxs-lookup"><span data-stu-id="3075d-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="3075d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3075d-110">EXAMPLES</span></span>

### <span data-ttu-id="3075d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3075d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="3075d-112">Löscht den virtuellen Azure SQL "vm" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3075d-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="3075d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3075d-113">PARAMETERS</span></span>

### <span data-ttu-id="3075d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3075d-114">-AsJob</span></span>
<span data-ttu-id="3075d-115">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="3075d-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3075d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3075d-116">-DefaultProfile</span></span>
<span data-ttu-id="3075d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3075d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3075d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3075d-118">-InputObject</span></span>
<span data-ttu-id="3075d-119">SQL virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="3075d-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3075d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3075d-120">-Name</span></span>
<span data-ttu-id="3075d-121">SQL namen des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="3075d-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3075d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3075d-122">-PassThru</span></span>
<span data-ttu-id="3075d-123">Gibt an, ob die gelöschte Ressource am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3075d-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="3075d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3075d-124">-ResourceGroupName</span></span>
<span data-ttu-id="3075d-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3075d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="3075d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3075d-126">-ResourceId</span></span>
<span data-ttu-id="3075d-127">SQL ressourcen-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="3075d-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3075d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3075d-128">-Confirm</span></span>
<span data-ttu-id="3075d-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3075d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3075d-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3075d-130">-WhatIf</span></span>
<span data-ttu-id="3075d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3075d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3075d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3075d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3075d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3075d-133">CommonParameters</span></span>
<span data-ttu-id="3075d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3075d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3075d-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3075d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3075d-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3075d-136">INPUTS</span></span>

### <span data-ttu-id="3075d-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="3075d-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="3075d-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3075d-138">OUTPUTS</span></span>

### <span data-ttu-id="3075d-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="3075d-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="3075d-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3075d-140">NOTES</span></span>

## <span data-ttu-id="3075d-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3075d-141">RELATED LINKS</span></span>
