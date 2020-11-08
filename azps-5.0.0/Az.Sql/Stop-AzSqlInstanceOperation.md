---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178491"
---
# <span data-ttu-id="813e3-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="813e3-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="813e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="813e3-102">SYNOPSIS</span></span>
<span data-ttu-id="813e3-103">Beendet die Vorgänge einer SQL-verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="813e3-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="813e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="813e3-104">SYNTAX</span></span>

### <span data-ttu-id="813e3-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="813e3-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="813e3-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="813e3-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="813e3-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="813e3-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="813e3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="813e3-108">DESCRIPTION</span></span>
<span data-ttu-id="813e3-109">Das Stop-AzSqlInstanceOperation-Cmdlet beendet den Vorgang mit dem angegebenen Vorgangsnamen in einer verwalteten SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="813e3-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="813e3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="813e3-110">EXAMPLES</span></span>

### <span data-ttu-id="813e3-111">Beispiel 1: Abrufen eines bestimmten Vorgangs</span><span class="sxs-lookup"><span data-stu-id="813e3-111">Example 1: Get a specific operation</span></span>
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

<span data-ttu-id="813e3-112">Dieser Befehl beendet den Vorgang mit dem Namen "d0f5bef5-e2b1-4ef8-BB42-2e54073874f9" auf einer verwalteten SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="813e3-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="813e3-113">Beispiel 2: Verwenden der Vorgangs Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="813e3-113">Example 2: Using operation resource id</span></span>
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

<span data-ttu-id="813e3-114">Dieser Befehl beendet den Vorgang mit der Ressourcen-ID $managedInstanceOperation. ID.</span><span class="sxs-lookup"><span data-stu-id="813e3-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="813e3-115">Beispiel 3: Verwenden des Vorgangs Objekts</span><span class="sxs-lookup"><span data-stu-id="813e3-115">Example 3: Using operation object</span></span>
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

<span data-ttu-id="813e3-116">Mit diesem Befehl wird der Vorgang mit Objekt $managedInstanceOperation beendet.</span><span class="sxs-lookup"><span data-stu-id="813e3-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="813e3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="813e3-117">PARAMETERS</span></span>

### <span data-ttu-id="813e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813e3-118">-DefaultProfile</span></span>
<span data-ttu-id="813e3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="813e3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="813e3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="813e3-120">-Force</span></span>
<span data-ttu-id="813e3-121">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="813e3-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="813e3-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="813e3-122">-InputObject</span></span>
<span data-ttu-id="813e3-123">Der Vorgang, der abgebrochen werden soll</span><span class="sxs-lookup"><span data-stu-id="813e3-123">The operation to cancel</span></span>

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

### <span data-ttu-id="813e3-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="813e3-124">-ManagedInstanceName</span></span>
<span data-ttu-id="813e3-125">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="813e3-125">The name of the instance.</span></span>

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

### <span data-ttu-id="813e3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="813e3-126">-Name</span></span>
<span data-ttu-id="813e3-127">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="813e3-127">The name of the operation.</span></span>

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

### <span data-ttu-id="813e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="813e3-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="813e3-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="813e3-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="813e3-130">-ResourceId</span></span>
<span data-ttu-id="813e3-131">Die Ressourcen-ID des zu beendenden Vorgangs Objekts</span><span class="sxs-lookup"><span data-stu-id="813e3-131">The resource id of operation object to stop</span></span>

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

### <span data-ttu-id="813e3-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="813e3-132">-Confirm</span></span>
<span data-ttu-id="813e3-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="813e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="813e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="813e3-134">-WhatIf</span></span>
<span data-ttu-id="813e3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="813e3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="813e3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="813e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="813e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813e3-137">CommonParameters</span></span>
<span data-ttu-id="813e3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="813e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813e3-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="813e3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813e3-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="813e3-140">INPUTS</span></span>

### <span data-ttu-id="813e3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="813e3-141">System.String</span></span>

### <span data-ttu-id="813e3-142">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="813e3-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="813e3-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="813e3-143">OUTPUTS</span></span>

### <span data-ttu-id="813e3-144">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="813e3-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="813e3-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="813e3-145">NOTES</span></span>

## <span data-ttu-id="813e3-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="813e3-146">RELATED LINKS</span></span>
