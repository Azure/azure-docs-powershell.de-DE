---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156156"
---
# <span data-ttu-id="ed8d8-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ed8d8-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="ed8d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8d8-103">Entfernt eine azure SQL verwaltete Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="ed8d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed8d8-104">SYNTAX</span></span>

### <span data-ttu-id="ed8d8-105">RemoveInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed8d8-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8d8-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ed8d8-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8d8-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8d8-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8d8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed8d8-108">DESCRIPTION</span></span>
<span data-ttu-id="ed8d8-109">Das **Cmdlet "Remove-AzSqlInstance"** entfernt eine azure SQL Datenbank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="ed8d8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed8d8-110">EXAMPLES</span></span>

### <span data-ttu-id="ed8d8-111">Beispiel 1: Entfernen einer Instanz</span><span class="sxs-lookup"><span data-stu-id="ed8d8-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ed8d8-112">Mit diesem Befehl wird die Instanz namens "managedInstance1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="ed8d8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed8d8-113">PARAMETERS</span></span>

### <span data-ttu-id="ed8d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8d8-114">-DefaultProfile</span></span>
<span data-ttu-id="ed8d8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed8d8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ed8d8-116">-Force</span></span>
<span data-ttu-id="ed8d8-117">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="ed8d8-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ed8d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed8d8-118">-InputObject</span></span>
<span data-ttu-id="ed8d8-119">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="ed8d8-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="ed8d8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ed8d8-120">-Name</span></span>
<span data-ttu-id="ed8d8-121">SQL Den Namen der Instanz.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-121">SQL instance name.</span></span>

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

### <span data-ttu-id="ed8d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed8d8-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed8d8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8d8-124">-ResourceId</span></span>
<span data-ttu-id="ed8d8-125">Die Ressourcen-ID des zu entfernende Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="ed8d8-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="ed8d8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed8d8-126">-Confirm</span></span>
<span data-ttu-id="ed8d8-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8d8-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed8d8-128">-WhatIf</span></span>
<span data-ttu-id="ed8d8-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed8d8-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed8d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8d8-131">CommonParameters</span></span>
<span data-ttu-id="ed8d8-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8d8-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed8d8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8d8-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed8d8-134">INPUTS</span></span>

### <span data-ttu-id="ed8d8-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ed8d8-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="ed8d8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ed8d8-136">System.String</span></span>

## <span data-ttu-id="ed8d8-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed8d8-137">OUTPUTS</span></span>

### <span data-ttu-id="ed8d8-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ed8d8-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="ed8d8-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed8d8-139">NOTES</span></span>

## <span data-ttu-id="ed8d8-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed8d8-140">RELATED LINKS</span></span>
