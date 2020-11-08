---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179570"
---
# <span data-ttu-id="1695d-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="1695d-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="1695d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1695d-102">SYNOPSIS</span></span>
<span data-ttu-id="1695d-103">Ruft die Vorgänge einer verwalteten SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="1695d-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="1695d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1695d-104">SYNTAX</span></span>

### <span data-ttu-id="1695d-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1695d-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1695d-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="1695d-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1695d-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="1695d-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1695d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1695d-108">DESCRIPTION</span></span>
<span data-ttu-id="1695d-109">Das Get-AzSqlInstanceOperation-Cmdlet ruft Informationen zu den Vorgängen in einer verwalteten SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="1695d-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="1695d-110">Sie können alle Vorgänge in einer verwalteten Instanz anzeigen oder einen bestimmten Vorgang anzeigen, indem Sie den Vorgangsnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="1695d-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="1695d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1695d-111">EXAMPLES</span></span>

### <span data-ttu-id="1695d-112">Beispiel 1: Abrufen aller Instanzen Vorgänge</span><span class="sxs-lookup"><span data-stu-id="1695d-112">Example 1: Get all instance's operations</span></span>
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

<span data-ttu-id="1695d-113">Dieser Befehl ruft alle Vorgänge einer verwalteten SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="1695d-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="1695d-114">Beispiel 2: Abrufen eines bestimmten Vorgangs</span><span class="sxs-lookup"><span data-stu-id="1695d-114">Example 2: Get a specific operation</span></span>
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

<span data-ttu-id="1695d-115">Dieser Befehl ruft den Vorgang mit dem Namen "5870c6d8-6703-4b27-8AE4-687b4ca7caea" auf einer verwalteten SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="1695d-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="1695d-116">Beispiel 3: Verwenden der Vorgangs Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1695d-116">Example 3: Using operation resource id</span></span>
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

<span data-ttu-id="1695d-117">Dieser Befehl ruft den Vorgang mit der ID "/Subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/Providers/Microsoft.SQL/managedInstances/ps3698/Operations/5870c6d8-6703-4b27-8AE4-687b4ca7caea" ab.</span><span class="sxs-lookup"><span data-stu-id="1695d-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="1695d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="1695d-118">PARAMETERS</span></span>

### <span data-ttu-id="1695d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1695d-119">-DefaultProfile</span></span>
<span data-ttu-id="1695d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1695d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1695d-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="1695d-121">-ManagedInstanceName</span></span>
<span data-ttu-id="1695d-122">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="1695d-122">The name of the instance.</span></span>

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

### <span data-ttu-id="1695d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1695d-123">-Name</span></span>
<span data-ttu-id="1695d-124">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1695d-124">The name of the operation.</span></span>

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

### <span data-ttu-id="1695d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1695d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1695d-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1695d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="1695d-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1695d-127">-ResourceId</span></span>
<span data-ttu-id="1695d-128">Der Ressourcenbezeichner des verwalteten Instanzen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1695d-128">The managed instance operation resource identifier.</span></span>

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

### <span data-ttu-id="1695d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1695d-129">CommonParameters</span></span>
<span data-ttu-id="1695d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1695d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1695d-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1695d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1695d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1695d-132">INPUTS</span></span>

### <span data-ttu-id="1695d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1695d-133">System.String</span></span>

## <span data-ttu-id="1695d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1695d-134">OUTPUTS</span></span>

### <span data-ttu-id="1695d-135">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="1695d-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="1695d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="1695d-136">NOTES</span></span>

## <span data-ttu-id="1695d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1695d-137">RELATED LINKS</span></span>
