---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: 7af4302a17d15ba539a726ce84ef47bb1d574609
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826248"
---
# <span data-ttu-id="4720e-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="4720e-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="4720e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4720e-102">SYNOPSIS</span></span>
<span data-ttu-id="4720e-103">Löscht eine SQL Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4720e-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="4720e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4720e-104">SYNTAX</span></span>

### <span data-ttu-id="4720e-105">ParamaterList (Standard)</span><span class="sxs-lookup"><span data-stu-id="4720e-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4720e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4720e-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4720e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4720e-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4720e-108">Namen</span><span class="sxs-lookup"><span data-stu-id="4720e-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4720e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4720e-109">DESCRIPTION</span></span>
<span data-ttu-id="4720e-110">Das Remove-AzSqlVMGroup-Cmdlet löscht eine SQL Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4720e-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="4720e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4720e-111">EXAMPLES</span></span>

### <span data-ttu-id="4720e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4720e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="4720e-113">Löscht die Azure SQL Virtual Machine-Gruppe "Testgruppe" in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4720e-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="4720e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4720e-114">PARAMETERS</span></span>

### <span data-ttu-id="4720e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4720e-115">-AsJob</span></span>
<span data-ttu-id="4720e-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="4720e-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4720e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4720e-117">-DefaultProfile</span></span>
<span data-ttu-id="4720e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4720e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4720e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4720e-119">-InputObject</span></span>
<span data-ttu-id="4720e-120">SQL-Objekt für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="4720e-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="4720e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4720e-121">-Name</span></span>
<span data-ttu-id="4720e-122">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="4720e-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="4720e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4720e-123">-PassThru</span></span>
<span data-ttu-id="4720e-124">Gibt an, ob die gelöschte Ressource am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4720e-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="4720e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4720e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4720e-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4720e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4720e-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4720e-127">-ResourceId</span></span>
<span data-ttu-id="4720e-128">Ressourcen-ID der SQL-virtuellen Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="4720e-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="4720e-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4720e-129">-Confirm</span></span>
<span data-ttu-id="4720e-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4720e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4720e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4720e-131">-WhatIf</span></span>
<span data-ttu-id="4720e-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4720e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4720e-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4720e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4720e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4720e-134">CommonParameters</span></span>
<span data-ttu-id="4720e-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4720e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4720e-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4720e-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4720e-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4720e-137">INPUTS</span></span>

### <span data-ttu-id="4720e-138">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="4720e-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="4720e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4720e-139">System.String</span></span>

## <span data-ttu-id="4720e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4720e-140">OUTPUTS</span></span>

### <span data-ttu-id="4720e-141">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="4720e-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="4720e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4720e-142">NOTES</span></span>

## <span data-ttu-id="4720e-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4720e-143">RELATED LINKS</span></span>
