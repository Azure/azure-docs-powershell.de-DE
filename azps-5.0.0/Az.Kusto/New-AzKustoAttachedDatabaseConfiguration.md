---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179204"
---
# <span data-ttu-id="fe62b-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe62b-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="fe62b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe62b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe62b-103">Erstellt oder aktualisiert eine angefügte Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fe62b-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="fe62b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe62b-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe62b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe62b-105">DESCRIPTION</span></span>
<span data-ttu-id="fe62b-106">Erstellt oder aktualisiert eine angefügte Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fe62b-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="fe62b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe62b-107">EXAMPLES</span></span>

### <span data-ttu-id="fe62b-108">Beispiel 1: Erstellen eines neuen AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe62b-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="fe62b-109">Der obige Befehl erstellt eine ReadOnly-Datenbank "mykustodatabase" im Cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="fe62b-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="fe62b-110">Sie folgt der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="fe62b-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="fe62b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe62b-111">PARAMETERS</span></span>

### <span data-ttu-id="fe62b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe62b-112">-AsJob</span></span>
<span data-ttu-id="fe62b-113">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="fe62b-113">Run the command as a job</span></span>

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

### <span data-ttu-id="fe62b-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="fe62b-114">-ClusterName</span></span>
<span data-ttu-id="fe62b-115">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="fe62b-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fe62b-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="fe62b-116">-ClusterResourceId</span></span>
<span data-ttu-id="fe62b-117">Die Ressourcen-ID des Clusters, in dem sich die Datenbanken befinden, die Sie anfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="fe62b-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="fe62b-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe62b-118">-DatabaseName</span></span>
<span data-ttu-id="fe62b-119">Den Namen der Datenbank, die Sie anfügen möchten, verwenden Sie \*, wenn Sie alle aktuellen und zukünftigen Datenbanken befolgen möchten.</span><span class="sxs-lookup"><span data-stu-id="fe62b-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="fe62b-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="fe62b-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="fe62b-121">Die standardmäßige Änderung des Prinzipaltyps</span><span class="sxs-lookup"><span data-stu-id="fe62b-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe62b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe62b-122">-DefaultProfile</span></span>
<span data-ttu-id="fe62b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe62b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe62b-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="fe62b-124">-Location</span></span>
<span data-ttu-id="fe62b-125">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="fe62b-125">Resource location.</span></span>

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

### <span data-ttu-id="fe62b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fe62b-126">-Name</span></span>
<span data-ttu-id="fe62b-127">Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fe62b-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe62b-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fe62b-128">-NoWait</span></span>
<span data-ttu-id="fe62b-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="fe62b-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fe62b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe62b-130">-ResourceGroupName</span></span>
<span data-ttu-id="fe62b-131">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="fe62b-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fe62b-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fe62b-132">-SubscriptionId</span></span>
<span data-ttu-id="fe62b-133">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fe62b-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fe62b-134">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="fe62b-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fe62b-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe62b-135">-Confirm</span></span>
<span data-ttu-id="fe62b-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe62b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe62b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe62b-137">-WhatIf</span></span>
<span data-ttu-id="fe62b-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe62b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe62b-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe62b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe62b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe62b-140">CommonParameters</span></span>
<span data-ttu-id="fe62b-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe62b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe62b-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe62b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe62b-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe62b-143">INPUTS</span></span>

## <span data-ttu-id="fe62b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe62b-144">OUTPUTS</span></span>

### <span data-ttu-id="fe62b-145">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe62b-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="fe62b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe62b-146">NOTES</span></span>

<span data-ttu-id="fe62b-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="fe62b-147">ALIASES</span></span>

## <span data-ttu-id="fe62b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe62b-148">RELATED LINKS</span></span>

