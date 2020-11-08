---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173427"
---
# <span data-ttu-id="2539a-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="2539a-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="2539a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2539a-102">SYNOPSIS</span></span>
<span data-ttu-id="2539a-103">Rufen Sie einen oder mehrere Listener der Verfügbarkeitsgruppen in einer Gruppe von SQL-virtuellen Computern ab.</span><span class="sxs-lookup"><span data-stu-id="2539a-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="2539a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2539a-104">SYNTAX</span></span>

### <span data-ttu-id="2539a-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="2539a-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2539a-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="2539a-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2539a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2539a-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2539a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2539a-108">DESCRIPTION</span></span>
<span data-ttu-id="2539a-109">Der Get-AzAvailabilityGroupListener ruft mindestens einen Verfügbarkeitsgruppen-Listener aus der Gruppe SQL Virtual Machine ab.</span><span class="sxs-lookup"><span data-stu-id="2539a-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="2539a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2539a-110">EXAMPLES</span></span>

### <span data-ttu-id="2539a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2539a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="2539a-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="2539a-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="2539a-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="2539a-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="2539a-114">Dieser Befehl ruft Informationen zum AgListener01 der verfügbarkeitsgruppe in der Gruppe SqlVmGroup01 und Ressourcengruppe ResourceGroup01 der SQL-virtuellen Maschine ab.</span><span class="sxs-lookup"><span data-stu-id="2539a-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="2539a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2539a-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="2539a-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="2539a-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="2539a-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="2539a-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="2539a-118">Dieser Befehl ruft Informationen zu allen Verfügbarkeitsgruppen-Listenern in der Gruppe "SqlVmGroup01" und "Ressourcengruppe ResourceGroup01" der SQL-virtuellen Maschine ab.</span><span class="sxs-lookup"><span data-stu-id="2539a-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="2539a-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2539a-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="2539a-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="2539a-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="2539a-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="2539a-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="2539a-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="2539a-122">PARAMETERS</span></span>

### <span data-ttu-id="2539a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2539a-123">-DefaultProfile</span></span>
<span data-ttu-id="2539a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2539a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2539a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2539a-125">-Name</span></span>
<span data-ttu-id="2539a-126">Listener-Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2539a-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="2539a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2539a-127">-ResourceGroupName</span></span>
<span data-ttu-id="2539a-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2539a-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="2539a-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2539a-129">-ResourceId</span></span>
<span data-ttu-id="2539a-130">Verfügbarkeitsgruppen-Listener-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2539a-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="2539a-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="2539a-131">-SqlVMGroupName</span></span>
<span data-ttu-id="2539a-132">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="2539a-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="2539a-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="2539a-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="2539a-134">Gruppenobjekt der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="2539a-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="2539a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2539a-135">CommonParameters</span></span>
<span data-ttu-id="2539a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2539a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2539a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2539a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2539a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2539a-138">INPUTS</span></span>

### <span data-ttu-id="2539a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2539a-139">System.String</span></span>

### <span data-ttu-id="2539a-140">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="2539a-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="2539a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2539a-141">OUTPUTS</span></span>

### <span data-ttu-id="2539a-142">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="2539a-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="2539a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2539a-143">NOTES</span></span>

## <span data-ttu-id="2539a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2539a-144">RELATED LINKS</span></span>
