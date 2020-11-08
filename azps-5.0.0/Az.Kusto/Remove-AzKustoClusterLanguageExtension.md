---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179190"
---
# <span data-ttu-id="8c561-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="8c561-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="8c561-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c561-102">SYNOPSIS</span></span>
<span data-ttu-id="8c561-103">Entfernen Sie eine Liste der Spracherweiterungen, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="8c561-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="8c561-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c561-104">SYNTAX</span></span>

### <span data-ttu-id="8c561-105">RemoveExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c561-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c561-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8c561-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c561-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c561-107">DESCRIPTION</span></span>
<span data-ttu-id="8c561-108">Entfernen Sie eine Liste der Spracherweiterungen, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="8c561-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="8c561-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c561-109">EXAMPLES</span></span>

### <span data-ttu-id="8c561-110">Beispiel 1: Entfernen einer Liste von Spracherweiterungen aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="8c561-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="8c561-111">Der obige Befehl entfernt eine Liste der Spracherweiterungen, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="8c561-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="8c561-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c561-112">PARAMETERS</span></span>

### <span data-ttu-id="8c561-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c561-113">-AsJob</span></span>
<span data-ttu-id="8c561-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="8c561-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8c561-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="8c561-115">-ClusterName</span></span>
<span data-ttu-id="8c561-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="8c561-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8c561-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c561-117">-DefaultProfile</span></span>
<span data-ttu-id="8c561-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c561-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c561-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8c561-119">-InputObject</span></span>
<span data-ttu-id="8c561-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8c561-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8c561-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8c561-121">-NoWait</span></span>
<span data-ttu-id="8c561-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="8c561-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8c561-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c561-123">-PassThru</span></span>
<span data-ttu-id="8c561-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="8c561-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8c561-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c561-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c561-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="8c561-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8c561-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8c561-127">-SubscriptionId</span></span>
<span data-ttu-id="8c561-128">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c561-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c561-129">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8c561-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8c561-130">-Wert</span><span class="sxs-lookup"><span data-stu-id="8c561-130">-Value</span></span>
<span data-ttu-id="8c561-131">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="8c561-131">The list of language extensions.</span></span>
<span data-ttu-id="8c561-132">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Wert Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8c561-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="8c561-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c561-133">-Confirm</span></span>
<span data-ttu-id="8c561-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c561-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c561-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c561-135">-WhatIf</span></span>
<span data-ttu-id="8c561-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c561-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c561-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c561-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c561-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c561-138">CommonParameters</span></span>
<span data-ttu-id="8c561-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c561-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c561-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c561-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c561-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c561-141">INPUTS</span></span>

### <span data-ttu-id="8c561-142">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8c561-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8c561-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c561-143">OUTPUTS</span></span>

### <span data-ttu-id="8c561-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c561-144">System.Boolean</span></span>

## <span data-ttu-id="8c561-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c561-145">NOTES</span></span>

<span data-ttu-id="8c561-146">Aliase</span><span class="sxs-lookup"><span data-stu-id="8c561-146">ALIASES</span></span>

<span data-ttu-id="8c561-147">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c561-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c561-148">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c561-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c561-149">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8c561-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c561-150">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="8c561-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c561-151">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8c561-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8c561-152">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="8c561-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8c561-153">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="8c561-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8c561-154">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="8c561-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8c561-155">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="8c561-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c561-156">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="8c561-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8c561-157">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="8c561-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8c561-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="8c561-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8c561-159">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c561-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8c561-160">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8c561-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="8c561-161">Value <ILanguageExtension [] >: die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="8c561-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="8c561-162">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="8c561-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="8c561-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c561-163">RELATED LINKS</span></span>

