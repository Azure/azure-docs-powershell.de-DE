---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173396"
---
# <span data-ttu-id="c4690-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="c4690-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="c4690-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4690-102">SYNOPSIS</span></span>
<span data-ttu-id="c4690-103">Unregister-AzStackHCI löscht die Microsoft. AzureStackHCI-Cloud-Ressource, die den lokalen Cluster darstellt, und hebt die Registrierung des lokalen Clusters mit Azure auf.</span><span class="sxs-lookup"><span data-stu-id="c4690-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="c4690-104">Die im Cluster verfügbaren registrierten Informationen werden verwendet, um die Registrierung des Clusters aufzuheben, wenn keine Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4690-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="c4690-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4690-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4690-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4690-106">DESCRIPTION</span></span>
<span data-ttu-id="c4690-107">Unregister-AzStackHCI löscht die Microsoft. AzureStackHCI-Cloud-Ressource, die den lokalen Cluster darstellt, und hebt die Registrierung des lokalen Clusters mit Azure auf.</span><span class="sxs-lookup"><span data-stu-id="c4690-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="c4690-108">Die im Cluster verfügbaren registrierten Informationen werden verwendet, um die Registrierung des Clusters aufzuheben, wenn keine Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4690-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="c4690-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4690-109">EXAMPLES</span></span>

### <span data-ttu-id="c4690-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4690-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="c4690-111">C:\PS \> Unregister-AzStackHCI-Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="c4690-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="c4690-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c4690-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="c4690-113">C:\PS \> Unregister-AzStackHCI-Computername ClusterNode1 Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="c4690-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="c4690-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c4690-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="c4690-115">C:\PS \> Unregister-AzStackHCI-Abonnement-"12a0f531-56CB-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-Accounting user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-bestätigen: $false Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="c4690-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="c4690-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="c4690-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="c4690-117">C:\PS \> Unregister-AzStackHCI-Abonnement-"12a0f531-56CB-4340-9501-257726d741fd"-resourceName HciCluster1-tenantal "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken ACee.. rerrer-Account-Nr user1@corp1.com -environmentname AzureCloud-Computername node1hci-Get-Credential Ergebnis für Anmeldeinformationen: Erfolg</span><span class="sxs-lookup"><span data-stu-id="c4690-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="c4690-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4690-118">PARAMETERS</span></span>

### <span data-ttu-id="c4690-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c4690-119">-SubscriptionId</span></span>
<span data-ttu-id="c4690-120">Gibt das Azure-Abonnement zum Erstellen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c4690-120">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c4690-121">-ResourceName</span></span>
<span data-ttu-id="c4690-122">Gibt den Ressourcennamen der in Azure erstellten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c4690-122">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="c4690-123">Wenn nicht angegeben, wird der lokale Clustername verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4690-123">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-124">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="c4690-124">-TenantId</span></span>
<span data-ttu-id="c4690-125">Gibt die Azure-Mandanten-Nr an.</span><span class="sxs-lookup"><span data-stu-id="c4690-125">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4690-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4690-127">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c4690-127">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="c4690-128">Wenn nicht angegeben, \<LocalClusterName\> wird RG als Ressourcengruppenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4690-128">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-129">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="c4690-129">-ArmAccessToken</span></span>
<span data-ttu-id="c4690-130">Gibt das Zugriffstoken für den Arm an.</span><span class="sxs-lookup"><span data-stu-id="c4690-130">Specifies the ARM access token.</span></span>
<span data-ttu-id="c4690-131">Wenn Sie dies zusammen mit GraphAccessToken und der Konto-Nr angeben, wird eine Azure Interactive-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="c4690-131">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-132">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="c4690-132">-GraphAccessToken</span></span>
<span data-ttu-id="c4690-133">Gibt das Diagramm Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="c4690-133">Specifies the Graph access token.</span></span>
<span data-ttu-id="c4690-134">Wenn Sie dies zusammen mit ArmAccessToken und der Konto-Nr angeben, wird eine Azure Interactive-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="c4690-134">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-135">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="c4690-135">-AccountId</span></span>
<span data-ttu-id="c4690-136">Gibt das Zugriffstoken für den Arm an.</span><span class="sxs-lookup"><span data-stu-id="c4690-136">Specifies the ARM access token.</span></span>
<span data-ttu-id="c4690-137">Wenn Sie dies zusammen mit ArmAccessToken und GraphAccessToken angeben, wird eine Azure Interactive-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="c4690-137">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-138">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="c4690-138">-EnvironmentName</span></span>
<span data-ttu-id="c4690-139">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="c4690-139">Specifies the Azure Environment.</span></span>
<span data-ttu-id="c4690-140">Der Standardwert ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="c4690-140">Default is AzureCloud.</span></span>
<span data-ttu-id="c4690-141">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="c4690-141">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-142">-Computername</span><span class="sxs-lookup"><span data-stu-id="c4690-142">-ComputerName</span></span>
<span data-ttu-id="c4690-143">Gibt einen der Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="c4690-143">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-144">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="c4690-144">-Credential</span></span>
<span data-ttu-id="c4690-145">Gibt die Anmeldeinformationen für den Computername an.</span><span class="sxs-lookup"><span data-stu-id="c4690-145">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="c4690-146">Standard ist der aktuelle Benutzer, der das Cmdlet ausführt.</span><span class="sxs-lookup"><span data-stu-id="c4690-146">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4690-147">-WhatIf</span></span>
<span data-ttu-id="c4690-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4690-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4690-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4690-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4690-150">-Confirm</span></span>
<span data-ttu-id="c4690-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4690-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4690-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4690-152">CommonParameters</span></span>
<span data-ttu-id="c4690-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4690-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4690-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4690-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4690-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4690-155">INPUTS</span></span>

## <span data-ttu-id="c4690-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4690-156">OUTPUTS</span></span>

### <span data-ttu-id="c4690-157">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="c4690-157">PSCustomObject.</span></span> <span data-ttu-id="c4690-158">Gibt die folgenden Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="c4690-158">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="c4690-159">Ergebnis: Erfolg oder Fehler oder storniert.</span><span class="sxs-lookup"><span data-stu-id="c4690-159">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="c4690-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4690-160">NOTES</span></span>

## <span data-ttu-id="c4690-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4690-161">RELATED LINKS</span></span>
