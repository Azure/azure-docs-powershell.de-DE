---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008420"
---
# <span data-ttu-id="8e6f2-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="8e6f2-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="8e6f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6f2-103">Löscht die Datenbank mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="8e6f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e6f2-104">SYNTAX</span></span>

### <span data-ttu-id="8e6f2-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e6f2-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8e6f2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e6f2-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e6f2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e6f2-107">DESCRIPTION</span></span>
<span data-ttu-id="8e6f2-108">Löscht die Datenbank mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="8e6f2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e6f2-109">EXAMPLES</span></span>

### <span data-ttu-id="8e6f2-110">Beispiel 1: Löschen einer vorhandenen Kusto-Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="8e6f2-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="8e6f2-111">Der obige Befehl löscht die Kusto-Datenbank mit dem Namen "mykustodatabase" im Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="8e6f2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e6f2-112">PARAMETERS</span></span>

### <span data-ttu-id="8e6f2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e6f2-113">-AsJob</span></span>
<span data-ttu-id="8e6f2-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="8e6f2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8e6f2-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="8e6f2-115">-ClusterName</span></span>
<span data-ttu-id="8e6f2-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e6f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e6f2-117">-DefaultProfile</span></span>
<span data-ttu-id="8e6f2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e6f2-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e6f2-119">-InputObject</span></span>
<span data-ttu-id="8e6f2-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e6f2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8e6f2-121">-Name</span></span>
<span data-ttu-id="8e6f2-122">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e6f2-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8e6f2-123">-NoWait</span></span>
<span data-ttu-id="8e6f2-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="8e6f2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8e6f2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e6f2-125">-PassThru</span></span>
<span data-ttu-id="8e6f2-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="8e6f2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8e6f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e6f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e6f2-128">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e6f2-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8e6f2-129">-SubscriptionId</span></span>
<span data-ttu-id="8e6f2-130">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e6f2-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e6f2-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e6f2-132">-Confirm</span></span>
<span data-ttu-id="8e6f2-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e6f2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e6f2-134">-WhatIf</span></span>
<span data-ttu-id="8e6f2-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e6f2-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e6f2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6f2-137">CommonParameters</span></span>
<span data-ttu-id="8e6f2-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6f2-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e6f2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6f2-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e6f2-140">INPUTS</span></span>

### <span data-ttu-id="8e6f2-141">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8e6f2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8e6f2-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e6f2-142">OUTPUTS</span></span>

### <span data-ttu-id="8e6f2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e6f2-143">System.Boolean</span></span>

## <span data-ttu-id="8e6f2-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e6f2-144">NOTES</span></span>

<span data-ttu-id="8e6f2-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="8e6f2-145">ALIASES</span></span>

<span data-ttu-id="8e6f2-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e6f2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e6f2-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e6f2-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e6f2-149">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="8e6f2-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e6f2-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8e6f2-151">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8e6f2-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8e6f2-153">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8e6f2-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="8e6f2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e6f2-155">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8e6f2-156">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8e6f2-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8e6f2-158">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8e6f2-159">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8e6f2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8e6f2-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e6f2-160">RELATED LINKS</span></span>

