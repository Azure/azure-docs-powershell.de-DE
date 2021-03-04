---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 0e1cfc142c4c98614519c26639144cc701d2118c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924912"
---
# <span data-ttu-id="83bf3-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="83bf3-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="83bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="83bf3-103">Fügen Sie eine Liste der Spracherweiterungen hinzu, die in KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="83bf3-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="83bf3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83bf3-104">SYNTAX</span></span>

### <span data-ttu-id="83bf3-105">AddExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="83bf3-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83bf3-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83bf3-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83bf3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83bf3-107">DESCRIPTION</span></span>
<span data-ttu-id="83bf3-108">Fügen Sie eine Liste der Spracherweiterungen hinzu, die in KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="83bf3-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="83bf3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83bf3-109">EXAMPLES</span></span>

### <span data-ttu-id="83bf3-110">Beispiel 1: Hinzufügen einer Liste von Spracherweiterungen</span><span class="sxs-lookup"><span data-stu-id="83bf3-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="83bf3-111">Der obige Befehl fügt eine Liste der Spracherweiterungen hinzu, die in KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="83bf3-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="83bf3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="83bf3-112">PARAMETERS</span></span>

### <span data-ttu-id="83bf3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83bf3-113">-AsJob</span></span>
<span data-ttu-id="83bf3-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="83bf3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="83bf3-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="83bf3-115">-ClusterName</span></span>
<span data-ttu-id="83bf3-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="83bf3-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="83bf3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83bf3-117">-DefaultProfile</span></span>
<span data-ttu-id="83bf3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83bf3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83bf3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83bf3-119">-InputObject</span></span>
<span data-ttu-id="83bf3-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="83bf3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83bf3-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="83bf3-121">-NoWait</span></span>
<span data-ttu-id="83bf3-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="83bf3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83bf3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83bf3-123">-PassThru</span></span>
<span data-ttu-id="83bf3-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83bf3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="83bf3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83bf3-125">-ResourceGroupName</span></span>
<span data-ttu-id="83bf3-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="83bf3-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="83bf3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83bf3-127">-SubscriptionId</span></span>
<span data-ttu-id="83bf3-128">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="83bf3-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="83bf3-129">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="83bf3-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="83bf3-130">-Wert</span><span class="sxs-lookup"><span data-stu-id="83bf3-130">-Value</span></span>
<span data-ttu-id="83bf3-131">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="83bf3-131">The list of language extensions.</span></span>
<span data-ttu-id="83bf3-132">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu WERT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="83bf3-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83bf3-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83bf3-133">-Confirm</span></span>
<span data-ttu-id="83bf3-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83bf3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83bf3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83bf3-135">-WhatIf</span></span>
<span data-ttu-id="83bf3-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83bf3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83bf3-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83bf3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83bf3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83bf3-138">CommonParameters</span></span>
<span data-ttu-id="83bf3-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83bf3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83bf3-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83bf3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83bf3-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83bf3-141">INPUTS</span></span>

### <span data-ttu-id="83bf3-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="83bf3-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="83bf3-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83bf3-143">OUTPUTS</span></span>

### <span data-ttu-id="83bf3-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83bf3-144">System.Boolean</span></span>

## <span data-ttu-id="83bf3-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="83bf3-145">NOTES</span></span>

<span data-ttu-id="83bf3-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="83bf3-146">ALIASES</span></span>

<span data-ttu-id="83bf3-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="83bf3-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83bf3-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="83bf3-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83bf3-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83bf3-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83bf3-150">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="83bf3-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83bf3-151">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="83bf3-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="83bf3-152">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="83bf3-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="83bf3-153">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="83bf3-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="83bf3-154">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="83bf3-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="83bf3-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="83bf3-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83bf3-156">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="83bf3-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="83bf3-157">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="83bf3-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="83bf3-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="83bf3-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="83bf3-159">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="83bf3-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="83bf3-160">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="83bf3-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="83bf3-161">WERT <ILanguageExtension[]>: Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="83bf3-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="83bf3-162">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="83bf3-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="83bf3-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="83bf3-163">RELATED LINKS</span></span>

