---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: ad9c09118252499f99708ae99d36ee9ba2418ff2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460592"
---
# <span data-ttu-id="c58b9-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="c58b9-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="c58b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c58b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c58b9-103">Register-AzStackHCI erstellt eine Microsoft.AzureStackHCI-Cloudressource, die den lokalen Cluster darstellt, und registriert den lokalen Cluster bei Azure.</span><span class="sxs-lookup"><span data-stu-id="c58b9-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="c58b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c58b9-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="c58b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c58b9-105">DESCRIPTION</span></span>
<span data-ttu-id="c58b9-106">Register-AzStackHCI erstellt eine Microsoft.AzureStackHCI-Cloudressource, die den lokalen Cluster darstellt, und registriert den lokalen Cluster bei Azure.</span><span class="sxs-lookup"><span data-stu-id="c58b9-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="c58b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c58b9-107">EXAMPLES</span></span>

### <span data-ttu-id="c58b9-108">BEISPIEL 1</span><span class="sxs-lookup"><span data-stu-id="c58b9-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="c58b9-109">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Ergebnis: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/cluster/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="c58b9-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="c58b9-110">BEISPIEL 2</span><span class="sxs-lookup"><span data-stu-id="c58b9-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="c58b9-111">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Ergebnis: Success ResourceId: /subscriptions/12a0f53 1-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/cluster/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="c58b9-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="c58b9-112">BEISPIEL 3</span><span class="sxs-lookup"><span data-stu-id="c58b9-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="c58b9-113">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer.. ere= -GraphAccessToken acyee.. rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/cluster/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="c58b9-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="c58b9-114">BEISPIEL 4</span><span class="sxs-lookup"><span data-stu-id="c58b9-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="c58b9-115">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer.. ere= -GraphAccessToken acee.. rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-950 257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/cluster/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="c58b9-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="c58b9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c58b9-116">PARAMETERS</span></span>

