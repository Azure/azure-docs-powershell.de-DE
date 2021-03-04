---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 6a687139f7dec156e539c09b864a88c4e8876fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929027"
---
# <span data-ttu-id="9e4c8-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="9e4c8-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="9e4c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4c8-103">Entfernen Sie eine Liste der Spracherweiterungen, die in KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="9e4c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e4c8-104">SYNTAX</span></span>

### <span data-ttu-id="9e4c8-105">RemoveExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e4c8-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e4c8-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9e4c8-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9e4c8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e4c8-107">DESCRIPTION</span></span>
<span data-ttu-id="9e4c8-108">Entfernen Sie eine Liste der Spracherweiterungen, die in KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="9e4c8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e4c8-109">EXAMPLES</span></span>

### <span data-ttu-id="9e4c8-110">Beispiel 1: Entfernen einer Liste von Spracherweiterungen aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="9e4c8-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="9e4c8-111">Der obige Befehl entfernt eine Liste der Spracherweiterungen, die in KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="9e4c8-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e4c8-112">PARAMETERS</span></span>

### <span data-ttu-id="9e4c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e4c8-113">-AsJob</span></span>
<span data-ttu-id="9e4c8-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="9e4c8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9e4c8-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9e4c8-115">-ClusterName</span></span>
<span data-ttu-id="9e4c8-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4c8-117">-DefaultProfile</span></span>
<span data-ttu-id="9e4c8-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4c8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e4c8-119">-InputObject</span></span>
<span data-ttu-id="9e4c8-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c8-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9e4c8-121">-NoWait</span></span>
<span data-ttu-id="9e4c8-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9e4c8-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9e4c8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e4c8-123">-PassThru</span></span>
<span data-ttu-id="9e4c8-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9e4c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e4c8-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c8-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e4c8-127">-SubscriptionId</span></span>
<span data-ttu-id="9e4c8-128">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e4c8-129">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c8-130">-Wert</span><span class="sxs-lookup"><span data-stu-id="9e4c8-130">-Value</span></span>
<span data-ttu-id="9e4c8-131">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-131">The list of language extensions.</span></span>
<span data-ttu-id="9e4c8-132">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu WERT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e4c8-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e4c8-133">-Confirm</span></span>
<span data-ttu-id="9e4c8-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e4c8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e4c8-135">-WhatIf</span></span>
<span data-ttu-id="9e4c8-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e4c8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e4c8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4c8-138">CommonParameters</span></span>
<span data-ttu-id="9e4c8-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4c8-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e4c8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4c8-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e4c8-141">INPUTS</span></span>

### <span data-ttu-id="9e4c8-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9e4c8-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9e4c8-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e4c8-143">OUTPUTS</span></span>

### <span data-ttu-id="9e4c8-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e4c8-144">System.Boolean</span></span>

## <span data-ttu-id="9e4c8-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e4c8-145">NOTES</span></span>

<span data-ttu-id="9e4c8-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9e4c8-146">ALIASES</span></span>

<span data-ttu-id="9e4c8-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="9e4c8-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e4c8-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e4c8-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e4c8-150">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="9e4c8-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e4c8-151">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9e4c8-152">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9e4c8-153">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9e4c8-154">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9e4c8-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="9e4c8-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e4c8-156">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9e4c8-157">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9e4c8-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9e4c8-159">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9e4c8-160">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="9e4c8-161">WERT <ILanguageExtension[]>: Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="9e4c8-162">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="9e4c8-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="9e4c8-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e4c8-163">RELATED LINKS</span></span>

