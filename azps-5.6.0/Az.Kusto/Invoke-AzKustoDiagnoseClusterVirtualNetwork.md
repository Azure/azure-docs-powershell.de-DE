---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: d2530404774c3cb735dedb6eb233979fe602fe4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948640"
---
# <span data-ttu-id="bce64-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bce64-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="bce64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bce64-102">SYNOPSIS</span></span>
<span data-ttu-id="bce64-103">Diagnose des Netzwerkkonnektivitätsstatus für externe Ressourcen, von denen der Dienst abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="bce64-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="bce64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bce64-104">SYNTAX</span></span>

### <span data-ttu-id="bce64-105">Diagnose (Standard)</span><span class="sxs-lookup"><span data-stu-id="bce64-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bce64-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bce64-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bce64-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bce64-107">DESCRIPTION</span></span>
<span data-ttu-id="bce64-108">Diagnose des Netzwerkkonnektivitätsstatus für externe Ressourcen, von denen der Dienst abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="bce64-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="bce64-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bce64-109">EXAMPLES</span></span>

### <span data-ttu-id="bce64-110">Beispiel 1: Anzeigen der Diagnose der Netzwerkkonnektivität für externe Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bce64-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="bce64-111">Der obige Befehl diagnoset den Netzwerkkonnektivitätsstatus für externe Ressourcen, von denen der Cluster "testnewkustocluster" abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="bce64-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="bce64-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bce64-112">PARAMETERS</span></span>

### <span data-ttu-id="bce64-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bce64-113">-AsJob</span></span>
<span data-ttu-id="bce64-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="bce64-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bce64-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bce64-115">-ClusterName</span></span>
<span data-ttu-id="bce64-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="bce64-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="bce64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce64-117">-DefaultProfile</span></span>
<span data-ttu-id="bce64-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bce64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce64-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bce64-119">-InputObject</span></span>
<span data-ttu-id="bce64-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="bce64-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bce64-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bce64-121">-NoWait</span></span>
<span data-ttu-id="bce64-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="bce64-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bce64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce64-123">-ResourceGroupName</span></span>
<span data-ttu-id="bce64-124">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="bce64-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="bce64-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bce64-125">-SubscriptionId</span></span>
<span data-ttu-id="bce64-126">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="bce64-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bce64-127">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="bce64-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bce64-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bce64-128">-Confirm</span></span>
<span data-ttu-id="bce64-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bce64-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce64-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce64-130">-WhatIf</span></span>
<span data-ttu-id="bce64-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bce64-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce64-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bce64-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce64-133">CommonParameters</span></span>
<span data-ttu-id="bce64-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce64-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bce64-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce64-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bce64-136">INPUTS</span></span>

### <span data-ttu-id="bce64-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="bce64-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="bce64-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bce64-138">OUTPUTS</span></span>

### <span data-ttu-id="bce64-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bce64-139">System.String</span></span>

## <span data-ttu-id="bce64-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bce64-140">NOTES</span></span>

<span data-ttu-id="bce64-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bce64-141">ALIASES</span></span>

<span data-ttu-id="bce64-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="bce64-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bce64-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="bce64-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bce64-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bce64-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bce64-145">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="bce64-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bce64-146">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="bce64-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="bce64-147">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="bce64-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="bce64-148">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="bce64-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="bce64-149">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="bce64-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="bce64-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="bce64-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bce64-151">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="bce64-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="bce64-152">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="bce64-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="bce64-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="bce64-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="bce64-154">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="bce64-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bce64-155">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="bce64-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bce64-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bce64-156">RELATED LINKS</span></span>

