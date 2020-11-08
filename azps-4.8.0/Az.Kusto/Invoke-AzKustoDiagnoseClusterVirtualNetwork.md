---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173758"
---
# <span data-ttu-id="41f6a-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="41f6a-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="41f6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="41f6a-103">Diagnostiziert den Netzwerkverbindungsstatus für externe Ressourcen, von denen der Dienst abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="41f6a-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="41f6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41f6a-104">SYNTAX</span></span>

### <span data-ttu-id="41f6a-105">Diagnose (Standard)</span><span class="sxs-lookup"><span data-stu-id="41f6a-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="41f6a-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41f6a-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41f6a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41f6a-107">DESCRIPTION</span></span>
<span data-ttu-id="41f6a-108">Diagnostiziert den Netzwerkverbindungsstatus für externe Ressourcen, von denen der Dienst abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="41f6a-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="41f6a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41f6a-109">EXAMPLES</span></span>

### <span data-ttu-id="41f6a-110">Beispiel 1: Anzeigen der Netzwerk Verbindungsdiagnose für externe Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41f6a-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="41f6a-111">Der obige Befehl diagnostiziert den Netzwerkverbindungsstatus für externe Ressourcen, von denen der Cluster "testnewkustocluster" abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="41f6a-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="41f6a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="41f6a-112">PARAMETERS</span></span>

### <span data-ttu-id="41f6a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41f6a-113">-AsJob</span></span>
<span data-ttu-id="41f6a-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="41f6a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="41f6a-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="41f6a-115">-ClusterName</span></span>
<span data-ttu-id="41f6a-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="41f6a-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f6a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f6a-117">-DefaultProfile</span></span>
<span data-ttu-id="41f6a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41f6a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41f6a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41f6a-119">-InputObject</span></span>
<span data-ttu-id="41f6a-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="41f6a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41f6a-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="41f6a-121">-NoWait</span></span>
<span data-ttu-id="41f6a-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="41f6a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="41f6a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f6a-123">-ResourceGroupName</span></span>
<span data-ttu-id="41f6a-124">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="41f6a-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f6a-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="41f6a-125">-SubscriptionId</span></span>
<span data-ttu-id="41f6a-126">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="41f6a-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41f6a-127">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="41f6a-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f6a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41f6a-128">-Confirm</span></span>
<span data-ttu-id="41f6a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41f6a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f6a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f6a-130">-WhatIf</span></span>
<span data-ttu-id="41f6a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41f6a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f6a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41f6a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f6a-133">CommonParameters</span></span>
<span data-ttu-id="41f6a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f6a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41f6a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f6a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41f6a-136">INPUTS</span></span>

### <span data-ttu-id="41f6a-137">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="41f6a-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="41f6a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41f6a-138">OUTPUTS</span></span>

### <span data-ttu-id="41f6a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="41f6a-139">System.String</span></span>

## <span data-ttu-id="41f6a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="41f6a-140">NOTES</span></span>

<span data-ttu-id="41f6a-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="41f6a-141">ALIASES</span></span>

<span data-ttu-id="41f6a-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41f6a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41f6a-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41f6a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41f6a-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="41f6a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41f6a-145">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="41f6a-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41f6a-146">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="41f6a-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="41f6a-147">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="41f6a-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="41f6a-148">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="41f6a-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="41f6a-149">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="41f6a-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="41f6a-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="41f6a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41f6a-151">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="41f6a-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="41f6a-152">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="41f6a-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="41f6a-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="41f6a-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="41f6a-154">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="41f6a-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="41f6a-155">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="41f6a-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="41f6a-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41f6a-156">RELATED LINKS</span></span>

