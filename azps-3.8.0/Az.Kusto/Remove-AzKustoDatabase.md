---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 47b519b324018e4fc369d281f7fb7eac554ac571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995829"
---
# <span data-ttu-id="bcf73-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="bcf73-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="bcf73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bcf73-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf73-103">Löscht eine vorhandene Kusto-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bcf73-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="bcf73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcf73-104">SYNTAX</span></span>

### <span data-ttu-id="bcf73-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcf73-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf73-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf73-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf73-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bcf73-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf73-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bcf73-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf73-109">Löscht eine vorhandene Kusto-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bcf73-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="bcf73-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bcf73-110">EXAMPLES</span></span>

### <span data-ttu-id="bcf73-111">Beispiel 1: Löschen einer vorhandenen Kusto-Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="bcf73-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="bcf73-112">Der obige Befehl löscht die Kusto-Datenbank mit dem Namen "mykustodatabase" im Cluster "mykustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="bcf73-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="bcf73-113">Beispiel 2 – Löschen einer vorhandenen Kusto-Datenbank durch Piping</span><span class="sxs-lookup"><span data-stu-id="bcf73-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="bcf73-114">Der obige Befehl ruft die Kusto-Datenbank mit dem Namen "mykustodatabase" im Cluster "mykustocluster" ab, die in der Ressourcengruppe "testrg" mithilfe des `Get-AzKustoDatabase` Cmdlets gefunden wird, und führt dann das Ergebnis aus, um `Remove-AzKustoDatabase` es zu löschen.</span><span class="sxs-lookup"><span data-stu-id="bcf73-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="bcf73-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcf73-115">PARAMETERS</span></span>

### <span data-ttu-id="bcf73-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="bcf73-116">-ClusterName</span></span>
<span data-ttu-id="bcf73-117">Der Name des Clusters, unter dem die Datenbank vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bcf73-117">Name of the cluster under which the database exists.</span></span>

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

### <span data-ttu-id="bcf73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf73-118">-DefaultProfile</span></span>
<span data-ttu-id="bcf73-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bcf73-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf73-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bcf73-120">-InputObject</span></span>
<span data-ttu-id="bcf73-121">Kusto-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="bcf73-121">Kusto database object.</span></span>

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

### <span data-ttu-id="bcf73-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bcf73-122">-Name</span></span>
<span data-ttu-id="bcf73-123">Der Name der zu entfernende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bcf73-123">Name of database to be removed.</span></span>

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

### <span data-ttu-id="bcf73-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcf73-124">-PassThru</span></span>
<span data-ttu-id="bcf73-125">Gibt zurück, ob die angegebene Datenbank erfolgreich angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="bcf73-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="bcf73-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf73-126">-ResourceGroupName</span></span>
<span data-ttu-id="bcf73-127">Der Name der Ressourcengruppe, unter der der Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bcf73-127">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="bcf73-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bcf73-128">-ResourceId</span></span>
<span data-ttu-id="bcf73-129">Kusto-Datenbank-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="bcf73-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="bcf73-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bcf73-130">-Confirm</span></span>
<span data-ttu-id="bcf73-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcf73-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf73-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf73-132">-WhatIf</span></span>
<span data-ttu-id="bcf73-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcf73-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf73-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcf73-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf73-135">CommonParameters</span></span>
<span data-ttu-id="bcf73-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf73-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf73-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf73-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bcf73-138">INPUTS</span></span>

### <span data-ttu-id="bcf73-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bcf73-139">System.String</span></span>

### <span data-ttu-id="bcf73-140">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="bcf73-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="bcf73-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bcf73-141">OUTPUTS</span></span>

### <span data-ttu-id="bcf73-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcf73-142">System.Boolean</span></span>

## <span data-ttu-id="bcf73-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="bcf73-143">NOTES</span></span>

## <span data-ttu-id="bcf73-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bcf73-144">RELATED LINKS</span></span>
