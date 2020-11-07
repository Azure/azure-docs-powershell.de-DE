---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: ce2fbe2f598ca6d08033c397a988f140379fda96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650809"
---
# <span data-ttu-id="4048f-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4048f-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="4048f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4048f-102">SYNOPSIS</span></span>
<span data-ttu-id="4048f-103">Fortsetzen eines angehalten Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="4048f-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="4048f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4048f-104">SYNTAX</span></span>

### <span data-ttu-id="4048f-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="4048f-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4048f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4048f-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4048f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4048f-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4048f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4048f-108">DESCRIPTION</span></span>
<span data-ttu-id="4048f-109">Fortsetzen eines angehalten Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="4048f-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="4048f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4048f-110">EXAMPLES</span></span>

### <span data-ttu-id="4048f-111">Beispiel 1 – fortsetzen eines angehalten Kusto-Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="4048f-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="4048f-112">Der obige Befehl setzt den angehalten Kusto-Cluster mit dem Namen "mykustocluster" fort, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="4048f-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="4048f-113">Beispiel 2 – fortsetzen eines angehalten Kusto-Clusters durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="4048f-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="4048f-114">Der obige Befehl ruft den Kusto-Cluster mit dem Namen "mykustocluster" ab, der in der Ressourcengruppe "testrg" mit dem Cmdlet gefunden wird `Get-AzKustoCluster` , und leitet dann das Ergebnis an, um `Resume-AzKustoCluster` es fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4048f-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="4048f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4048f-115">PARAMETERS</span></span>

### <span data-ttu-id="4048f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4048f-116">-DefaultProfile</span></span>
<span data-ttu-id="4048f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4048f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4048f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4048f-118">-InputObject</span></span>
<span data-ttu-id="4048f-119">Kusto-Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="4048f-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="4048f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4048f-120">-Name</span></span>
<span data-ttu-id="4048f-121">Der Name des Clusters, der fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4048f-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="4048f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4048f-122">-PassThru</span></span>
<span data-ttu-id="4048f-123">Gibt zurück, ob der angegebene Cluster erfolgreich fortgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="4048f-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="4048f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4048f-124">-ResourceGroupName</span></span>
<span data-ttu-id="4048f-125">Der Name der Ressourcengruppe, unter der der Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4048f-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048f-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4048f-126">-ResourceId</span></span>
<span data-ttu-id="4048f-127">Kusto-Cluster-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="4048f-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="4048f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4048f-128">-Confirm</span></span>
<span data-ttu-id="4048f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4048f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4048f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4048f-130">-WhatIf</span></span>
<span data-ttu-id="4048f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4048f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4048f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4048f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4048f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4048f-133">CommonParameters</span></span>
<span data-ttu-id="4048f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4048f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4048f-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4048f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4048f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4048f-136">INPUTS</span></span>

### <span data-ttu-id="4048f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4048f-137">System.String</span></span>

### <span data-ttu-id="4048f-138">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4048f-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4048f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4048f-139">OUTPUTS</span></span>

### <span data-ttu-id="4048f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4048f-140">System.Boolean</span></span>

## <span data-ttu-id="4048f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="4048f-141">NOTES</span></span>

## <span data-ttu-id="4048f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4048f-142">RELATED LINKS</span></span>
