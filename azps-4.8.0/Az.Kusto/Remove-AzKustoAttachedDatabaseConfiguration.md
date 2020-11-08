---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008425"
---
# <span data-ttu-id="08b5f-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="08b5f-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="08b5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="08b5f-103">Löscht die angefügte Datenbankkonfiguration mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="08b5f-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="08b5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08b5f-104">SYNTAX</span></span>

### <span data-ttu-id="08b5f-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="08b5f-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="08b5f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="08b5f-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08b5f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08b5f-107">DESCRIPTION</span></span>
<span data-ttu-id="08b5f-108">Löscht die angefügte Datenbankkonfiguration mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="08b5f-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="08b5f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08b5f-109">EXAMPLES</span></span>

### <span data-ttu-id="08b5f-110">Beispiel 1: Löschen eines vorhandenen AttachedDatabaseConfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="08b5f-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="08b5f-111">Der obige Befehl löscht die im AttachedDatabaseConfiguration "myfollowerconfiguration" definierte Nachfolger Datenbank aus dem Cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="08b5f-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="08b5f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="08b5f-112">PARAMETERS</span></span>

### <span data-ttu-id="08b5f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08b5f-113">-AsJob</span></span>
<span data-ttu-id="08b5f-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="08b5f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="08b5f-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="08b5f-115">-ClusterName</span></span>
<span data-ttu-id="08b5f-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="08b5f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="08b5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b5f-117">-DefaultProfile</span></span>
<span data-ttu-id="08b5f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08b5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08b5f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="08b5f-119">-InputObject</span></span>
<span data-ttu-id="08b5f-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="08b5f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="08b5f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="08b5f-121">-Name</span></span>
<span data-ttu-id="08b5f-122">Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="08b5f-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b5f-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="08b5f-123">-NoWait</span></span>
<span data-ttu-id="08b5f-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="08b5f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="08b5f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08b5f-125">-PassThru</span></span>
<span data-ttu-id="08b5f-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="08b5f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="08b5f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b5f-127">-ResourceGroupName</span></span>
<span data-ttu-id="08b5f-128">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="08b5f-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="08b5f-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="08b5f-129">-SubscriptionId</span></span>
<span data-ttu-id="08b5f-130">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="08b5f-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="08b5f-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="08b5f-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="08b5f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08b5f-132">-Confirm</span></span>
<span data-ttu-id="08b5f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08b5f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b5f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08b5f-134">-WhatIf</span></span>
<span data-ttu-id="08b5f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08b5f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08b5f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08b5f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08b5f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b5f-137">CommonParameters</span></span>
<span data-ttu-id="08b5f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b5f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b5f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08b5f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b5f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08b5f-140">INPUTS</span></span>

### <span data-ttu-id="08b5f-141">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="08b5f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="08b5f-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08b5f-142">OUTPUTS</span></span>

### <span data-ttu-id="08b5f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08b5f-143">System.Boolean</span></span>

## <span data-ttu-id="08b5f-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="08b5f-144">NOTES</span></span>

<span data-ttu-id="08b5f-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="08b5f-145">ALIASES</span></span>

<span data-ttu-id="08b5f-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08b5f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="08b5f-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08b5f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08b5f-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="08b5f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="08b5f-149">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="08b5f-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="08b5f-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="08b5f-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="08b5f-151">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="08b5f-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="08b5f-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="08b5f-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="08b5f-153">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="08b5f-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="08b5f-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="08b5f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="08b5f-155">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="08b5f-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="08b5f-156">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="08b5f-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="08b5f-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="08b5f-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="08b5f-158">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="08b5f-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="08b5f-159">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="08b5f-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="08b5f-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08b5f-160">RELATED LINKS</span></span>

