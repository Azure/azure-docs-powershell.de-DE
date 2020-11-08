---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: d7af2877d4823f1da85f08e61035b386d57a9c2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179237"
---
# <span data-ttu-id="f8cce-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f8cce-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="f8cce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8cce-102">SYNOPSIS</span></span>
<span data-ttu-id="f8cce-103">Hinzufügen von Berechtigungen für Datenbankprinzipale</span><span class="sxs-lookup"><span data-stu-id="f8cce-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="f8cce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8cce-104">SYNTAX</span></span>

### <span data-ttu-id="f8cce-105">Addexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8cce-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f8cce-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f8cce-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8cce-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8cce-107">DESCRIPTION</span></span>
<span data-ttu-id="f8cce-108">Hinzufügen von Berechtigungen für Datenbankprinzipale</span><span class="sxs-lookup"><span data-stu-id="f8cce-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="f8cce-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8cce-109">EXAMPLES</span></span>

### <span data-ttu-id="f8cce-110">Beispiel 1: Hinzufügen von Berechtigungen für Datenbankprinzipale</span><span class="sxs-lookup"><span data-stu-id="f8cce-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="f8cce-111">Der obige Befehl fügt Berechtigungen für Datenbankprinzipale hinzu</span><span class="sxs-lookup"><span data-stu-id="f8cce-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="f8cce-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8cce-112">PARAMETERS</span></span>

### <span data-ttu-id="f8cce-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f8cce-113">-ClusterName</span></span>
<span data-ttu-id="f8cce-114">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f8cce-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8cce-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8cce-115">-DatabaseName</span></span>
<span data-ttu-id="f8cce-116">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f8cce-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8cce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8cce-117">-DefaultProfile</span></span>
<span data-ttu-id="f8cce-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8cce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8cce-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8cce-119">-InputObject</span></span>
<span data-ttu-id="f8cce-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f8cce-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8cce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8cce-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8cce-122">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f8cce-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8cce-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f8cce-123">-SubscriptionId</span></span>
<span data-ttu-id="f8cce-124">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f8cce-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8cce-125">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f8cce-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f8cce-126">-Wert</span><span class="sxs-lookup"><span data-stu-id="f8cce-126">-Value</span></span>
<span data-ttu-id="f8cce-127">Die Liste der Kusto-Datenbankprinzipale.</span><span class="sxs-lookup"><span data-stu-id="f8cce-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="f8cce-128">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Wert Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f8cce-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8cce-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8cce-129">-Confirm</span></span>
<span data-ttu-id="f8cce-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8cce-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8cce-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8cce-131">-WhatIf</span></span>
<span data-ttu-id="f8cce-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8cce-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8cce-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8cce-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8cce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8cce-134">CommonParameters</span></span>
<span data-ttu-id="f8cce-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8cce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8cce-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8cce-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8cce-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8cce-137">INPUTS</span></span>

### <span data-ttu-id="f8cce-138">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f8cce-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f8cce-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8cce-139">OUTPUTS</span></span>

### <span data-ttu-id="f8cce-140">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f8cce-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="f8cce-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8cce-141">NOTES</span></span>

<span data-ttu-id="f8cce-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="f8cce-142">ALIASES</span></span>

<span data-ttu-id="f8cce-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8cce-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8cce-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f8cce-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8cce-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f8cce-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8cce-146">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f8cce-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8cce-147">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f8cce-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f8cce-148">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f8cce-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f8cce-149">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="f8cce-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f8cce-150">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f8cce-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f8cce-151">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f8cce-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8cce-152">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="f8cce-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f8cce-153">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f8cce-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f8cce-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f8cce-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f8cce-155">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f8cce-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f8cce-156">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f8cce-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="f8cce-157">Value <IDatabasePrincipal [] >: die Liste der Kusto-Datenbankprinzipale.</span><span class="sxs-lookup"><span data-stu-id="f8cce-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="f8cce-158">`Name <String>`: Name des Datenbankprinzipals.</span><span class="sxs-lookup"><span data-stu-id="f8cce-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="f8cce-159">`Role <DatabasePrincipalRole>`: Datenbankprinzipal Rolle.</span><span class="sxs-lookup"><span data-stu-id="f8cce-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="f8cce-160">`Type <DatabasePrincipalType>`: Daten Bank Prinzipaltyp.</span><span class="sxs-lookup"><span data-stu-id="f8cce-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="f8cce-161">`[AppId <String>]`: Anwendungs-ID – nur relevant für den Typ des anwendungsprinzipals.</span><span class="sxs-lookup"><span data-stu-id="f8cce-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="f8cce-162">`[Email <String>]`: Datenbank-Prinzipal-e-Mail, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f8cce-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="f8cce-163">`[Fqn <String>]`: Vollqualifizierter Name des Datenbankprinzipals.</span><span class="sxs-lookup"><span data-stu-id="f8cce-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="f8cce-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8cce-164">RELATED LINKS</span></span>

