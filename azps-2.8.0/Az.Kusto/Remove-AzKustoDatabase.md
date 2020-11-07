---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 141c601b5a903462b15bbeb45d410db24608323f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650808"
---
# <span data-ttu-id="dd880-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="dd880-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="dd880-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd880-102">SYNOPSIS</span></span>
<span data-ttu-id="dd880-103">Löscht eine vorhandene Kusto-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dd880-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="dd880-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd880-104">SYNTAX</span></span>

### <span data-ttu-id="dd880-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd880-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd880-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd880-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd880-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd880-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd880-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd880-108">DESCRIPTION</span></span>
<span data-ttu-id="dd880-109">Löscht eine vorhandene Kusto-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dd880-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="dd880-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd880-110">EXAMPLES</span></span>

### <span data-ttu-id="dd880-111">Beispiel 1: Löschen einer vorhandenen Kusto-Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="dd880-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="dd880-112">Der obige Befehl löscht die Kusto-Datenbank mit dem Namen "mykustodatabase" im Cluster "mykustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="dd880-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="dd880-113">Beispiel 2 – Löschen einer vorhandenen Kusto-Datenbank durch Piping</span><span class="sxs-lookup"><span data-stu-id="dd880-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="dd880-114">Der obige Befehl ruft die Kusto-Datenbank mit dem Namen "mykustodatabase" im Cluster "mykustocluster" ab, die in der Ressourcengruppe "testrg" mithilfe des `Get-AzKustoDatabase` Cmdlets gefunden wird, und führt dann das Ergebnis aus, um `Remove-AzKustoDatabase` es zu löschen.</span><span class="sxs-lookup"><span data-stu-id="dd880-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="dd880-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd880-115">PARAMETERS</span></span>

### <span data-ttu-id="dd880-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="dd880-116">-ClusterName</span></span>
<span data-ttu-id="dd880-117">Der Name des Clusters, unter dem die Datenbank vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dd880-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd880-118">-DefaultProfile</span></span>
<span data-ttu-id="dd880-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd880-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd880-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd880-120">-InputObject</span></span>
<span data-ttu-id="dd880-121">Kusto-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="dd880-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dd880-122">-Name</span></span>
<span data-ttu-id="dd880-123">Der Name der zu entfernende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dd880-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd880-124">-PassThru</span></span>
<span data-ttu-id="dd880-125">Gibt zurück, ob die angegebene Datenbank erfolgreich angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="dd880-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="dd880-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd880-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd880-127">Der Name der Ressourcengruppe, unter der der Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dd880-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dd880-128">-ResourceId</span></span>
<span data-ttu-id="dd880-129">Kusto-Datenbank-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="dd880-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd880-130">-Confirm</span></span>
<span data-ttu-id="dd880-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd880-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd880-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd880-132">-WhatIf</span></span>
<span data-ttu-id="dd880-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd880-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd880-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd880-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd880-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd880-135">CommonParameters</span></span>
<span data-ttu-id="dd880-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd880-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd880-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd880-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd880-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd880-138">INPUTS</span></span>

### <span data-ttu-id="dd880-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dd880-139">System.String</span></span>

### <span data-ttu-id="dd880-140">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="dd880-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="dd880-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd880-141">OUTPUTS</span></span>

### <span data-ttu-id="dd880-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd880-142">System.Boolean</span></span>

## <span data-ttu-id="dd880-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd880-143">NOTES</span></span>

## <span data-ttu-id="dd880-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd880-144">RELATED LINKS</span></span>
