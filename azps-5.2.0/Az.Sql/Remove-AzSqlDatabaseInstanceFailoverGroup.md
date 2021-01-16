---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299787"
---
# <span data-ttu-id="6e8e0-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6e8e0-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="6e8e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8e0-103">Entfernt eine Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="6e8e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e8e0-104">SYNTAX</span></span>

### <span data-ttu-id="6e8e0-105">RemoveIFGDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e8e0-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e8e0-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e8e0-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e8e0-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="6e8e0-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8e0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e8e0-108">DESCRIPTION</span></span>
<span data-ttu-id="6e8e0-109">Mit diesem Befehl wird die Instanz failovergruppe mit dem angegebenen Namen entfernt, und alle Datenbanken bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="6e8e0-110">Die Registrierung des Listenerendpunkts wird im DNS aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="6e8e0-111">Der primäre Bereich der Instanz failover group sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="6e8e0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e8e0-112">EXAMPLES</span></span>

### <span data-ttu-id="6e8e0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6e8e0-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="6e8e0-114">Entfernen sie eine Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="6e8e0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e8e0-115">PARAMETERS</span></span>

### <span data-ttu-id="6e8e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8e0-116">-DefaultProfile</span></span>
<span data-ttu-id="6e8e0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e8e0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6e8e0-118">-Force</span></span>
<span data-ttu-id="6e8e0-119">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="6e8e0-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="6e8e0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e8e0-120">-InputObject</span></span>
<span data-ttu-id="6e8e0-121">Das zu entfernende Instanz-Failovergruppenobjekt</span><span class="sxs-lookup"><span data-stu-id="6e8e0-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8e0-122">-Location</span><span class="sxs-lookup"><span data-stu-id="6e8e0-122">-Location</span></span>
<span data-ttu-id="6e8e0-123">Der Name der lokalen Region, aus der die Instanz failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8e0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6e8e0-124">-Name</span></span>
<span data-ttu-id="6e8e0-125">Der Name der zu entfernende Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8e0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e8e0-126">-PassThru</span></span>
<span data-ttu-id="6e8e0-127">Gibt an, ob die Ausgabe der Cmdletausführung übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="6e8e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e8e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e8e0-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8e0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e8e0-130">-ResourceId</span></span>
<span data-ttu-id="6e8e0-131">Die Ressourcen-ID der zu entfernende Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8e0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e8e0-132">-Confirm</span></span>
<span data-ttu-id="6e8e0-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8e0-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6e8e0-134">-WhatIf</span></span>
<span data-ttu-id="6e8e0-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e8e0-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e8e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8e0-137">CommonParameters</span></span>
<span data-ttu-id="6e8e0-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e8e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8e0-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e8e0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8e0-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e8e0-140">INPUTS</span></span>

### <span data-ttu-id="6e8e0-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6e8e0-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="6e8e0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6e8e0-142">System.String</span></span>

## <span data-ttu-id="6e8e0-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e8e0-143">OUTPUTS</span></span>

### <span data-ttu-id="6e8e0-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6e8e0-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="6e8e0-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6e8e0-145">NOTES</span></span>

## <span data-ttu-id="6e8e0-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6e8e0-146">RELATED LINKS</span></span>
