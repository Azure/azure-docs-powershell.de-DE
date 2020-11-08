---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179179"
---
# <span data-ttu-id="a74fc-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a74fc-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="a74fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a74fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a74fc-103">Löscht eine Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a74fc-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="a74fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a74fc-104">SYNTAX</span></span>

### <span data-ttu-id="a74fc-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a74fc-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a74fc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a74fc-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a74fc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a74fc-107">DESCRIPTION</span></span>
<span data-ttu-id="a74fc-108">Löscht eine Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a74fc-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="a74fc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a74fc-109">EXAMPLES</span></span>

### <span data-ttu-id="a74fc-110">Beispiel 1: Löschen einer vorhandenen Kusto-Datenbank-PrincipalAssignment nach Namen</span><span class="sxs-lookup"><span data-stu-id="a74fc-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="a74fc-111">Der obige Befehl löscht die PrincipalAssignment namens "kustoprincipal1" in der Kusto-Datenbank "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="a74fc-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="a74fc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a74fc-112">PARAMETERS</span></span>

### <span data-ttu-id="a74fc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a74fc-113">-AsJob</span></span>
<span data-ttu-id="a74fc-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a74fc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a74fc-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="a74fc-115">-ClusterName</span></span>
<span data-ttu-id="a74fc-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="a74fc-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a74fc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a74fc-117">-DatabaseName</span></span>
<span data-ttu-id="a74fc-118">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a74fc-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="a74fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74fc-119">-DefaultProfile</span></span>
<span data-ttu-id="a74fc-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a74fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a74fc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a74fc-121">-InputObject</span></span>
<span data-ttu-id="a74fc-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a74fc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a74fc-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a74fc-123">-NoWait</span></span>
<span data-ttu-id="a74fc-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a74fc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a74fc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a74fc-125">-PassThru</span></span>
<span data-ttu-id="a74fc-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="a74fc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a74fc-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a74fc-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="a74fc-128">Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a74fc-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="a74fc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74fc-129">-ResourceGroupName</span></span>
<span data-ttu-id="a74fc-130">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="a74fc-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a74fc-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a74fc-131">-SubscriptionId</span></span>
<span data-ttu-id="a74fc-132">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a74fc-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a74fc-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a74fc-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a74fc-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a74fc-134">-Confirm</span></span>
<span data-ttu-id="a74fc-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a74fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a74fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a74fc-136">-WhatIf</span></span>
<span data-ttu-id="a74fc-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a74fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a74fc-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a74fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a74fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74fc-139">CommonParameters</span></span>
<span data-ttu-id="a74fc-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74fc-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a74fc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74fc-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a74fc-142">INPUTS</span></span>

### <span data-ttu-id="a74fc-143">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a74fc-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a74fc-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a74fc-144">OUTPUTS</span></span>

### <span data-ttu-id="a74fc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a74fc-145">System.Boolean</span></span>

## <span data-ttu-id="a74fc-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="a74fc-146">NOTES</span></span>

<span data-ttu-id="a74fc-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="a74fc-147">ALIASES</span></span>

<span data-ttu-id="a74fc-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a74fc-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a74fc-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a74fc-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a74fc-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a74fc-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a74fc-151">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a74fc-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a74fc-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a74fc-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a74fc-153">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="a74fc-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a74fc-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="a74fc-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a74fc-155">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a74fc-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a74fc-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a74fc-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a74fc-157">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="a74fc-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a74fc-158">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a74fc-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a74fc-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="a74fc-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a74fc-160">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a74fc-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a74fc-161">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a74fc-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a74fc-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a74fc-162">RELATED LINKS</span></span>

