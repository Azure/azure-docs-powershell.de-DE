---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299304"
---
# <span data-ttu-id="0aab0-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="0aab0-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="0aab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aab0-102">SYNOPSIS</span></span>
<span data-ttu-id="0aab0-103">Entfernen Sie Berechtigungen für Datenbankprinzipale.</span><span class="sxs-lookup"><span data-stu-id="0aab0-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="0aab0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0aab0-104">SYNTAX</span></span>

### <span data-ttu-id="0aab0-105">RemoveExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="0aab0-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0aab0-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0aab0-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0aab0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aab0-107">DESCRIPTION</span></span>
<span data-ttu-id="0aab0-108">Entfernen Sie Berechtigungen für Datenbankprinzipale.</span><span class="sxs-lookup"><span data-stu-id="0aab0-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="0aab0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0aab0-109">EXAMPLES</span></span>

### <span data-ttu-id="0aab0-110">Beispiel 1: Entfernen von Berechtigungen für Datenbankprinzipale</span><span class="sxs-lookup"><span data-stu-id="0aab0-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="0aab0-111">Der oben aufgeführte Befehl entfernt Datenbankprinzipalberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="0aab0-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="0aab0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0aab0-112">PARAMETERS</span></span>

### <span data-ttu-id="0aab0-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0aab0-113">-ClusterName</span></span>
<span data-ttu-id="0aab0-114">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="0aab0-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0aab0-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0aab0-115">-DatabaseName</span></span>
<span data-ttu-id="0aab0-116">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="0aab0-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="0aab0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aab0-117">-DefaultProfile</span></span>
<span data-ttu-id="0aab0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aab0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aab0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aab0-119">-InputObject</span></span>
<span data-ttu-id="0aab0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0aab0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0aab0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aab0-121">-ResourceGroupName</span></span>
<span data-ttu-id="0aab0-122">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="0aab0-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0aab0-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0aab0-123">-SubscriptionId</span></span>
<span data-ttu-id="0aab0-124">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0aab0-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0aab0-125">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="0aab0-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0aab0-126">-Value</span><span class="sxs-lookup"><span data-stu-id="0aab0-126">-Value</span></span>
<span data-ttu-id="0aab0-127">Die Liste der Kusto-Datenbankprinzipale.</span><span class="sxs-lookup"><span data-stu-id="0aab0-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="0aab0-128">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0aab0-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aab0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0aab0-129">-Confirm</span></span>
<span data-ttu-id="0aab0-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0aab0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aab0-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0aab0-131">-WhatIf</span></span>
<span data-ttu-id="0aab0-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0aab0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aab0-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0aab0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aab0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aab0-134">CommonParameters</span></span>
<span data-ttu-id="0aab0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aab0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aab0-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0aab0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aab0-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0aab0-137">INPUTS</span></span>

### <span data-ttu-id="0aab0-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0aab0-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0aab0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0aab0-139">OUTPUTS</span></span>

### <span data-ttu-id="0aab0-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="0aab0-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="0aab0-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0aab0-141">NOTES</span></span>

<span data-ttu-id="0aab0-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0aab0-142">ALIASES</span></span>

<span data-ttu-id="0aab0-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0aab0-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0aab0-144">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0aab0-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0aab0-145">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0aab0-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0aab0-146">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0aab0-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0aab0-147">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0aab0-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0aab0-148">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="0aab0-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0aab0-149">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="0aab0-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0aab0-150">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="0aab0-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0aab0-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0aab0-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0aab0-152">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="0aab0-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0aab0-153">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0aab0-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0aab0-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="0aab0-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0aab0-155">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0aab0-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0aab0-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="0aab0-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="0aab0-157">VALUE <IDatabasePrincipal[]>: Die Liste der Kusto-Datenbankprinzipale.</span><span class="sxs-lookup"><span data-stu-id="0aab0-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="0aab0-158">`Name <String>`: Name des Datenbankprinzipals.</span><span class="sxs-lookup"><span data-stu-id="0aab0-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="0aab0-159">`Role <DatabasePrincipalRole>`: Datenbankprinzipalrolle.</span><span class="sxs-lookup"><span data-stu-id="0aab0-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="0aab0-160">`Type <DatabasePrincipalType>`: Datenbankprinzipaltyp.</span><span class="sxs-lookup"><span data-stu-id="0aab0-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="0aab0-161">`[AppId <String>]`: Anwendungs-ID – relevant nur für den Prinzipaltyp der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0aab0-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="0aab0-162">`[Email <String>]`: Datenbankprinzipal-E-Mail,wenn vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0aab0-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="0aab0-163">`[Fqn <String>]`: Vollqualifizierter Name des Datenbankprinzipal.</span><span class="sxs-lookup"><span data-stu-id="0aab0-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="0aab0-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0aab0-164">RELATED LINKS</span></span>

