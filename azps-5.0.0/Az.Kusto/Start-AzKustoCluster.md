---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179177"
---
# <span data-ttu-id="8a79a-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8a79a-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="8a79a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a79a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a79a-103">Startet einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="8a79a-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="8a79a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a79a-104">SYNTAX</span></span>

### <span data-ttu-id="8a79a-105">Start (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a79a-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a79a-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a79a-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a79a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a79a-107">DESCRIPTION</span></span>
<span data-ttu-id="8a79a-108">Startet einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="8a79a-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="8a79a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a79a-109">EXAMPLES</span></span>

### <span data-ttu-id="8a79a-110">Beispiel 1: Starten eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="8a79a-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="8a79a-111">Mit dem obigen Befehl wird ein Kusto-Cluster gestartet.</span><span class="sxs-lookup"><span data-stu-id="8a79a-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="8a79a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a79a-112">PARAMETERS</span></span>

### <span data-ttu-id="8a79a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a79a-113">-AsJob</span></span>
<span data-ttu-id="8a79a-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="8a79a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8a79a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a79a-115">-DefaultProfile</span></span>
<span data-ttu-id="8a79a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a79a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a79a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8a79a-117">-InputObject</span></span>
<span data-ttu-id="8a79a-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8a79a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8a79a-119">-Name</span></span>
<span data-ttu-id="8a79a-120">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="8a79a-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a79a-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8a79a-121">-NoWait</span></span>
<span data-ttu-id="8a79a-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="8a79a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8a79a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a79a-123">-PassThru</span></span>
<span data-ttu-id="8a79a-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="8a79a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8a79a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a79a-125">-ResourceGroupName</span></span>
<span data-ttu-id="8a79a-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="8a79a-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a79a-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8a79a-127">-SubscriptionId</span></span>
<span data-ttu-id="8a79a-128">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8a79a-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8a79a-129">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8a79a-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a79a-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a79a-130">-Confirm</span></span>
<span data-ttu-id="8a79a-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a79a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a79a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a79a-132">-WhatIf</span></span>
<span data-ttu-id="8a79a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a79a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a79a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a79a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a79a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a79a-135">CommonParameters</span></span>
<span data-ttu-id="8a79a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a79a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a79a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a79a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a79a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a79a-138">INPUTS</span></span>

### <span data-ttu-id="8a79a-139">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8a79a-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8a79a-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a79a-140">OUTPUTS</span></span>

### <span data-ttu-id="8a79a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a79a-141">System.Boolean</span></span>

## <span data-ttu-id="8a79a-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a79a-142">NOTES</span></span>

<span data-ttu-id="8a79a-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="8a79a-143">ALIASES</span></span>

<span data-ttu-id="8a79a-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8a79a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a79a-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8a79a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a79a-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8a79a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a79a-147">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="8a79a-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a79a-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8a79a-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8a79a-149">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="8a79a-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8a79a-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="8a79a-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8a79a-151">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="8a79a-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8a79a-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="8a79a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a79a-153">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="8a79a-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8a79a-154">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="8a79a-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8a79a-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="8a79a-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8a79a-156">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8a79a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8a79a-157">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8a79a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8a79a-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a79a-158">RELATED LINKS</span></span>

