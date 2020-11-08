---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179231"
---
# <span data-ttu-id="6c9da-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c9da-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="6c9da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c9da-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9da-103">Gibt eine angefügte Datenbankkonfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="6c9da-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="6c9da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c9da-104">SYNTAX</span></span>

### <span data-ttu-id="6c9da-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c9da-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6c9da-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6c9da-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6c9da-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6c9da-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c9da-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c9da-108">DESCRIPTION</span></span>
<span data-ttu-id="6c9da-109">Gibt eine angefügte Datenbankkonfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="6c9da-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="6c9da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c9da-110">EXAMPLES</span></span>

### <span data-ttu-id="6c9da-111">Beispiel 1: Auflisten aller AttachedDatabaseConfigurations in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="6c9da-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="6c9da-112">Der obige Befehl listet alle AttachedDatabaseConfigurations im Cluster "testnewkustoclusterf" auf.</span><span class="sxs-lookup"><span data-stu-id="6c9da-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="6c9da-113">Beispiel 2: Abrufen einer bestimmten AttachedDatabaseConfiguration in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="6c9da-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="6c9da-114">Der obige Befehl gibt den AttachedDatabaseConfigurations mit dem Namen "myfollowerconfiguration" im Cluster "testnewkustoclusterf" zurück.</span><span class="sxs-lookup"><span data-stu-id="6c9da-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="6c9da-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c9da-115">PARAMETERS</span></span>

### <span data-ttu-id="6c9da-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6c9da-116">-ClusterName</span></span>
<span data-ttu-id="6c9da-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="6c9da-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9da-118">-DefaultProfile</span></span>
<span data-ttu-id="6c9da-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c9da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c9da-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c9da-120">-InputObject</span></span>
<span data-ttu-id="6c9da-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6c9da-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9da-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6c9da-122">-Name</span></span>
<span data-ttu-id="6c9da-123">Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c9da-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c9da-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c9da-125">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="6c9da-125">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9da-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6c9da-126">-SubscriptionId</span></span>
<span data-ttu-id="6c9da-127">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6c9da-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6c9da-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="6c9da-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9da-129">CommonParameters</span></span>
<span data-ttu-id="6c9da-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9da-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c9da-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9da-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c9da-132">INPUTS</span></span>

### <span data-ttu-id="6c9da-133">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="6c9da-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="6c9da-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c9da-134">OUTPUTS</span></span>

### <span data-ttu-id="6c9da-135">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c9da-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="6c9da-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c9da-136">NOTES</span></span>

<span data-ttu-id="6c9da-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="6c9da-137">ALIASES</span></span>

<span data-ttu-id="6c9da-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c9da-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c9da-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c9da-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c9da-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="6c9da-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c9da-141">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="6c9da-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c9da-142">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c9da-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="6c9da-143">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="6c9da-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="6c9da-144">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="6c9da-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="6c9da-145">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="6c9da-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="6c9da-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="6c9da-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c9da-147">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="6c9da-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="6c9da-148">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="6c9da-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="6c9da-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="6c9da-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="6c9da-150">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6c9da-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6c9da-151">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="6c9da-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6c9da-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c9da-152">RELATED LINKS</span></span>

