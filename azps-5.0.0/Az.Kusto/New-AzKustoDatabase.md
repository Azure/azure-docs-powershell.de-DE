---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179198"
---
# <span data-ttu-id="1880a-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="1880a-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="1880a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1880a-102">SYNOPSIS</span></span>
<span data-ttu-id="1880a-103">Erstellt oder aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1880a-103">Creates or updates a database.</span></span>

## <span data-ttu-id="1880a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1880a-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1880a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1880a-105">DESCRIPTION</span></span>
<span data-ttu-id="1880a-106">Erstellt oder aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1880a-106">Creates or updates a database.</span></span>

## <span data-ttu-id="1880a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1880a-107">EXAMPLES</span></span>

### <span data-ttu-id="1880a-108">Beispiel 1: Erstellen einer neuen Kusto-Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="1880a-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="1880a-109">Der obige Befehl erstellt eine neue Kusto-Datenbank mit dem Namen "mykustodatabase" im vorhandenen Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="1880a-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="1880a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1880a-110">PARAMETERS</span></span>

### <span data-ttu-id="1880a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1880a-111">-AsJob</span></span>
<span data-ttu-id="1880a-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1880a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1880a-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1880a-113">-ClusterName</span></span>
<span data-ttu-id="1880a-114">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="1880a-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1880a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1880a-115">-DefaultProfile</span></span>
<span data-ttu-id="1880a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1880a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1880a-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="1880a-117">-HotCachePeriod</span></span>
<span data-ttu-id="1880a-118">Der Zeitpunkt, zu dem die Daten im Cache für schnelle Abfragen in TimeSpan aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1880a-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1880a-119">-Art</span><span class="sxs-lookup"><span data-stu-id="1880a-119">-Kind</span></span>
<span data-ttu-id="1880a-120">Art der Datenbank</span><span class="sxs-lookup"><span data-stu-id="1880a-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1880a-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="1880a-121">-Location</span></span>
<span data-ttu-id="1880a-122">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="1880a-122">Resource location.</span></span>

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

### <span data-ttu-id="1880a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1880a-123">-Name</span></span>
<span data-ttu-id="1880a-124">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="1880a-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1880a-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1880a-125">-NoWait</span></span>
<span data-ttu-id="1880a-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1880a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1880a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1880a-127">-ResourceGroupName</span></span>
<span data-ttu-id="1880a-128">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="1880a-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1880a-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="1880a-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="1880a-130">Der Zeitpunkt, zu dem die Daten aufbewahrt werden sollen, bevor Sie nicht mehr auf Abfragen in TimeSpan zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="1880a-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1880a-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="1880a-131">-SubscriptionId</span></span>
<span data-ttu-id="1880a-132">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1880a-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1880a-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="1880a-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1880a-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1880a-134">-Confirm</span></span>
<span data-ttu-id="1880a-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1880a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1880a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1880a-136">-WhatIf</span></span>
<span data-ttu-id="1880a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1880a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1880a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1880a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1880a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1880a-139">CommonParameters</span></span>
<span data-ttu-id="1880a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1880a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1880a-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1880a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1880a-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1880a-142">INPUTS</span></span>

## <span data-ttu-id="1880a-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1880a-143">OUTPUTS</span></span>

### <span data-ttu-id="1880a-144">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="1880a-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="1880a-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="1880a-145">NOTES</span></span>

<span data-ttu-id="1880a-146">Aliase</span><span class="sxs-lookup"><span data-stu-id="1880a-146">ALIASES</span></span>

## <span data-ttu-id="1880a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1880a-147">RELATED LINKS</span></span>

