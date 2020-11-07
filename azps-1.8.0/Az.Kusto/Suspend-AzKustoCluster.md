---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/suspend-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
ms.openlocfilehash: 6eceaffb371226c9dda0099a32a309272d6bdb3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819439"
---
# <span data-ttu-id="3d50a-101">Suspend-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3d50a-101">Suspend-AzKustoCluster</span></span>

## <span data-ttu-id="3d50a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d50a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d50a-103">Sperren eines vorhandenen Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="3d50a-103">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="3d50a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d50a-104">SYNTAX</span></span>

### <span data-ttu-id="3d50a-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d50a-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d50a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d50a-106">ByResourceId</span></span>
```
Suspend-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d50a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3d50a-107">ByInputObject</span></span>
```
Suspend-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d50a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d50a-108">DESCRIPTION</span></span>
<span data-ttu-id="3d50a-109">Sperren eines vorhandenen Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="3d50a-109">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="3d50a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d50a-110">EXAMPLES</span></span>

### <span data-ttu-id="3d50a-111">Beispiel 1 – Sperren eines vorhandenen Kusto-Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="3d50a-111">Example 1 - Suspend an existing Kusto cluster by name</span></span>

```
PS C:\> Suspend-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="3d50a-112">Der obige Befehl unterbricht den Kusto-Cluster mit dem Namen "mykustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="3d50a-112">The above command suspends the Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="3d50a-113">Beispiel 2 – Anhalten eines vorhandenen Kusto-Clusters durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="3d50a-113">Example 2 - Suspend an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Suspend-AzKustoCluster
```

<span data-ttu-id="3d50a-114">Der obige Befehl ruft den Kusto-Cluster mit dem Namen "mykustocluster" ab, der in der Ressourcengruppe "testrg" mit dem Cmdlet gefunden wird `Get-AzKustoCluster` , und leitet dann das Ergebnis an, um `Suspend-AzKustoCluster` es auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="3d50a-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Suspend-AzKustoCluster` to suspend it.</span></span>

## <span data-ttu-id="3d50a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d50a-115">PARAMETERS</span></span>

### <span data-ttu-id="3d50a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d50a-116">-DefaultProfile</span></span>
<span data-ttu-id="3d50a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d50a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d50a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d50a-118">-InputObject</span></span>
<span data-ttu-id="3d50a-119">Kusto-Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="3d50a-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="3d50a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3d50a-120">-Name</span></span>
<span data-ttu-id="3d50a-121">Der Name des Clusters, der angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d50a-121">Name of cluster to be suspend.</span></span>

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

### <span data-ttu-id="3d50a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d50a-122">-PassThru</span></span>
<span data-ttu-id="3d50a-123">Gibt zurück, ob der angegebene Cluster erfolgreich angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="3d50a-123">Return whether the specified cluster was successfully suspended or not.</span></span>

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

### <span data-ttu-id="3d50a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d50a-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d50a-125">Der Name der Ressourcengruppe, unter der der Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3d50a-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="3d50a-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3d50a-126">-ResourceId</span></span>
<span data-ttu-id="3d50a-127">Kusto-Cluster-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="3d50a-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="3d50a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d50a-128">-Confirm</span></span>
<span data-ttu-id="3d50a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d50a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d50a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d50a-130">-WhatIf</span></span>
<span data-ttu-id="3d50a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d50a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d50a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d50a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d50a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d50a-133">CommonParameters</span></span>
<span data-ttu-id="3d50a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d50a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d50a-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d50a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d50a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d50a-136">INPUTS</span></span>

### <span data-ttu-id="3d50a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3d50a-137">System.String</span></span>

### <span data-ttu-id="3d50a-138">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3d50a-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="3d50a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d50a-139">OUTPUTS</span></span>

### <span data-ttu-id="3d50a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d50a-140">System.Boolean</span></span>

## <span data-ttu-id="3d50a-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d50a-141">NOTES</span></span>

## <span data-ttu-id="3d50a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d50a-142">RELATED LINKS</span></span>
