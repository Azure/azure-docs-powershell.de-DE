---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 1949cc2a875f2e55c2d35dcbbd7b062ff2cae021
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995831"
---
# <span data-ttu-id="b4019-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b4019-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="b4019-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4019-102">SYNOPSIS</span></span>
<span data-ttu-id="b4019-103">Löscht einen vorhandenen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b4019-103">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="b4019-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4019-104">SYNTAX</span></span>

### <span data-ttu-id="b4019-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4019-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4019-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4019-106">ByResourceId</span></span>
```
Remove-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4019-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4019-107">ByInputObject</span></span>
```
Remove-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4019-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4019-108">DESCRIPTION</span></span>
<span data-ttu-id="b4019-109">Löscht einen vorhandenen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b4019-109">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="b4019-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4019-110">EXAMPLES</span></span>

### <span data-ttu-id="b4019-111">Beispiel 1: Löschen eines vorhandenen Kusto-Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="b4019-111">Example 1 - Delete an existing Kusto cluster by name</span></span>

```
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="b4019-112">Der obige Befehl löscht den Kusto-Clusternamens "mykustocluster" in der Ressourcengruppe "testrg".</span><span class="sxs-lookup"><span data-stu-id="b4019-112">The above command deletes the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="b4019-113">Beispiel 2 – Löschen eines vorhandenen Kusto-Clusters durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="b4019-113">Example 2 - Delete an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Remove-AzKustoCluster
```

<span data-ttu-id="b4019-114">Der obige Befehl ruft den Kusto-Cluster mit dem Namen "mykustocluster" in der Ressourcengruppe "testrg" mit dem `Get-AzKustoCluster` Cmdlet ab und führt dann das Ergebnis aus, um `Remove-AzKustoCluster` es zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b4019-114">The above command gets the Kusto cluster named "mykustocluster" in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Remove-AzKustoCluster` to delete it.</span></span>

## <span data-ttu-id="b4019-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4019-115">PARAMETERS</span></span>

### <span data-ttu-id="b4019-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4019-116">-DefaultProfile</span></span>
<span data-ttu-id="b4019-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4019-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4019-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4019-118">-InputObject</span></span>
<span data-ttu-id="b4019-119">Kusto-Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="b4019-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4019-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b4019-120">-Name</span></span>
<span data-ttu-id="b4019-121">Der Name des Clusters, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4019-121">Name of cluster to be removed.</span></span>

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

### <span data-ttu-id="b4019-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4019-122">-PassThru</span></span>
<span data-ttu-id="b4019-123">Gibt zurück, ob der angegebene Cluster erfolgreich gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="b4019-123">Return whether the specified cluster was successfully deleted or not.</span></span>

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

### <span data-ttu-id="b4019-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4019-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4019-125">Der Name der Ressourcengruppe, unter der der Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b4019-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="b4019-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b4019-126">-ResourceId</span></span>
<span data-ttu-id="b4019-127">Kusto-Cluster-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="b4019-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="b4019-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4019-128">-Confirm</span></span>
<span data-ttu-id="b4019-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4019-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4019-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4019-130">-WhatIf</span></span>
<span data-ttu-id="b4019-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4019-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4019-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4019-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4019-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4019-133">CommonParameters</span></span>
<span data-ttu-id="b4019-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4019-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4019-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4019-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4019-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4019-136">INPUTS</span></span>

### <span data-ttu-id="b4019-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b4019-137">System.String</span></span>

### <span data-ttu-id="b4019-138">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b4019-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="b4019-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4019-139">OUTPUTS</span></span>

### <span data-ttu-id="b4019-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4019-140">System.Boolean</span></span>

## <span data-ttu-id="b4019-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4019-141">NOTES</span></span>

## <span data-ttu-id="b4019-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4019-142">RELATED LINKS</span></span>
