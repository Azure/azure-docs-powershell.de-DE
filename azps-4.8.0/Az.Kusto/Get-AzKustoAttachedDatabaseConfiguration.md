---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166399"
---
# <span data-ttu-id="96fc8-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="96fc8-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="96fc8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="96fc8-103">Gibt eine angefügte Datenbankkonfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="96fc8-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="96fc8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96fc8-104">SYNTAX</span></span>

### <span data-ttu-id="96fc8-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="96fc8-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96fc8-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="96fc8-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96fc8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96fc8-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="96fc8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96fc8-108">DESCRIPTION</span></span>
<span data-ttu-id="96fc8-109">Gibt eine angefügte Datenbankkonfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="96fc8-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="96fc8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96fc8-110">EXAMPLES</span></span>

### <span data-ttu-id="96fc8-111">Beispiel 1: Auflisten aller AttachedDatabaseConfigurations in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="96fc8-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="96fc8-112">Der obige Befehl listet alle AttachedDatabaseConfigurations im Cluster "testnewkustoclusterf" auf.</span><span class="sxs-lookup"><span data-stu-id="96fc8-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="96fc8-113">Beispiel 2: Abrufen einer bestimmten AttachedDatabaseConfiguration in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="96fc8-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="96fc8-114">Der obige Befehl gibt den AttachedDatabaseConfigurations mit dem Namen "myfollowerconfiguration" im Cluster "testnewkustoclusterf" zurück.</span><span class="sxs-lookup"><span data-stu-id="96fc8-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="96fc8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="96fc8-115">PARAMETERS</span></span>

### <span data-ttu-id="96fc8-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="96fc8-116">-ClusterName</span></span>
<span data-ttu-id="96fc8-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="96fc8-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="96fc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96fc8-118">-DefaultProfile</span></span>
<span data-ttu-id="96fc8-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96fc8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96fc8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96fc8-120">-InputObject</span></span>
<span data-ttu-id="96fc8-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="96fc8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96fc8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="96fc8-122">-Name</span></span>
<span data-ttu-id="96fc8-123">Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="96fc8-123">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="96fc8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96fc8-124">-ResourceGroupName</span></span>
<span data-ttu-id="96fc8-125">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="96fc8-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="96fc8-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="96fc8-126">-SubscriptionId</span></span>
<span data-ttu-id="96fc8-127">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="96fc8-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="96fc8-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="96fc8-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96fc8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96fc8-129">CommonParameters</span></span>
<span data-ttu-id="96fc8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96fc8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96fc8-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96fc8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96fc8-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96fc8-132">INPUTS</span></span>

### <span data-ttu-id="96fc8-133">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="96fc8-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="96fc8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96fc8-134">OUTPUTS</span></span>

### <span data-ttu-id="96fc8-135">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="96fc8-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="96fc8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="96fc8-136">NOTES</span></span>

<span data-ttu-id="96fc8-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="96fc8-137">ALIASES</span></span>

<span data-ttu-id="96fc8-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96fc8-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96fc8-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96fc8-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96fc8-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="96fc8-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96fc8-141">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="96fc8-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96fc8-142">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="96fc8-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="96fc8-143">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="96fc8-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="96fc8-144">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="96fc8-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="96fc8-145">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="96fc8-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="96fc8-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="96fc8-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96fc8-147">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="96fc8-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="96fc8-148">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="96fc8-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="96fc8-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="96fc8-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="96fc8-150">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="96fc8-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="96fc8-151">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="96fc8-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="96fc8-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96fc8-152">RELATED LINKS</span></span>

