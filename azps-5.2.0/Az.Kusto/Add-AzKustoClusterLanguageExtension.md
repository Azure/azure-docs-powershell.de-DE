---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361638"
---
# <span data-ttu-id="dd9b2-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="dd9b2-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="dd9b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9b2-103">Fügen Sie eine Liste der Spracherweiterungen hinzu, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="dd9b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd9b2-104">SYNTAX</span></span>

### <span data-ttu-id="dd9b2-105">AddExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd9b2-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd9b2-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dd9b2-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd9b2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd9b2-107">DESCRIPTION</span></span>
<span data-ttu-id="dd9b2-108">Fügen Sie eine Liste der Spracherweiterungen hinzu, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="dd9b2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd9b2-109">EXAMPLES</span></span>

### <span data-ttu-id="dd9b2-110">Beispiel 1: Hinzufügen einer Liste von Spracherweiterungen</span><span class="sxs-lookup"><span data-stu-id="dd9b2-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="dd9b2-111">Der oben aufgeführte Befehl fügt eine Liste der Spracherweiterungen hinzu, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="dd9b2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd9b2-112">PARAMETERS</span></span>

### <span data-ttu-id="dd9b2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd9b2-113">-AsJob</span></span>
<span data-ttu-id="dd9b2-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd9b2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dd9b2-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dd9b2-115">-ClusterName</span></span>
<span data-ttu-id="dd9b2-116">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9b2-117">-DefaultProfile</span></span>
<span data-ttu-id="dd9b2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd9b2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd9b2-119">-InputObject</span></span>
<span data-ttu-id="dd9b2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd9b2-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dd9b2-121">-NoWait</span></span>
<span data-ttu-id="dd9b2-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="dd9b2-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd9b2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd9b2-123">-PassThru</span></span>
<span data-ttu-id="dd9b2-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dd9b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd9b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd9b2-126">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9b2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd9b2-127">-SubscriptionId</span></span>
<span data-ttu-id="dd9b2-128">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd9b2-129">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9b2-130">-Value</span><span class="sxs-lookup"><span data-stu-id="dd9b2-130">-Value</span></span>
<span data-ttu-id="dd9b2-131">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-131">The list of language extensions.</span></span>
<span data-ttu-id="dd9b2-132">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9b2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd9b2-133">-Confirm</span></span>
<span data-ttu-id="dd9b2-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd9b2-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dd9b2-135">-WhatIf</span></span>
<span data-ttu-id="dd9b2-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd9b2-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd9b2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9b2-138">CommonParameters</span></span>
<span data-ttu-id="dd9b2-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9b2-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd9b2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9b2-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd9b2-141">INPUTS</span></span>

### <span data-ttu-id="dd9b2-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="dd9b2-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="dd9b2-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd9b2-143">OUTPUTS</span></span>

### <span data-ttu-id="dd9b2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd9b2-144">System.Boolean</span></span>

## <span data-ttu-id="dd9b2-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dd9b2-145">NOTES</span></span>

<span data-ttu-id="dd9b2-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dd9b2-146">ALIASES</span></span>

<span data-ttu-id="dd9b2-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dd9b2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd9b2-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd9b2-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd9b2-150">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="dd9b2-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd9b2-151">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="dd9b2-152">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="dd9b2-153">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="dd9b2-154">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="dd9b2-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="dd9b2-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dd9b2-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd9b2-156">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="dd9b2-157">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="dd9b2-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="dd9b2-159">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd9b2-160">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="dd9b2-161">VALUE <ILanguageExtension[]>: Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="dd9b2-162">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="dd9b2-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="dd9b2-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dd9b2-163">RELATED LINKS</span></span>

