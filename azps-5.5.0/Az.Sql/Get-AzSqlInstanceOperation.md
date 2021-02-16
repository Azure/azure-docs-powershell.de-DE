---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150548"
---
# <span data-ttu-id="71c41-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="71c41-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="71c41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71c41-102">SYNOPSIS</span></span>
<span data-ttu-id="71c41-103">Ruft die SQL einer verwalteten Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="71c41-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="71c41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71c41-104">SYNTAX</span></span>

### <span data-ttu-id="71c41-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="71c41-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71c41-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="71c41-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71c41-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="71c41-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71c41-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71c41-108">DESCRIPTION</span></span>
<span data-ttu-id="71c41-109">Das Get-AzSqlInstanceOperation cmdlet ruft Informationen zu den Vorgängen in einer verwalteten instanz SQL ab.</span><span class="sxs-lookup"><span data-stu-id="71c41-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="71c41-110">Sie können alle Vorgänge in einer verwalteten Instanz oder einen bestimmten Vorgang anzeigen, indem Sie den Namen des Vorgangs eingeben.</span><span class="sxs-lookup"><span data-stu-id="71c41-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="71c41-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71c41-111">EXAMPLES</span></span>

### <span data-ttu-id="71c41-112">Beispiel 1: Alle Vorgänge der Instanz erhalten</span><span class="sxs-lookup"><span data-stu-id="71c41-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="71c41-113">Dieser Befehl ruft alle Vorgänge als verwaltete SQL ab.</span><span class="sxs-lookup"><span data-stu-id="71c41-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="71c41-114">Beispiel 2: Erhalten eines bestimmten Vorgangs</span><span class="sxs-lookup"><span data-stu-id="71c41-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="71c41-115">Dieser Befehl ruft den Vorgang mit dem Namen '5870c6d8-6703-4b27-8ae4-687b4ca7caea' für eine verwaltete instanz SQL ab.</span><span class="sxs-lookup"><span data-stu-id="71c41-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="71c41-116">Beispiel 3: Verwenden der Vorgangsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="71c41-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="71c41-117">Dieser Befehl ruft den Vorgang mit id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span><span class="sxs-lookup"><span data-stu-id="71c41-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="71c41-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71c41-118">PARAMETERS</span></span>

### <span data-ttu-id="71c41-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c41-119">-DefaultProfile</span></span>
<span data-ttu-id="71c41-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71c41-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71c41-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="71c41-121">-ManagedInstanceName</span></span>
<span data-ttu-id="71c41-122">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="71c41-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c41-123">-Name</span><span class="sxs-lookup"><span data-stu-id="71c41-123">-Name</span></span>
<span data-ttu-id="71c41-124">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="71c41-124">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c41-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c41-125">-ResourceGroupName</span></span>
<span data-ttu-id="71c41-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71c41-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c41-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71c41-127">-ResourceId</span></span>
<span data-ttu-id="71c41-128">Der Ressourcenbezeichner für den Verwalteten Instanzvorgang.</span><span class="sxs-lookup"><span data-stu-id="71c41-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c41-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c41-129">CommonParameters</span></span>
<span data-ttu-id="71c41-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c41-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c41-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71c41-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c41-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71c41-132">INPUTS</span></span>

### <span data-ttu-id="71c41-133">System.String</span><span class="sxs-lookup"><span data-stu-id="71c41-133">System.String</span></span>

## <span data-ttu-id="71c41-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71c41-134">OUTPUTS</span></span>

### <span data-ttu-id="71c41-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="71c41-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="71c41-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71c41-136">NOTES</span></span>

## <span data-ttu-id="71c41-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71c41-137">RELATED LINKS</span></span>
