---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370571"
---
# <span data-ttu-id="c1bea-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="c1bea-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="c1bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1bea-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bea-103">Beendet die SQL einer verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="c1bea-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="c1bea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1bea-104">SYNTAX</span></span>

### <span data-ttu-id="c1bea-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1bea-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1bea-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1bea-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1bea-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1bea-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1bea-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1bea-108">DESCRIPTION</span></span>
<span data-ttu-id="c1bea-109">Das Stop-AzSqlInstanceOperation cmdlet beendet den Vorgang mit dem angegebenen Vorgangsnamen in SQL verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="c1bea-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="c1bea-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1bea-110">EXAMPLES</span></span>

### <span data-ttu-id="c1bea-111">Beispiel 1: Erhalten eines bestimmten Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c1bea-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="c1bea-112">Dieser Befehl beendet den Vorgang mit dem Namen 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' für eine verwaltete SQL Instanz.</span><span class="sxs-lookup"><span data-stu-id="c1bea-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="c1bea-113">Beispiel 2: Verwenden der Vorgangsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c1bea-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="c1bea-114">Dieser Befehl beendet den Vorgang mit der Ressourcen-ID $managedInstanceOperation.Id.</span><span class="sxs-lookup"><span data-stu-id="c1bea-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="c1bea-115">Beispiel 3: Verwenden des Vorgangsobjekts</span><span class="sxs-lookup"><span data-stu-id="c1bea-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="c1bea-116">Dieser Befehl beendet den Vorgang mit $managedInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="c1bea-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="c1bea-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1bea-117">PARAMETERS</span></span>

### <span data-ttu-id="c1bea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1bea-118">-DefaultProfile</span></span>
<span data-ttu-id="c1bea-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1bea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1bea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c1bea-120">-Force</span></span>
<span data-ttu-id="c1bea-121">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="c1bea-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c1bea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1bea-122">-InputObject</span></span>
<span data-ttu-id="c1bea-123">Der vorgang, der abgebrochen werden soll</span><span class="sxs-lookup"><span data-stu-id="c1bea-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="c1bea-124">-ManagedInstanceName</span></span>
<span data-ttu-id="c1bea-125">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="c1bea-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c1bea-126">-Name</span></span>
<span data-ttu-id="c1bea-127">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c1bea-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1bea-128">-ResourceGroupName</span></span>
<span data-ttu-id="c1bea-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c1bea-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1bea-130">-ResourceId</span></span>
<span data-ttu-id="c1bea-131">Die Ressourcen-ID des zu beendende Vorgangsobjekts</span><span class="sxs-lookup"><span data-stu-id="c1bea-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1bea-132">-Confirm</span></span>
<span data-ttu-id="c1bea-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1bea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1bea-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c1bea-134">-WhatIf</span></span>
<span data-ttu-id="c1bea-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1bea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1bea-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1bea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1bea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bea-137">CommonParameters</span></span>
<span data-ttu-id="c1bea-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1bea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bea-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1bea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bea-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1bea-140">INPUTS</span></span>

### <span data-ttu-id="c1bea-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c1bea-141">System.String</span></span>

### <span data-ttu-id="c1bea-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="c1bea-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="c1bea-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1bea-143">OUTPUTS</span></span>

### <span data-ttu-id="c1bea-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="c1bea-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="c1bea-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1bea-145">NOTES</span></span>

## <span data-ttu-id="c1bea-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1bea-146">RELATED LINKS</span></span>
