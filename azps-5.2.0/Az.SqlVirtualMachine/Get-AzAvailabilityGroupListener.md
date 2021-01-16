---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364676"
---
# <span data-ttu-id="9b650-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="9b650-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="9b650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b650-102">SYNOPSIS</span></span>
<span data-ttu-id="9b650-103">Erhalten Sie einen oder mehrere Verfügbarkeitsgruppenlistener in SQL Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="9b650-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="9b650-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b650-104">SYNTAX</span></span>

### <span data-ttu-id="9b650-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b650-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b650-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="9b650-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b650-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b650-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b650-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b650-108">DESCRIPTION</span></span>
<span data-ttu-id="9b650-109">Der Get-AzAvailabilityGroupListener ruft einen oder mehrere Verfügbarkeitsgruppenlistener aus der Gruppe SQL virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="9b650-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="9b650-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b650-110">EXAMPLES</span></span>

### <span data-ttu-id="9b650-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b650-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="9b650-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="9b650-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="9b650-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="9b650-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="9b650-114">Dieser Befehl ruft Informationen zum Availability Group Listener AgListener01 in der SQL Virtual Machine Group SqlVmGroup01 und Resource Group ResourceGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="9b650-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="9b650-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9b650-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="9b650-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="9b650-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="9b650-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="9b650-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="9b650-118">Dieser Befehl ruft Informationen zu allen Verfügbarkeitsgruppenlistenern in der SQL Virtual Machine Group SqlVmGroup01 und Resource Group ResourceGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="9b650-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="9b650-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9b650-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="9b650-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="9b650-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="9b650-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="9b650-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="9b650-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b650-122">PARAMETERS</span></span>

### <span data-ttu-id="9b650-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b650-123">-DefaultProfile</span></span>
<span data-ttu-id="9b650-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b650-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b650-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9b650-125">-Name</span></span>
<span data-ttu-id="9b650-126">Name des Listeners der Verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9b650-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b650-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b650-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b650-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9b650-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b650-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b650-129">-ResourceId</span></span>
<span data-ttu-id="9b650-130">Ressourcen-ID des Verfügbarkeitsgruppenlisteners</span><span class="sxs-lookup"><span data-stu-id="9b650-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="9b650-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="9b650-131">-SqlVMGroupName</span></span>
<span data-ttu-id="9b650-132">SQL des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9b650-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="9b650-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="9b650-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="9b650-134">SQL virtuellen Computer-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="9b650-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="9b650-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b650-135">CommonParameters</span></span>
<span data-ttu-id="9b650-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b650-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b650-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b650-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b650-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b650-138">INPUTS</span></span>

### <span data-ttu-id="9b650-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9b650-139">System.String</span></span>

### <span data-ttu-id="9b650-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="9b650-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="9b650-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b650-141">OUTPUTS</span></span>

### <span data-ttu-id="9b650-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="9b650-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="9b650-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9b650-143">NOTES</span></span>

## <span data-ttu-id="9b650-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9b650-144">RELATED LINKS</span></span>
