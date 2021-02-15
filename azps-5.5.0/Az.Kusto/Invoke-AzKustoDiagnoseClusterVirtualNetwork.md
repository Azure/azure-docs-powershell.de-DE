---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175196"
---
# <span data-ttu-id="f1139-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f1139-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="f1139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1139-102">SYNOPSIS</span></span>
<span data-ttu-id="f1139-103">Diagnostiziert den Netzwerkverbindungsstatus für externe Ressourcen, von denen der Dienst abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="f1139-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="f1139-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1139-104">SYNTAX</span></span>

### <span data-ttu-id="f1139-105">Diagnose (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1139-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f1139-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1139-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1139-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1139-107">DESCRIPTION</span></span>
<span data-ttu-id="f1139-108">Diagnostiziert den Netzwerkverbindungsstatus für externe Ressourcen, von denen der Dienst abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="f1139-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="f1139-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1139-109">EXAMPLES</span></span>

### <span data-ttu-id="f1139-110">Beispiel 1: Anzeigen der Diagnose der Netzwerkkonnektivität für externe Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f1139-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="f1139-111">Mit dem oben angegebenen Befehl wird der Netzwerkverbindungsstatus für externe Ressourcen diagnostizieren, von denen der Cluster "testnewkustocluster" abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="f1139-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="f1139-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1139-112">PARAMETERS</span></span>

### <span data-ttu-id="f1139-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1139-113">-AsJob</span></span>
<span data-ttu-id="f1139-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1139-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f1139-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f1139-115">-ClusterName</span></span>
<span data-ttu-id="f1139-116">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f1139-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f1139-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1139-117">-DefaultProfile</span></span>
<span data-ttu-id="f1139-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1139-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1139-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1139-119">-InputObject</span></span>
<span data-ttu-id="f1139-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f1139-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1139-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1139-121">-NoWait</span></span>
<span data-ttu-id="f1139-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f1139-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1139-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1139-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1139-124">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="f1139-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f1139-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1139-125">-SubscriptionId</span></span>
<span data-ttu-id="f1139-126">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f1139-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f1139-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="f1139-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f1139-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1139-128">-Confirm</span></span>
<span data-ttu-id="f1139-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1139-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1139-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1139-130">-WhatIf</span></span>
<span data-ttu-id="f1139-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1139-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1139-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1139-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1139-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1139-133">CommonParameters</span></span>
<span data-ttu-id="f1139-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1139-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1139-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1139-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1139-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1139-136">INPUTS</span></span>

### <span data-ttu-id="f1139-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f1139-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f1139-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1139-138">OUTPUTS</span></span>

### <span data-ttu-id="f1139-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f1139-139">System.String</span></span>

## <span data-ttu-id="f1139-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1139-140">NOTES</span></span>

<span data-ttu-id="f1139-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f1139-141">ALIASES</span></span>

<span data-ttu-id="f1139-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f1139-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1139-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1139-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1139-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1139-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1139-145">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f1139-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1139-146">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1139-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f1139-147">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f1139-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f1139-148">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="f1139-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f1139-149">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="f1139-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f1139-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f1139-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1139-151">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="f1139-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f1139-152">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f1139-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f1139-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="f1139-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f1139-154">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f1139-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f1139-155">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="f1139-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f1139-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1139-156">RELATED LINKS</span></span>

