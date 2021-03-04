---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: 3f38a11cd5d4a124e7db7a99422239f73cbe96dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930715"
---
# <span data-ttu-id="07ead-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="07ead-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="07ead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ead-102">SYNOPSIS</span></span>
<span data-ttu-id="07ead-103">Unregister-AzStackHCI löscht die Microsoft.AzureStackHCI-Cloudressource, die den lokalen Cluster darstellt, und registriert den lokalen Cluster bei Azure.</span><span class="sxs-lookup"><span data-stu-id="07ead-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="07ead-104">Die im Cluster verfügbaren registrierten Informationen werden zum Aufheben der Registrierung des Clusters verwendet, wenn keine Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="07ead-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="07ead-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07ead-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07ead-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07ead-106">DESCRIPTION</span></span>
<span data-ttu-id="07ead-107">Unregister-AzStackHCI löscht die Microsoft.AzureStackHCI-Cloudressource, die den lokalen Cluster darstellt, und registriert den lokalen Cluster bei Azure.</span><span class="sxs-lookup"><span data-stu-id="07ead-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="07ead-108">Die im Cluster verfügbaren registrierten Informationen werden zum Aufheben der Registrierung des Clusters verwendet, wenn keine Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="07ead-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="07ead-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07ead-109">EXAMPLES</span></span>

### <span data-ttu-id="07ead-110">BEISPIEL 1</span><span class="sxs-lookup"><span data-stu-id="07ead-110">EXAMPLE 1</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
<span data-ttu-id="07ead-111">Aufrufen eines Clusterknotens</span><span class="sxs-lookup"><span data-stu-id="07ead-111">Invoking on one of the cluster node</span></span>

### <span data-ttu-id="07ead-112">BEISPIEL 2</span><span class="sxs-lookup"><span data-stu-id="07ead-112">EXAMPLE 2</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
<span data-ttu-id="07ead-113">Aufrufen über den Verwaltungsknoten</span><span class="sxs-lookup"><span data-stu-id="07ead-113">Invoking from the management node</span></span>

### <span data-ttu-id="07ead-114">BEISPIEL 3</span><span class="sxs-lookup"><span data-stu-id="07ead-114">EXAMPLE 3</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
<span data-ttu-id="07ead-115">Aufrufen von WAC</span><span class="sxs-lookup"><span data-stu-id="07ead-115">Invoking from WAC</span></span>

### <span data-ttu-id="07ead-116">BEISPIEL 4</span><span class="sxs-lookup"><span data-stu-id="07ead-116">EXAMPLE 4</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
<span data-ttu-id="07ead-117">Aufrufen mit allen Parametern</span><span class="sxs-lookup"><span data-stu-id="07ead-117">Invoking with all the parameters</span></span>

## <span data-ttu-id="07ead-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="07ead-118">PARAMETERS</span></span>

### <span data-ttu-id="07ead-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="07ead-119">-AccountId</span></span>
<span data-ttu-id="07ead-120">Gibt das zugriffstoken ARM an.</span><span class="sxs-lookup"><span data-stu-id="07ead-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="07ead-121">Wenn Sie dies zusammen mit ArmAccessToken und GraphAccessToken angeben, wird die interaktive Azure-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="07ead-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="07ead-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="07ead-122">-ArmAccessToken</span></span>
<span data-ttu-id="07ead-123">Gibt das zugriffstoken ARM an.</span><span class="sxs-lookup"><span data-stu-id="07ead-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="07ead-124">Wenn Sie dies zusammen mit GraphAccessToken und AccountId angeben, wird die interaktive Azure-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="07ead-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="07ead-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="07ead-125">-ComputerName</span></span>
<span data-ttu-id="07ead-126">Gibt einen der Clusterknoten im lokalen Cluster an, der bei Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="07ead-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="07ead-127">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="07ead-127">-Credential</span></span>
<span data-ttu-id="07ead-128">Gibt die Anmeldeinformationen für den Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="07ead-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="07ead-129">Standardmäßig wird das Cmdlet vom aktuellen Benutzer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07ead-129">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="07ead-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="07ead-130">-EnvironmentName</span></span>
<span data-ttu-id="07ead-131">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="07ead-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="07ead-132">Standardmäßig ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="07ead-132">Default is AzureCloud.</span></span>
<span data-ttu-id="07ead-133">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="07ead-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="07ead-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="07ead-134">-GraphAccessToken</span></span>
<span data-ttu-id="07ead-135">Gibt das Zugriffstoken "Graph" an.</span><span class="sxs-lookup"><span data-stu-id="07ead-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="07ead-136">Wenn Sie dies zusammen mit ArmAccessToken und AccountId angeben, wird die interaktive Azure-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="07ead-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="07ead-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ead-137">-ResourceGroupName</span></span>
<span data-ttu-id="07ead-138">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="07ead-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="07ead-139">Wenn nicht \<LocalClusterName\> angegeben, wird "-rg" als Ressourcengruppenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="07ead-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="07ead-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="07ead-140">-ResourceName</span></span>
<span data-ttu-id="07ead-141">Gibt den Ressourcennamen der in Azure erstellten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="07ead-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="07ead-142">Wenn nicht angegeben, wird der lokale Clustername verwendet.</span><span class="sxs-lookup"><span data-stu-id="07ead-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="07ead-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07ead-143">-SubscriptionId</span></span>
<span data-ttu-id="07ead-144">Gibt das Azure-Abonnement zum Erstellen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="07ead-144">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="07ead-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="07ead-145">-TenantId</span></span>
<span data-ttu-id="07ead-146">Gibt die Azure TenantId an.</span><span class="sxs-lookup"><span data-stu-id="07ead-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="07ead-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="07ead-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="07ead-148">Verwenden Sie die Gerätecodeauthentifizierung anstelle einer interaktiven Browseraufforderung.</span><span class="sxs-lookup"><span data-stu-id="07ead-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="07ead-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07ead-149">-Confirm</span></span>
<span data-ttu-id="07ead-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07ead-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ead-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ead-151">-WhatIf</span></span>
<span data-ttu-id="07ead-152">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07ead-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07ead-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07ead-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07ead-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ead-154">CommonParameters</span></span>
<span data-ttu-id="07ead-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ead-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ead-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07ead-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ead-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07ead-157">INPUTS</span></span>

## <span data-ttu-id="07ead-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07ead-158">OUTPUTS</span></span>

### <span data-ttu-id="07ead-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="07ead-159">PSCustomObject.</span></span> <span data-ttu-id="07ead-160">Gibt folgende Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="07ead-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="07ead-161">Ergebnis: Erfolg oder Fehlgeschlagen oder Abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="07ead-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="07ead-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="07ead-162">NOTES</span></span>

## <span data-ttu-id="07ead-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="07ead-163">RELATED LINKS</span></span>
