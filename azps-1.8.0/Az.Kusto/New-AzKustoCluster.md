---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9157c5dfff46893cfee88d02d8f1564801f889fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819464"
---
# <span data-ttu-id="200bd-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="200bd-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="200bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="200bd-102">SYNOPSIS</span></span>
<span data-ttu-id="200bd-103">Erstellt einen neuen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="200bd-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="200bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="200bd-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="200bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="200bd-105">DESCRIPTION</span></span>
<span data-ttu-id="200bd-106">Erstellt einen neuen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="200bd-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="200bd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="200bd-107">EXAMPLES</span></span>

### <span data-ttu-id="200bd-108">Beispiel 1: Erstellen eines neuen Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="200bd-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="200bd-109">Der obige Befehl erstellt einen neuen Kusto-Cluster mit dem Namen "mykustocluster" in der Ressourcengruppe "testrg".</span><span class="sxs-lookup"><span data-stu-id="200bd-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="200bd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="200bd-110">PARAMETERS</span></span>

### <span data-ttu-id="200bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="200bd-111">-DefaultProfile</span></span>
<span data-ttu-id="200bd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="200bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="200bd-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="200bd-113">-Location</span></span>
<span data-ttu-id="200bd-114">Azure-Bereich, in dem der Cluster erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="200bd-114">Azure region where the cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="200bd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="200bd-115">-Name</span></span>
<span data-ttu-id="200bd-116">Der Name des zu erstellende Clusters.</span><span class="sxs-lookup"><span data-stu-id="200bd-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="200bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="200bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="200bd-118">Name der Ressourcengruppe, unter der Sie den Cluster erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="200bd-118">Name of resource group under which you want to create the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="200bd-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="200bd-119">-Sku</span></span>
<span data-ttu-id="200bd-120">Name der SKU, die zum Erstellen des Clusters verwendet wird</span><span class="sxs-lookup"><span data-stu-id="200bd-120">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="200bd-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="200bd-121">-Tag</span></span>
<span data-ttu-id="200bd-122">Eine Zeichenfolge, Zeichenfolgenwörterbuch für Transponder, die diesem Cluster zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="200bd-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="200bd-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="200bd-123">-Tier</span></span>
<span data-ttu-id="200bd-124">Name der zum Erstellen des Clusters verwendeten Ebene</span><span class="sxs-lookup"><span data-stu-id="200bd-124">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="200bd-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="200bd-125">-Confirm</span></span>
<span data-ttu-id="200bd-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="200bd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="200bd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="200bd-127">-WhatIf</span></span>
<span data-ttu-id="200bd-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="200bd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="200bd-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="200bd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="200bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="200bd-130">CommonParameters</span></span>
<span data-ttu-id="200bd-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="200bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="200bd-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="200bd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="200bd-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="200bd-133">INPUTS</span></span>

### <span data-ttu-id="200bd-134">Keine</span><span class="sxs-lookup"><span data-stu-id="200bd-134">None</span></span>

## <span data-ttu-id="200bd-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="200bd-135">OUTPUTS</span></span>

### <span data-ttu-id="200bd-136">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="200bd-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="200bd-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="200bd-137">NOTES</span></span>

## <span data-ttu-id="200bd-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="200bd-138">RELATED LINKS</span></span>
