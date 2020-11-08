---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177399"
---
# <span data-ttu-id="4c5f6-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="4c5f6-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="4c5f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5f6-103">Register-AzStackHCI erstellt eine Microsoft. AzureStackHCI-Cloud-Ressource, die den lokalen Cluster darstellt, und registriert den lokalen Cluster mit Azure.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="4c5f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c5f6-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="4c5f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c5f6-105">DESCRIPTION</span></span>
<span data-ttu-id="4c5f6-106">Register-AzStackHCI erstellt eine Microsoft. AzureStackHCI-Cloud-Ressource, die den lokalen Cluster darstellt, und registriert den lokalen Cluster mit Azure.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="4c5f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c5f6-107">EXAMPLES</span></span>

### <span data-ttu-id="4c5f6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c5f6-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="4c5f6-109">C:\PS \> Register-AzStackHCI-Subscription-"12a0f531-56CB-4340-9501-257726d741fd" Ergebnis: Success Resourcen:/Subscriptions/12a0f531-56CB-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="4c5f6-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="4c5f6-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4c5f6-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="4c5f6-111">C:\PS \> Register-AzStackHCI-Subscription-"12a0f531-56CB-4340-9501-257726d741fd"-Computername ClusterNode1 Ergebnis: Success Resourcen:/Subscriptions/12a0f531-56CB-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="4c5f6-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="4c5f6-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4c5f6-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="4c5f6-113">C:\PS \> Register-AzStackHCI-Subscription-"12a0f531-56CB-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-Accounting user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Ergebnis: PendingForAdminConsent/Subscriptions/12a0f531-56CB-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview : PortalResourceURL https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="4c5f6-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="4c5f6-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="4c5f6-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="4c5f6-115">C:\PS \> Register-AzStackHCI-Abonnement-"12a0f531-56CB-4340-9501-257726d741fd"-Region westus-resourceName HciCluster1-tenantal "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken ACee.. rerrer-Accounting user1@corp1.com -environmentname AzureCloud-Computername node1hci-Get-Credential Ergebnis: Success Resourcen:/Subscriptions/12a0f531-56CB-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="4c5f6-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="4c5f6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c5f6-116">PARAMETERS</span></span>

### <span data-ttu-id="4c5f6-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4c5f6-117">-SubscriptionId</span></span>
<span data-ttu-id="4c5f6-118">Gibt das Azure-Abonnement zum Erstellen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="4c5f6-119">Dies ist der einzige obligatorische Parameter.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c5f6-120">-Region</span><span class="sxs-lookup"><span data-stu-id="4c5f6-120">-Region</span></span>
<span data-ttu-id="4c5f6-121">Gibt den Bereich zum Erstellen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="4c5f6-122">Standard ist eastus.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-122">Default is EastUS.</span></span>

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

### <span data-ttu-id="4c5f6-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4c5f6-123">-ResourceName</span></span>
<span data-ttu-id="4c5f6-124">Gibt den Ressourcennamen der in Azure erstellten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="4c5f6-125">Wenn nicht angegeben, wird der lokale Clustername verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-125">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="4c5f6-126">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="4c5f6-126">-TenantId</span></span>
<span data-ttu-id="4c5f6-127">Gibt die Azure-Mandanten-Nr an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-127">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="4c5f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c5f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="4c5f6-129">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="4c5f6-130">Wenn nicht angegeben, \<LocalClusterName\> wird RG als Ressourcengruppenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="4c5f6-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="4c5f6-131">-ArmAccessToken</span></span>
<span data-ttu-id="4c5f6-132">Gibt das Zugriffstoken für den Arm an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="4c5f6-133">Wenn Sie dies zusammen mit GraphAccessToken und der Konto-Nr angeben, wird eine Azure Interactive-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="4c5f6-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="4c5f6-134">-GraphAccessToken</span></span>
<span data-ttu-id="4c5f6-135">Gibt das Diagramm Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="4c5f6-136">Wenn Sie dies zusammen mit ArmAccessToken und der Konto-Nr angeben, wird eine Azure Interactive-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="4c5f6-137">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="4c5f6-137">-AccountId</span></span>
<span data-ttu-id="4c5f6-138">Gibt das Zugriffstoken für den Arm an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="4c5f6-139">Wenn Sie dies zusammen mit ArmAccessToken und GraphAccessToken angeben, wird eine Azure Interactive-Anmeldung vermieden.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c5f6-140">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="4c5f6-140">-EnvironmentName</span></span>
<span data-ttu-id="4c5f6-141">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="4c5f6-142">Der Standardwert ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-142">Default is AzureCloud.</span></span>
<span data-ttu-id="4c5f6-143">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="4c5f6-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c5f6-144">-Computername</span><span class="sxs-lookup"><span data-stu-id="4c5f6-144">-ComputerName</span></span>
<span data-ttu-id="4c5f6-145">Gibt den Clusternamen oder einen Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c5f6-146">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4c5f6-146">-Credential</span></span>
<span data-ttu-id="4c5f6-147">Gibt die Anmeldeinformationen für den Computername an.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="4c5f6-148">Standard ist der aktuelle Benutzer, der das Cmdlet ausführt.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c5f6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5f6-149">CommonParameters</span></span>
<span data-ttu-id="4c5f6-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5f6-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c5f6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5f6-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c5f6-152">INPUTS</span></span>

## <span data-ttu-id="4c5f6-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c5f6-153">OUTPUTS</span></span>

### <span data-ttu-id="4c5f6-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-154">PSCustomObject.</span></span> <span data-ttu-id="4c5f6-155">Gibt die folgenden Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="4c5f6-156">Ergebnis: Erfolg oder Fehler oder PendingForAdminConsent oder storniert.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="4c5f6-157">Resourcen-ID: Ressourcen-ID der in Azure erstellten Ressource.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="4c5f6-158">PortalResourceURL: Azure-Portal-Ressourcen-URL.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="4c5f6-159">PortalAADAppPermissionsURL: Azure Portal URL für die Aad-App-Berechtigungsseite.</span><span class="sxs-lookup"><span data-stu-id="4c5f6-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="4c5f6-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c5f6-160">NOTES</span></span>

## <span data-ttu-id="4c5f6-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c5f6-161">RELATED LINKS</span></span>
