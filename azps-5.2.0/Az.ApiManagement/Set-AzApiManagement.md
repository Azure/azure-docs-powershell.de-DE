---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296584"
---
# <span data-ttu-id="5d8bf-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d8bf-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="5d8bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8bf-103">Aktualisiert einen Azure API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="5d8bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d8bf-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d8bf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d8bf-105">DESCRIPTION</span></span>

<span data-ttu-id="5d8bf-106">Das **Cmdlet Set-AzApiManagement** aktualisiert einen Azure API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="5d8bf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d8bf-107">EXAMPLES</span></span>

### <span data-ttu-id="5d8bf-108">Beispiel 1: Abrufen eines API-Verwaltungsdiensts, Skalieren auf Premium und Hinzufügen einer Region</span><span class="sxs-lookup"><span data-stu-id="5d8bf-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="5d8bf-109">Dieses Beispiel ruft eine Api-Verwaltungsinstanz ab, skaliert sie auf fünf Premiumeinheiten und fügt der Premiumregion weitere drei Einheiten hinzu.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="5d8bf-110">Beispiel 2: Aktualisieren der Bereitstellung (externes VNET)</span><span class="sxs-lookup"><span data-stu-id="5d8bf-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="5d8bf-111">Dieser Befehl aktualisiert eine vorhandene API-Verwaltungsbereitstellung und wird einem externen *VpnType beitreten.*</span><span class="sxs-lookup"><span data-stu-id="5d8bf-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="5d8bf-112">Beispiel 3: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mithilfe eines Geheimschlüssels aus der KeyVault-Ressource</span><span class="sxs-lookup"><span data-stu-id="5d8bf-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="5d8bf-113">Beispiel 4: Aktualisieren von Publisher-E-Mail, NotificationSender-E-Mail und Organisationsname</span><span class="sxs-lookup"><span data-stu-id="5d8bf-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="5d8bf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d8bf-114">PARAMETERS</span></span>

### <span data-ttu-id="5d8bf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d8bf-115">-AsJob</span></span>
<span data-ttu-id="5d8bf-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5d8bf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d8bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8bf-117">-DefaultProfile</span></span>
<span data-ttu-id="5d8bf-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8bf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d8bf-119">-InputObject</span></span>
<span data-ttu-id="5d8bf-120">Die ApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-120">The ApiManagement instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8bf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d8bf-121">-PassThru</span></span>
<span data-ttu-id="5d8bf-122">Sendet bei einem erfolgreichen Vorgang aktualisiertes "PsApiManagement" an die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="5d8bf-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5d8bf-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="5d8bf-124">Generieren und zuweisen Sie eine Azure Active Directory-Identität für diesen Server zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="5d8bf-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5d8bf-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="5d8bf-126">Weisen Sie diesem Server Benutzeridentitäten zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault zu.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8bf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d8bf-127">-Confirm</span></span>
<span data-ttu-id="5d8bf-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d8bf-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5d8bf-129">-WhatIf</span></span>
<span data-ttu-id="5d8bf-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d8bf-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d8bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8bf-132">CommonParameters</span></span>
<span data-ttu-id="5d8bf-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d8bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8bf-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d8bf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8bf-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d8bf-135">INPUTS</span></span>

### <span data-ttu-id="5d8bf-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d8bf-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="5d8bf-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d8bf-137">OUTPUTS</span></span>

### <span data-ttu-id="5d8bf-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d8bf-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="5d8bf-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d8bf-139">NOTES</span></span>

## <span data-ttu-id="5d8bf-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d8bf-140">RELATED LINKS</span></span>

[<span data-ttu-id="5d8bf-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d8bf-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="5d8bf-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d8bf-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="5d8bf-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d8bf-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
