---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: d7af2877d4823f1da85f08e61035b386d57a9c2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361625"
---
# <span data-ttu-id="d28f5-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="d28f5-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="d28f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d28f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d28f5-103">Berechtigungen zum Hinzufügen von Datenbankprinzipalen</span><span class="sxs-lookup"><span data-stu-id="d28f5-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="d28f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d28f5-104">SYNTAX</span></span>

### <span data-ttu-id="d28f5-105">AddExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d28f5-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d28f5-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d28f5-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d28f5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d28f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d28f5-108">Berechtigungen zum Hinzufügen von Datenbankprinzipalen</span><span class="sxs-lookup"><span data-stu-id="d28f5-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="d28f5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d28f5-109">EXAMPLES</span></span>

### <span data-ttu-id="d28f5-110">Beispiel 1: Hinzufügen von Berechtigungen für Datenbankprinzipale</span><span class="sxs-lookup"><span data-stu-id="d28f5-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="d28f5-111">Der oben aufgeführte Befehl fügt Datenbankprinzipalberechtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="d28f5-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="d28f5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d28f5-112">PARAMETERS</span></span>

### <span data-ttu-id="d28f5-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d28f5-113">-ClusterName</span></span>
<span data-ttu-id="d28f5-114">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d28f5-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d28f5-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d28f5-115">-DatabaseName</span></span>
<span data-ttu-id="d28f5-116">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="d28f5-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d28f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d28f5-117">-DefaultProfile</span></span>
<span data-ttu-id="d28f5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d28f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d28f5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d28f5-119">-InputObject</span></span>
<span data-ttu-id="d28f5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d28f5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d28f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d28f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="d28f5-122">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="d28f5-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d28f5-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d28f5-123">-SubscriptionId</span></span>
<span data-ttu-id="d28f5-124">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d28f5-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d28f5-125">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d28f5-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d28f5-126">-Value</span><span class="sxs-lookup"><span data-stu-id="d28f5-126">-Value</span></span>
<span data-ttu-id="d28f5-127">Die Liste der Kusto-Datenbankprinzipale.</span><span class="sxs-lookup"><span data-stu-id="d28f5-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="d28f5-128">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d28f5-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="d28f5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d28f5-129">-Confirm</span></span>
<span data-ttu-id="d28f5-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d28f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d28f5-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d28f5-131">-WhatIf</span></span>
<span data-ttu-id="d28f5-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d28f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d28f5-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d28f5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d28f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d28f5-134">CommonParameters</span></span>
<span data-ttu-id="d28f5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d28f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d28f5-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d28f5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d28f5-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d28f5-137">INPUTS</span></span>

### <span data-ttu-id="d28f5-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d28f5-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d28f5-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d28f5-139">OUTPUTS</span></span>

### <span data-ttu-id="d28f5-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="d28f5-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="d28f5-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d28f5-141">NOTES</span></span>

<span data-ttu-id="d28f5-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d28f5-142">ALIASES</span></span>

<span data-ttu-id="d28f5-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d28f5-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d28f5-144">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d28f5-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d28f5-145">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d28f5-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d28f5-146">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d28f5-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d28f5-147">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d28f5-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d28f5-148">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d28f5-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d28f5-149">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="d28f5-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d28f5-150">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="d28f5-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d28f5-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d28f5-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d28f5-152">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="d28f5-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d28f5-153">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d28f5-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d28f5-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="d28f5-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d28f5-155">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d28f5-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d28f5-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d28f5-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d28f5-157">VALUE <IDatabasePrincipal[]>: Die Liste der Kusto-Datenbankprinzipale.</span><span class="sxs-lookup"><span data-stu-id="d28f5-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="d28f5-158">`Name <String>`: Name des Datenbankprinzipals.</span><span class="sxs-lookup"><span data-stu-id="d28f5-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="d28f5-159">`Role <DatabasePrincipalRole>`: Datenbankprinzipalrolle.</span><span class="sxs-lookup"><span data-stu-id="d28f5-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="d28f5-160">`Type <DatabasePrincipalType>`: Datenbankprinzipaltyp.</span><span class="sxs-lookup"><span data-stu-id="d28f5-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="d28f5-161">`[AppId <String>]`: Anwendungs-ID – relevant nur für den Prinzipaltyp der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d28f5-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="d28f5-162">`[Email <String>]`: Datenbankprinzipal-E-Mail,wenn vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d28f5-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="d28f5-163">`[Fqn <String>]`: Vollqualifizierter Name des Datenbankprinzipal.</span><span class="sxs-lookup"><span data-stu-id="d28f5-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="d28f5-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d28f5-164">RELATED LINKS</span></span>

