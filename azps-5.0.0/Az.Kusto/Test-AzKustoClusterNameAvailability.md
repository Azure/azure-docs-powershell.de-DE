---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180386"
---
# <span data-ttu-id="441ee-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="441ee-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="441ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="441ee-102">SYNOPSIS</span></span>
<span data-ttu-id="441ee-103">Überprüft, ob der Clustername gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="441ee-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="441ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="441ee-104">SYNTAX</span></span>

### <span data-ttu-id="441ee-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="441ee-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="441ee-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="441ee-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="441ee-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="441ee-107">DESCRIPTION</span></span>
<span data-ttu-id="441ee-108">Überprüft, ob der Clustername gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="441ee-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="441ee-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="441ee-109">EXAMPLES</span></span>

### <span data-ttu-id="441ee-110">Beispiel 1: Überprüfen der Verfügbarkeit eines Kusto-Clusternamens, der verwendet wird</span><span class="sxs-lookup"><span data-stu-id="441ee-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="441ee-111">Der obige Befehl gibt zurück, ob im Bereich "Ost-USA" ein Kusto-Cluster mit dem Namen "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="441ee-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="441ee-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Kusto-Clusternamens, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="441ee-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="441ee-113">Der obige Befehl gibt zurück, ob im Bereich "Ost-USA" ein Kusto-Cluster mit dem Namen "availablekustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="441ee-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="441ee-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="441ee-114">PARAMETERS</span></span>

### <span data-ttu-id="441ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441ee-115">-DefaultProfile</span></span>
<span data-ttu-id="441ee-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="441ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="441ee-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="441ee-117">-InputObject</span></span>
<span data-ttu-id="441ee-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="441ee-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="441ee-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="441ee-119">-Location</span></span>
<span data-ttu-id="441ee-120">Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="441ee-120">Azure location.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441ee-121">-Name</span><span class="sxs-lookup"><span data-stu-id="441ee-121">-Name</span></span>
<span data-ttu-id="441ee-122">Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="441ee-122">Cluster name.</span></span>

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

### <span data-ttu-id="441ee-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="441ee-123">-SubscriptionId</span></span>
<span data-ttu-id="441ee-124">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="441ee-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="441ee-125">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="441ee-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441ee-126">-Typ</span><span class="sxs-lookup"><span data-stu-id="441ee-126">-Type</span></span>
<span data-ttu-id="441ee-127">Der Typ der Ressource, Microsoft. Kusto/Clusters.</span><span class="sxs-lookup"><span data-stu-id="441ee-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441ee-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="441ee-128">-Confirm</span></span>
<span data-ttu-id="441ee-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="441ee-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="441ee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="441ee-130">-WhatIf</span></span>
<span data-ttu-id="441ee-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="441ee-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="441ee-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="441ee-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="441ee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441ee-133">CommonParameters</span></span>
<span data-ttu-id="441ee-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="441ee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441ee-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="441ee-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441ee-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="441ee-136">INPUTS</span></span>

### <span data-ttu-id="441ee-137">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="441ee-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="441ee-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="441ee-138">OUTPUTS</span></span>

### <span data-ttu-id="441ee-139">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="441ee-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="441ee-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="441ee-140">NOTES</span></span>

<span data-ttu-id="441ee-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="441ee-141">ALIASES</span></span>

<span data-ttu-id="441ee-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="441ee-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="441ee-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="441ee-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="441ee-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="441ee-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="441ee-145">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="441ee-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="441ee-146">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="441ee-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="441ee-147">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="441ee-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="441ee-148">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="441ee-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="441ee-149">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="441ee-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="441ee-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="441ee-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="441ee-151">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="441ee-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="441ee-152">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="441ee-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="441ee-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="441ee-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="441ee-154">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="441ee-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="441ee-155">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="441ee-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="441ee-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="441ee-156">RELATED LINKS</span></span>

