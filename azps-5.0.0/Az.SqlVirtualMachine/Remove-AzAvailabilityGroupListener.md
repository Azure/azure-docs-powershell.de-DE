---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175850"
---
# <span data-ttu-id="06b93-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="06b93-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="06b93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06b93-102">SYNOPSIS</span></span>
<span data-ttu-id="06b93-103">Löscht einen Verfügbarkeitsgruppen-Listener.</span><span class="sxs-lookup"><span data-stu-id="06b93-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="06b93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06b93-104">SYNTAX</span></span>

### <span data-ttu-id="06b93-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="06b93-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06b93-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="06b93-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b93-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="06b93-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b93-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="06b93-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b93-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06b93-109">DESCRIPTION</span></span>
<span data-ttu-id="06b93-110">Das Remove-AzAvailabilityGroupListener-Cmdlet löscht einen Verfügbarkeitsgruppen-Listener.</span><span class="sxs-lookup"><span data-stu-id="06b93-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="06b93-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06b93-111">EXAMPLES</span></span>

### <span data-ttu-id="06b93-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06b93-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="06b93-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="06b93-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="06b93-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="06b93-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="06b93-115">Löscht die AgListener01 der verfügbarkeitsgruppe in der verfügbarkeitsgruppe AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="06b93-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="06b93-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="06b93-116">PARAMETERS</span></span>

### <span data-ttu-id="06b93-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06b93-117">-AsJob</span></span>
<span data-ttu-id="06b93-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="06b93-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="06b93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b93-119">-DefaultProfile</span></span>
<span data-ttu-id="06b93-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06b93-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06b93-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="06b93-121">-InputObject</span></span>
<span data-ttu-id="06b93-122">Listener-Objekt der verfügbarkeitsgruppe</span><span class="sxs-lookup"><span data-stu-id="06b93-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06b93-123">-Name</span><span class="sxs-lookup"><span data-stu-id="06b93-123">-Name</span></span>
<span data-ttu-id="06b93-124">Listener-Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="06b93-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b93-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06b93-125">-PassThru</span></span>
<span data-ttu-id="06b93-126">Gibt an, ob die gelöschte Ressource am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="06b93-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="06b93-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b93-127">-ResourceGroupName</span></span>
<span data-ttu-id="06b93-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06b93-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="06b93-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="06b93-129">-ResourceId</span></span>
<span data-ttu-id="06b93-130">Verfügbarkeitsgruppen-Listener-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="06b93-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b93-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="06b93-131">-SqlVMGroupName</span></span>
<span data-ttu-id="06b93-132">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="06b93-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b93-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="06b93-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="06b93-134">Gruppenobjekt der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="06b93-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06b93-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06b93-135">-Confirm</span></span>
<span data-ttu-id="06b93-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06b93-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b93-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b93-137">-WhatIf</span></span>
<span data-ttu-id="06b93-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06b93-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b93-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06b93-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b93-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b93-140">CommonParameters</span></span>
<span data-ttu-id="06b93-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b93-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b93-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06b93-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b93-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06b93-143">INPUTS</span></span>

### <span data-ttu-id="06b93-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="06b93-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="06b93-145">System. String</span><span class="sxs-lookup"><span data-stu-id="06b93-145">System.String</span></span>

### <span data-ttu-id="06b93-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="06b93-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="06b93-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06b93-147">OUTPUTS</span></span>

### <span data-ttu-id="06b93-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="06b93-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="06b93-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="06b93-149">NOTES</span></span>

## <span data-ttu-id="06b93-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06b93-150">RELATED LINKS</span></span>
