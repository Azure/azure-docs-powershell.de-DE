---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: 09aa7daaa3a583e42481e29675a08e8e1dd94d3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825403"
---
# <span data-ttu-id="4e68a-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4e68a-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="4e68a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e68a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e68a-103">Entfernt eine Azure SQL-Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="4e68a-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="4e68a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e68a-104">SYNTAX</span></span>

### <span data-ttu-id="4e68a-105">RemoveInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e68a-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e68a-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="4e68a-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e68a-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="4e68a-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e68a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e68a-108">DESCRIPTION</span></span>
<span data-ttu-id="4e68a-109">Das Cmdlet **Remove-AzSqlInstance** entfernt eine Azure SQL-Daten Bank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="4e68a-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="4e68a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e68a-110">EXAMPLES</span></span>

### <span data-ttu-id="4e68a-111">Beispiel 1: Entfernen einer Instanz</span><span class="sxs-lookup"><span data-stu-id="4e68a-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4e68a-112">Dieser Befehl entfernt die Instanz mit dem Namen managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="4e68a-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="4e68a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e68a-113">PARAMETERS</span></span>

### <span data-ttu-id="4e68a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e68a-114">-DefaultProfile</span></span>
<span data-ttu-id="4e68a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e68a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e68a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4e68a-116">-Force</span></span>
<span data-ttu-id="4e68a-117">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="4e68a-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4e68a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4e68a-118">-InputObject</span></span>
<span data-ttu-id="4e68a-119">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="4e68a-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4e68a-120">-Name</span></span>
<span data-ttu-id="4e68a-121">SQL-Instanzenname</span><span class="sxs-lookup"><span data-stu-id="4e68a-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e68a-122">-ResourceGroupName</span></span>
<span data-ttu-id="4e68a-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4e68a-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4e68a-124">-ResourceId</span></span>
<span data-ttu-id="4e68a-125">Die Ressourcen-ID des zu entfernenden Instance-Objekts</span><span class="sxs-lookup"><span data-stu-id="4e68a-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e68a-126">-Confirm</span></span>
<span data-ttu-id="4e68a-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e68a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e68a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e68a-128">-WhatIf</span></span>
<span data-ttu-id="4e68a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e68a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e68a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e68a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e68a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e68a-131">CommonParameters</span></span>
<span data-ttu-id="4e68a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e68a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e68a-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e68a-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e68a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e68a-134">INPUTS</span></span>

### <span data-ttu-id="4e68a-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4e68a-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="4e68a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4e68a-136">System.String</span></span>

## <span data-ttu-id="4e68a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e68a-137">OUTPUTS</span></span>

### <span data-ttu-id="4e68a-138">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4e68a-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="4e68a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e68a-139">NOTES</span></span>

## <span data-ttu-id="4e68a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e68a-140">RELATED LINKS</span></span>
