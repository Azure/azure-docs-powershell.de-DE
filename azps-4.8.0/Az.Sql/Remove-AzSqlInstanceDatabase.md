---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174111"
---
# <span data-ttu-id="5f323-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5f323-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="5f323-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f323-102">SYNOPSIS</span></span>
<span data-ttu-id="5f323-103">Entfernt eine Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5f323-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="5f323-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f323-104">SYNTAX</span></span>

### <span data-ttu-id="5f323-105">RemoveInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f323-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f323-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="5f323-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f323-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="5f323-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f323-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f323-108">DESCRIPTION</span></span>
<span data-ttu-id="5f323-109">Das Cmdlet " **Remove-AzSqlInstanceDatabase** " entfernt eine Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5f323-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="5f323-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f323-110">EXAMPLES</span></span>

### <span data-ttu-id="5f323-111">Beispiel 1: Entfernen einer Datenbank aus einer Instanz</span><span class="sxs-lookup"><span data-stu-id="5f323-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5f323-112">Dieser Befehl entfernt die Datenbank mit dem Namen database01 aus der Instanz managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="5f323-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="5f323-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f323-113">PARAMETERS</span></span>

### <span data-ttu-id="5f323-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f323-114">-DefaultProfile</span></span>
<span data-ttu-id="5f323-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f323-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f323-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5f323-116">-Force</span></span>
<span data-ttu-id="5f323-117">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="5f323-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5f323-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f323-118">-InputObject</span></span>
<span data-ttu-id="5f323-119">Das zu entfernende Instanzendaten Bank Objekt</span><span class="sxs-lookup"><span data-stu-id="5f323-119">The Instance Database object to remove</span></span>

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

### <span data-ttu-id="5f323-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5f323-120">-InstanceName</span></span>
<span data-ttu-id="5f323-121">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="5f323-121">The instance name.</span></span>

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

### <span data-ttu-id="5f323-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5f323-122">-Name</span></span>
<span data-ttu-id="5f323-123">Der Name der zu entfernenden Azure SQL-Instanzen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5f323-123">The name of the Azure SQL Instance Database to remove.</span></span>

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

### <span data-ttu-id="5f323-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f323-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f323-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f323-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="5f323-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5f323-126">-ResourceId</span></span>
<span data-ttu-id="5f323-127">Die Ressourcen-ID des zu entfernenden Instanz-Datenbankobjekts</span><span class="sxs-lookup"><span data-stu-id="5f323-127">The resource id of Instance Database object to remove</span></span>

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

### <span data-ttu-id="5f323-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f323-128">-Confirm</span></span>
<span data-ttu-id="5f323-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f323-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f323-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f323-130">-WhatIf</span></span>
<span data-ttu-id="5f323-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f323-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f323-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f323-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f323-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f323-133">CommonParameters</span></span>
<span data-ttu-id="5f323-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f323-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f323-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f323-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f323-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f323-136">INPUTS</span></span>

### <span data-ttu-id="5f323-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5f323-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="5f323-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5f323-138">System.String</span></span>

## <span data-ttu-id="5f323-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f323-139">OUTPUTS</span></span>

### <span data-ttu-id="5f323-140">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5f323-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="5f323-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f323-141">NOTES</span></span>

## <span data-ttu-id="5f323-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f323-142">RELATED LINKS</span></span>
