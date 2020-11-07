---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: 342944fbd933f135f3643d4022f965405de2f1df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659050"
---
# <span data-ttu-id="d66c9-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d66c9-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="d66c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d66c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d66c9-103">Entfernt eine Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="d66c9-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d66c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d66c9-104">SYNTAX</span></span>

### <span data-ttu-id="d66c9-105">RemoveInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="d66c9-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66c9-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d66c9-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66c9-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d66c9-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d66c9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d66c9-108">DESCRIPTION</span></span>
<span data-ttu-id="d66c9-109">Das Cmdlet " **Remove-AzSqlInstanceDatabase** " entfernt eine Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="d66c9-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d66c9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d66c9-110">EXAMPLES</span></span>

### <span data-ttu-id="d66c9-111">Beispiel 1: Entfernen einer Datenbank aus einer Instanz</span><span class="sxs-lookup"><span data-stu-id="d66c9-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d66c9-112">Dieser Befehl entfernt die Datenbank mit dem Namen database01 aus der Instanz managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="d66c9-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="d66c9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d66c9-113">PARAMETERS</span></span>

### <span data-ttu-id="d66c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66c9-114">-DefaultProfile</span></span>
<span data-ttu-id="d66c9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d66c9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66c9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d66c9-116">-Force</span></span>
<span data-ttu-id="d66c9-117">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="d66c9-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d66c9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d66c9-118">-InputObject</span></span>
<span data-ttu-id="d66c9-119">Das zu entfernende Instanzendaten Bank Objekt</span><span class="sxs-lookup"><span data-stu-id="d66c9-119">The Instance Database object to remove</span></span>

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

### <span data-ttu-id="d66c9-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d66c9-120">-InstanceName</span></span>
<span data-ttu-id="d66c9-121">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="d66c9-121">The instance name.</span></span>

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

### <span data-ttu-id="d66c9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d66c9-122">-Name</span></span>
<span data-ttu-id="d66c9-123">Der Name der zu entfernenden Azure SQL-Instanzen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d66c9-123">The name of the Azure SQL Instance Database to remove.</span></span>

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

### <span data-ttu-id="d66c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="d66c9-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d66c9-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d66c9-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d66c9-126">-ResourceId</span></span>
<span data-ttu-id="d66c9-127">Die Ressourcen-ID des zu entfernenden Instanz-Datenbankobjekts</span><span class="sxs-lookup"><span data-stu-id="d66c9-127">The resource id of Instance Database object to remove</span></span>

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

### <span data-ttu-id="d66c9-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d66c9-128">-Confirm</span></span>
<span data-ttu-id="d66c9-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d66c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d66c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66c9-130">-WhatIf</span></span>
<span data-ttu-id="d66c9-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d66c9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d66c9-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d66c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d66c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66c9-133">CommonParameters</span></span>
<span data-ttu-id="d66c9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d66c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66c9-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d66c9-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66c9-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d66c9-136">INPUTS</span></span>

### <span data-ttu-id="d66c9-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d66c9-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="d66c9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d66c9-138">System.String</span></span>

## <span data-ttu-id="d66c9-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d66c9-139">OUTPUTS</span></span>

### <span data-ttu-id="d66c9-140">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d66c9-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d66c9-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d66c9-141">NOTES</span></span>

## <span data-ttu-id="d66c9-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d66c9-142">RELATED LINKS</span></span>