### <span data-ttu-id="c58b9-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="c58b9-117">-AccountId</span></span>
<span data-ttu-id="c58b9-118">Gibt das ARM Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="c58b9-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="c58b9-119">Wenn Sie dies zusammen mit "ArmAccessToken" und "GraphAccessToken" angeben, vermeiden Sie die interaktive Azure-Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="c58b9-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58b9-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="c58b9-120">-ArmAccessToken</span></span>
<span data-ttu-id="c58b9-121">Gibt das ARM Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="c58b9-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="c58b9-122">Wenn Sie dies zusammen mit GraphAccessToken und AccountId angeben, vermeiden Sie interaktive Azure-Anmeldungen.</span><span class="sxs-lookup"><span data-stu-id="c58b9-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="c58b9-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c58b9-123">-CertificateThumbprint</span></span>
<span data-ttu-id="c58b9-124">Gibt den Fingerabdruck des Zertifikats an, das für alle Knoten verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c58b9-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="c58b9-125">Der Benutzer ist für die Verwaltung des Zertifikats zuständig.</span><span class="sxs-lookup"><span data-stu-id="c58b9-125">User is responsible for managing the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58b9-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="c58b9-126">-ComputerName</span></span>
<span data-ttu-id="c58b9-127">Gibt den Clusternamen oder einen der Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="c58b9-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58b9-128">-Credential</span><span class="sxs-lookup"><span data-stu-id="c58b9-128">-Credential</span></span>
<span data-ttu-id="c58b9-129">Gibt die Anmeldeinformationen für den Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="c58b9-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="c58b9-130">Standard ist der aktuelle Benutzer, der das Cmdlet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c58b9-130">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58b9-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="c58b9-131">-EnvironmentName</span></span>
<span data-ttu-id="c58b9-132">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="c58b9-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="c58b9-133">Der Standardwert ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="c58b9-133">Default is AzureCloud.</span></span>
<span data-ttu-id="c58b9-134">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="c58b9-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58b9-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="c58b9-135">-GraphAccessToken</span></span>
<span data-ttu-id="c58b9-136">Gibt das Zugriffstoken "Graph" an.</span><span class="sxs-lookup"><span data-stu-id="c58b9-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="c58b9-137">Wenn Sie dies zusammen mit "ArmAccessToken" und "AccountId" angeben, vermeiden Sie die interaktive Azure-Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="c58b9-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="c58b9-138">-Region</span><span class="sxs-lookup"><span data-stu-id="c58b9-138">-Region</span></span>
<span data-ttu-id="c58b9-139">Gibt die Region an, in der die Ressource erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c58b9-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="c58b9-140">Der Standardwert ist "EastUS".</span><span class="sxs-lookup"><span data-stu-id="c58b9-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="c58b9-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="c58b9-141">-RepairRegistration</span></span>
<span data-ttu-id="c58b9-142">Reparieren sie die aktuelle Azure Stack -HCI-Registrierung mit der Cloud.</span><span class="sxs-lookup"><span data-stu-id="c58b9-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="c58b9-143">Dieses Cmdlet löscht die lokalen Zertifikate für die gruppierten Knoten und die Remotezertifikate in der Azure AD-Anwendung in der Cloud und generiert neue Ersatzzertifikate für beide.</span><span class="sxs-lookup"><span data-stu-id="c58b9-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="c58b9-144">Die Ressourcengruppe, der Ressourcenname und andere Registrierungsmöglichkeiten bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="c58b9-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="c58b9-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c58b9-145">-ResourceGroupName</span></span>
<span data-ttu-id="c58b9-146">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c58b9-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="c58b9-147">Wenn nicht anders \<LocalClusterName\> angegeben, wird "-rg" als Ressourcengruppenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="c58b9-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="c58b9-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c58b9-148">-ResourceName</span></span>
<span data-ttu-id="c58b9-149">Gibt den Ressourcennamen der in Azure erstellten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c58b9-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="c58b9-150">Wird dieser Wert nicht angegeben, wird der lokale Clustername verwendet.</span><span class="sxs-lookup"><span data-stu-id="c58b9-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="c58b9-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c58b9-151">-SubscriptionId</span></span>
<span data-ttu-id="c58b9-152">Gibt das Azure-Abonnement an, um die Ressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c58b9-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="c58b9-153">Dies ist der einzige obligatorische Parameter.</span><span class="sxs-lookup"><span data-stu-id="c58b9-153">This is the only Mandatory parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58b9-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c58b9-154">-TenantId</span></span>
<span data-ttu-id="c58b9-155">Gibt die Azure TenantId an.</span><span class="sxs-lookup"><span data-stu-id="c58b9-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="c58b9-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="c58b9-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="c58b9-157">Verwenden Sie die Gerätecodeauthentifizierung anstelle einer interaktiven Browseraufforderung.</span><span class="sxs-lookup"><span data-stu-id="c58b9-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="c58b9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58b9-158">CommonParameters</span></span>
<span data-ttu-id="c58b9-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c58b9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58b9-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c58b9-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58b9-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c58b9-161">INPUTS</span></span>

## <span data-ttu-id="c58b9-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c58b9-162">OUTPUTS</span></span>

### <span data-ttu-id="c58b9-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="c58b9-163">PSCustomObject.</span></span> <span data-ttu-id="c58b9-164">Gibt die folgenden Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="c58b9-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="c58b9-165">Ergebnis: Success or Failed or PendingForAdminConsent or Cancelled.</span><span class="sxs-lookup"><span data-stu-id="c58b9-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="c58b9-166">ResourceId: Ressourcen-ID der in Azure erstellten Ressource.</span><span class="sxs-lookup"><span data-stu-id="c58b9-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="c58b9-167">PortalResourceURL: Ressourcen-URL des Azure-Portals.</span><span class="sxs-lookup"><span data-stu-id="c58b9-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="c58b9-168">PortalAADAppPermissionsURL: Azure-Portal-URL für die Berechtigungsseite einer AAD-App.</span><span class="sxs-lookup"><span data-stu-id="c58b9-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="c58b9-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c58b9-169">NOTES</span></span>

## <span data-ttu-id="c58b9-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c58b9-170">RELATED LINKS</span></span>
