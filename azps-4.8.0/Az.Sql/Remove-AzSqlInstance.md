---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174115"
---
# <span data-ttu-id="039ca-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="039ca-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="039ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="039ca-102">SYNOPSIS</span></span>
<span data-ttu-id="039ca-103">Entfernt eine Azure SQL-Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="039ca-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="039ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="039ca-104">SYNTAX</span></span>

### <span data-ttu-id="039ca-105">RemoveInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="039ca-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039ca-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="039ca-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039ca-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="039ca-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="039ca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="039ca-108">DESCRIPTION</span></span>
<span data-ttu-id="039ca-109">Das Cmdlet **Remove-AzSqlInstance** entfernt eine Azure SQL-Daten Bank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="039ca-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="039ca-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="039ca-110">EXAMPLES</span></span>

### <span data-ttu-id="039ca-111">Beispiel 1: Entfernen einer Instanz</span><span class="sxs-lookup"><span data-stu-id="039ca-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="039ca-112">Dieser Befehl entfernt die Instanz mit dem Namen managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="039ca-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="039ca-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="039ca-113">PARAMETERS</span></span>

### <span data-ttu-id="039ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039ca-114">-DefaultProfile</span></span>
<span data-ttu-id="039ca-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="039ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="039ca-116">-Force</span><span class="sxs-lookup"><span data-stu-id="039ca-116">-Force</span></span>
<span data-ttu-id="039ca-117">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="039ca-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="039ca-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="039ca-118">-InputObject</span></span>
<span data-ttu-id="039ca-119">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="039ca-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="039ca-120">-Name</span><span class="sxs-lookup"><span data-stu-id="039ca-120">-Name</span></span>
<span data-ttu-id="039ca-121">SQL-Instanzenname</span><span class="sxs-lookup"><span data-stu-id="039ca-121">SQL instance name.</span></span>

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

### <span data-ttu-id="039ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="039ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="039ca-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="039ca-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="039ca-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="039ca-124">-ResourceId</span></span>
<span data-ttu-id="039ca-125">Die Ressourcen-ID des zu entfernenden Instance-Objekts</span><span class="sxs-lookup"><span data-stu-id="039ca-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="039ca-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="039ca-126">-Confirm</span></span>
<span data-ttu-id="039ca-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="039ca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="039ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="039ca-128">-WhatIf</span></span>
<span data-ttu-id="039ca-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="039ca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="039ca-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="039ca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="039ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039ca-131">CommonParameters</span></span>
<span data-ttu-id="039ca-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="039ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039ca-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="039ca-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039ca-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="039ca-134">INPUTS</span></span>

### <span data-ttu-id="039ca-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="039ca-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="039ca-136">System. String</span><span class="sxs-lookup"><span data-stu-id="039ca-136">System.String</span></span>

## <span data-ttu-id="039ca-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="039ca-137">OUTPUTS</span></span>

### <span data-ttu-id="039ca-138">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="039ca-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="039ca-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="039ca-139">NOTES</span></span>

## <span data-ttu-id="039ca-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="039ca-140">RELATED LINKS</span></span>
