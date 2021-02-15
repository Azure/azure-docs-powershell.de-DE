---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e5ff59889b2b786d07699a5b9d46937372c0662f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143897"
---
# <span data-ttu-id="da623-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="da623-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="da623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da623-102">SYNOPSIS</span></span>
<span data-ttu-id="da623-103">Unregister-AzStackHCI die Microsoft.AzureStackHCI-Cloudressource, die den lokalen Cluster darstellt, und die Registrierung des lokalen Clusters mit Azure auf.</span><span class="sxs-lookup"><span data-stu-id="da623-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="da623-104">Die für den Cluster verfügbaren registrierten Informationen werden verwendet, um die Registrierung des Cluster auf aufgehoben, wenn keine Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="da623-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="da623-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da623-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da623-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da623-106">DESCRIPTION</span></span>
<span data-ttu-id="da623-107">Unregister-AzStackHCI die Microsoft.AzureStackHCI-Cloudressource, die den lokalen Cluster darstellt, und die Registrierung des lokalen Clusters mit Azure auf.</span><span class="sxs-lookup"><span data-stu-id="da623-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="da623-108">Die für den Cluster verfügbaren registrierten Informationen werden verwendet, um die Registrierung des Cluster auf aufgehoben, wenn keine Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="da623-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="da623-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da623-109">EXAMPLES</span></span>

### <span data-ttu-id="da623-110">BEISPIEL 1</span><span class="sxs-lookup"><span data-stu-id="da623-110">EXAMPLE 1</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
<span data-ttu-id="da623-111">Aufrufen eines Clusterknotens</span><span class="sxs-lookup"><span data-stu-id="da623-111">Invoking on one of the cluster node</span></span>

### <span data-ttu-id="da623-112">BEISPIEL 2</span><span class="sxs-lookup"><span data-stu-id="da623-112">EXAMPLE 2</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
<span data-ttu-id="da623-113">Aufrufen vom Verwaltungsknoten</span><span class="sxs-lookup"><span data-stu-id="da623-113">Invoking from the management node</span></span>

### <span data-ttu-id="da623-114">BEISPIEL 3</span><span class="sxs-lookup"><span data-stu-id="da623-114">EXAMPLE 3</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
<span data-ttu-id="da623-115">Aufrufen aus WAC</span><span class="sxs-lookup"><span data-stu-id="da623-115">Invoking from WAC</span></span>

### <span data-ttu-id="da623-116">BEISPIEL 4</span><span class="sxs-lookup"><span data-stu-id="da623-116">EXAMPLE 4</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
<span data-ttu-id="da623-117">Aufrufen mit allen Parametern</span><span class="sxs-lookup"><span data-stu-id="da623-117">Invoking with all the parameters</span></span>

## <span data-ttu-id="da623-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da623-118">PARAMETERS</span></span>

### <span data-ttu-id="da623-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="da623-119">-AccountId</span></span>
<span data-ttu-id="da623-120">Gibt das ARM Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="da623-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="da623-121">Wenn Sie dies zusammen mit "ArmAccessToken" und "GraphAccessToken" angeben, vermeiden Sie die interaktive Azure-Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="da623-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="da623-122">-ArmAccessToken</span></span>
<span data-ttu-id="da623-123">Gibt das ARM Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="da623-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="da623-124">Wenn Sie dies zusammen mit GraphAccessToken und AccountId angeben, vermeiden Sie interaktive Azure-Anmeldungen.</span><span class="sxs-lookup"><span data-stu-id="da623-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="da623-125">-ComputerName</span></span>
<span data-ttu-id="da623-126">Gibt einen der Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="da623-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="da623-127">-Credential</span></span>
<span data-ttu-id="da623-128">Gibt die Anmeldeinformationen für den Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="da623-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="da623-129">Standard ist der aktuelle Benutzer, der das Cmdlet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da623-129">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="da623-130">-EnvironmentName</span></span>
<span data-ttu-id="da623-131">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="da623-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="da623-132">Der Standardwert ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="da623-132">Default is AzureCloud.</span></span>
<span data-ttu-id="da623-133">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="da623-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="da623-134">-GraphAccessToken</span></span>
<span data-ttu-id="da623-135">Gibt das Zugriffstoken "Graph" an.</span><span class="sxs-lookup"><span data-stu-id="da623-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="da623-136">Wenn Sie dies zusammen mit "ArmAccessToken" und "AccountId" angeben, vermeiden Sie die interaktive Azure-Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="da623-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da623-137">-ResourceGroupName</span></span>
<span data-ttu-id="da623-138">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="da623-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="da623-139">Wenn nicht anders \<LocalClusterName\> angegeben, wird "-rg" als Ressourcengruppenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="da623-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="da623-140">-ResourceName</span></span>
<span data-ttu-id="da623-141">Gibt den Ressourcennamen der in Azure erstellten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="da623-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="da623-142">Wird dieser Wert nicht angegeben, wird der lokale Clustername verwendet.</span><span class="sxs-lookup"><span data-stu-id="da623-142">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da623-143">-SubscriptionId</span></span>
<span data-ttu-id="da623-144">Gibt das Azure-Abonnement an, um die Ressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da623-144">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="da623-145">-TenantId</span></span>
<span data-ttu-id="da623-146">Gibt die Azure TenantId an.</span><span class="sxs-lookup"><span data-stu-id="da623-146">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="da623-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="da623-148">Verwenden Sie die Gerätecodeauthentifizierung anstelle einer interaktiven Browseraufforderung.</span><span class="sxs-lookup"><span data-stu-id="da623-148">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da623-149">-Confirm</span></span>
<span data-ttu-id="da623-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da623-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da623-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="da623-151">-WhatIf</span></span>
<span data-ttu-id="da623-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da623-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da623-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da623-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da623-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da623-154">CommonParameters</span></span>
<span data-ttu-id="da623-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da623-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da623-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da623-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da623-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da623-157">INPUTS</span></span>

## <span data-ttu-id="da623-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da623-158">OUTPUTS</span></span>

### <span data-ttu-id="da623-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="da623-159">PSCustomObject.</span></span> <span data-ttu-id="da623-160">Gibt die folgenden Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="da623-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="da623-161">Ergebnis: "Erfolg", "Fehlgeschlagen" oder "Abgebrochen".</span><span class="sxs-lookup"><span data-stu-id="da623-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="da623-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="da623-162">NOTES</span></span>

## <span data-ttu-id="da623-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="da623-163">RELATED LINKS</span></span>
