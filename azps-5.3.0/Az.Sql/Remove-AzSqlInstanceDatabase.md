---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460612"
---
# <span data-ttu-id="0c39b-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0c39b-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="0c39b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c39b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c39b-103">Entfernt eine Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="0c39b-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="0c39b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c39b-104">SYNTAX</span></span>

### <span data-ttu-id="0c39b-105">RemoveInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c39b-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c39b-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="0c39b-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c39b-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="0c39b-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c39b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c39b-108">DESCRIPTION</span></span>
<span data-ttu-id="0c39b-109">Das **Cmdlet "Remove-AzSqlInstanceDatabase"** entfernt eine Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="0c39b-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="0c39b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c39b-110">EXAMPLES</span></span>

### <span data-ttu-id="0c39b-111">Beispiel 1: Entfernen einer Datenbank aus einer Instanz</span><span class="sxs-lookup"><span data-stu-id="0c39b-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0c39b-112">Mit diesem Befehl wird die Datenbank mit dem Namen "Database01" aus der Instanz "managedInstance1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c39b-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="0c39b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c39b-113">PARAMETERS</span></span>

### <span data-ttu-id="0c39b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c39b-114">-DefaultProfile</span></span>
<span data-ttu-id="0c39b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c39b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c39b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0c39b-116">-Force</span></span>
<span data-ttu-id="0c39b-117">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="0c39b-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0c39b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c39b-118">-InputObject</span></span>
<span data-ttu-id="0c39b-119">Das zu entfernende Instanzdatenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="0c39b-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c39b-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0c39b-120">-InstanceName</span></span>
<span data-ttu-id="0c39b-121">Der Instanzname.</span><span class="sxs-lookup"><span data-stu-id="0c39b-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c39b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0c39b-122">-Name</span></span>
<span data-ttu-id="0c39b-123">Der Name der Azure SQL-Instanzdatenbank, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c39b-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c39b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c39b-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c39b-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c39b-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c39b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c39b-126">-ResourceId</span></span>
<span data-ttu-id="0c39b-127">Die Ressourcen-ID des zu entfernende Instanzdatenbankobjekts</span><span class="sxs-lookup"><span data-stu-id="0c39b-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c39b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c39b-128">-Confirm</span></span>
<span data-ttu-id="0c39b-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c39b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c39b-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0c39b-130">-WhatIf</span></span>
<span data-ttu-id="0c39b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c39b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c39b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c39b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c39b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c39b-133">CommonParameters</span></span>
<span data-ttu-id="0c39b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c39b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c39b-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c39b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c39b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c39b-136">INPUTS</span></span>

### <span data-ttu-id="0c39b-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0c39b-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="0c39b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0c39b-138">System.String</span></span>

## <span data-ttu-id="0c39b-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c39b-139">OUTPUTS</span></span>

### <span data-ttu-id="0c39b-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0c39b-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="0c39b-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0c39b-141">NOTES</span></span>

## <span data-ttu-id="0c39b-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0c39b-142">RELATED LINKS</span></span>
