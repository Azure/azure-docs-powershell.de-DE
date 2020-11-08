---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176840"
---
# <span data-ttu-id="a7de8-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a7de8-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="a7de8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7de8-102">SYNOPSIS</span></span>
<span data-ttu-id="a7de8-103">Entfernt eine Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a7de8-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="a7de8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7de8-104">SYNTAX</span></span>

### <span data-ttu-id="a7de8-105">RemoveIFGDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7de8-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7de8-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7de8-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7de8-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="a7de8-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7de8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7de8-108">DESCRIPTION</span></span>
<span data-ttu-id="a7de8-109">Mit diesem Befehl wird die Failoverclusterinstanz mit dem angegebenen Namen entfernt, sodass alle Datenbanken intakt bleiben.</span><span class="sxs-lookup"><span data-stu-id="a7de8-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="a7de8-110">Der Listener-Endpunkt wird aus DNS aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="a7de8-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="a7de8-111">Der primäre Bereich der Instanz-Failover-Gruppe sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7de8-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="a7de8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7de8-112">EXAMPLES</span></span>

### <span data-ttu-id="a7de8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7de8-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="a7de8-114">Entfernen Sie eine Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a7de8-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="a7de8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7de8-115">PARAMETERS</span></span>

### <span data-ttu-id="a7de8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7de8-116">-DefaultProfile</span></span>
<span data-ttu-id="a7de8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7de8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7de8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a7de8-118">-Force</span></span>
<span data-ttu-id="a7de8-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen.</span><span class="sxs-lookup"><span data-stu-id="a7de8-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="a7de8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7de8-120">-InputObject</span></span>
<span data-ttu-id="a7de8-121">Das zu entfernende Instanzen-Failover-Gruppenobjekt</span><span class="sxs-lookup"><span data-stu-id="a7de8-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="a7de8-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="a7de8-122">-Location</span></span>
<span data-ttu-id="a7de8-123">Der Name des lokalen Bereichs, aus dem die Gruppe der Instanz-Failover abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7de8-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="a7de8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a7de8-124">-Name</span></span>
<span data-ttu-id="a7de8-125">Der Name der zu entfernenden Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a7de8-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="a7de8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7de8-126">-PassThru</span></span>
<span data-ttu-id="a7de8-127">Gibt an, ob die Ausgabe der Cmdlet-Ausführung übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7de8-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="a7de8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7de8-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7de8-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7de8-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7de8-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a7de8-130">-ResourceId</span></span>
<span data-ttu-id="a7de8-131">Die Ressourcen-ID der zu entfernenden Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a7de8-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="a7de8-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7de8-132">-Confirm</span></span>
<span data-ttu-id="a7de8-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7de8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7de8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7de8-134">-WhatIf</span></span>
<span data-ttu-id="a7de8-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7de8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7de8-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7de8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7de8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7de8-137">CommonParameters</span></span>
<span data-ttu-id="a7de8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7de8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7de8-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7de8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7de8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7de8-140">INPUTS</span></span>

### <span data-ttu-id="a7de8-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="a7de8-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="a7de8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a7de8-142">System.String</span></span>

## <span data-ttu-id="a7de8-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7de8-143">OUTPUTS</span></span>

### <span data-ttu-id="a7de8-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="a7de8-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="a7de8-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7de8-145">NOTES</span></span>

## <span data-ttu-id="a7de8-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7de8-146">RELATED LINKS</span></span>
