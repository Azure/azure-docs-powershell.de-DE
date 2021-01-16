---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374196"
---
# <span data-ttu-id="005ad-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="005ad-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="005ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="005ad-102">SYNOPSIS</span></span>
<span data-ttu-id="005ad-103">Unregister-AzStackHCI die Microsoft.AzureStackHCI-Cloudressource, die den lokalen Cluster darstellt, und die Registrierung des lokalen Clusters mit Azure auf.</span><span class="sxs-lookup"><span data-stu-id="005ad-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="005ad-104">Die registrierten Informationen, die für den Cluster verfügbar sind, werden verwendet, um die Registrierung des Cluster auf aufgehoben, wenn keine Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="005ad-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="005ad-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="005ad-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="005ad-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="005ad-106">DESCRIPTION</span></span>
<span data-ttu-id="005ad-107">Unregister-AzStackHCI die Microsoft.AzureStackHCI-Cloudressource, die den lokalen Cluster darstellt, und die Registrierung des lokalen Clusters mit Azure auf.</span><span class="sxs-lookup"><span data-stu-id="005ad-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="005ad-108">Die registrierten Informationen, die für den Cluster verfügbar sind, werden verwendet, um die Registrierung des Cluster auf aufgehoben, wenn keine Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="005ad-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="005ad-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="005ad-109">EXAMPLES</span></span>

### <span data-ttu-id="005ad-110">BEISPIEL 1</span><span class="sxs-lookup"><span data-stu-id="005ad-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="005ad-111">C:\PS \> Registrierung aufheben-AzStackHCI-Ergebnis: Success</span><span class="sxs-lookup"><span data-stu-id="005ad-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="005ad-112">BEISPIEL 2</span><span class="sxs-lookup"><span data-stu-id="005ad-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="005ad-113">C:\PS \> Registrierung aufheben-AzStackHCI -ComputerName ClusterNode1 Ergebnis: Success</span><span class="sxs-lookup"><span data-stu-id="005ad-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="005ad-114">BEISPIEL 3</span><span class="sxs-lookup"><span data-stu-id="005ad-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="005ad-115">C:\PS \> Registrierung aufheben-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer.. ere= -GraphAccessToken acyee.. rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span><span class="sxs-lookup"><span data-stu-id="005ad-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="005ad-116">BEISPIEL 4</span><span class="sxs-lookup"><span data-stu-id="005ad-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="005ad-117">C:\PS \> Registrierung aufheben-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer.. ere= -GraphAccessToken acee.. rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span><span class="sxs-lookup"><span data-stu-id="005ad-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="005ad-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="005ad-118">PARAMETERS</span></span>

### <span data-ttu-id="005ad-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="005ad-119">-AccountId</span></span>
<span data-ttu-id="005ad-120">Gibt das ARM Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="005ad-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="005ad-121">Wenn Sie dies zusammen mit "ArmAccessToken" und "GraphAccessToken" angeben, vermeiden Sie die interaktive Azure-Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="005ad-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="005ad-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="005ad-122">-ArmAccessToken</span></span>
<span data-ttu-id="005ad-123">Gibt das ARM Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="005ad-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="005ad-124">Wenn Sie dies zusammen mit GraphAccessToken und AccountId angeben, vermeiden Sie interaktive Azure-Anmeldungen.</span><span class="sxs-lookup"><span data-stu-id="005ad-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="005ad-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="005ad-125">-ComputerName</span></span>
<span data-ttu-id="005ad-126">Gibt einen der Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="005ad-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="005ad-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="005ad-127">-Credential</span></span>
<span data-ttu-id="005ad-128">Gibt die Anmeldeinformationen für den Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="005ad-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="005ad-129">Standard ist der aktuelle Benutzer, der das Cmdlet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="005ad-129">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="005ad-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="005ad-130">-EnvironmentName</span></span>
<span data-ttu-id="005ad-131">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="005ad-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="005ad-132">Der Standardwert ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="005ad-132">Default is AzureCloud.</span></span>
<span data-ttu-id="005ad-133">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="005ad-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="005ad-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="005ad-134">-GraphAccessToken</span></span>
<span data-ttu-id="005ad-135">Gibt das Zugriffstoken "Graph" an.</span><span class="sxs-lookup"><span data-stu-id="005ad-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="005ad-136">Wenn Sie dies zusammen mit "ArmAccessToken" und "AccountId" angeben, vermeiden Sie die interaktive Azure-Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="005ad-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="005ad-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="005ad-137">-ResourceGroupName</span></span>
<span data-ttu-id="005ad-138">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="005ad-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="005ad-139">Wenn nicht anders \<LocalClusterName\> angegeben, wird "-rg" als Ressourcengruppenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="005ad-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="005ad-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="005ad-140">-ResourceName</span></span>
<span data-ttu-id="005ad-141">Gibt den Ressourcennamen der in Azure erstellten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="005ad-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="005ad-142">Wird dieser Wert nicht angegeben, wird der lokale Clustername verwendet.</span><span class="sxs-lookup"><span data-stu-id="005ad-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="005ad-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="005ad-143">-SubscriptionId</span></span>
<span data-ttu-id="005ad-144">Gibt das Azure-Abonnement an, um die Ressource zu erstellen</span><span class="sxs-lookup"><span data-stu-id="005ad-144">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="005ad-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="005ad-145">-TenantId</span></span>
<span data-ttu-id="005ad-146">Gibt die Azure TenantId an.</span><span class="sxs-lookup"><span data-stu-id="005ad-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="005ad-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="005ad-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="005ad-148">Verwenden Sie die Gerätecodeauthentifizierung anstelle einer interaktiven Browseraufforderung.</span><span class="sxs-lookup"><span data-stu-id="005ad-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="005ad-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="005ad-149">-Confirm</span></span>
<span data-ttu-id="005ad-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="005ad-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="005ad-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="005ad-151">-WhatIf</span></span>
<span data-ttu-id="005ad-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="005ad-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="005ad-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="005ad-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="005ad-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="005ad-154">CommonParameters</span></span>
<span data-ttu-id="005ad-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="005ad-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="005ad-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="005ad-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="005ad-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="005ad-157">INPUTS</span></span>

## <span data-ttu-id="005ad-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="005ad-158">OUTPUTS</span></span>

### <span data-ttu-id="005ad-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="005ad-159">PSCustomObject.</span></span> <span data-ttu-id="005ad-160">Gibt die folgenden Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="005ad-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="005ad-161">Ergebnis: "Erfolg", "Fehlgeschlagen" oder "Abgebrochen".</span><span class="sxs-lookup"><span data-stu-id="005ad-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="005ad-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="005ad-162">NOTES</span></span>

## <span data-ttu-id="005ad-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="005ad-163">RELATED LINKS</span></span>
