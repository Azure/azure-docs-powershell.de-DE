---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663705"
---
# <span data-ttu-id="ba9c2-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba9c2-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="ba9c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9c2-103">Aktualisiert einen Azure API-Verwaltungsdienst</span><span class="sxs-lookup"><span data-stu-id="ba9c2-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba9c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba9c2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba9c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba9c2-105">DESCRIPTION</span></span>

<span data-ttu-id="ba9c2-106">Das Cmdlet " **Satz-AzureRmApiManagement** " aktualisiert einen Azure API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="ba9c2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba9c2-107">EXAMPLES</span></span>

### <span data-ttu-id="ba9c2-108">Beispiel 1 Abrufen eines API-Verwaltungsdiensts und Skalieren auf Premium und Hinzufügen eines Bereichs</span><span class="sxs-lookup"><span data-stu-id="ba9c2-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="ba9c2-109">In diesem Beispiel wird eine API-Verwaltungsinstanz abgerufen, auf fünf Premium-Einheiten skaliert und dann dem Premium-Bereich weitere drei Einheiten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="ba9c2-110">Beispiel 2: Update Bereitstellung (externe VNET)</span><span class="sxs-lookup"><span data-stu-id="ba9c2-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="ba9c2-111">Mit diesem Befehl wird eine vorhandene API-Verwaltungs Bereitstellung aktualisiert und eine Verknüpfung zu einem externen *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="ba9c2-112">Beispiel 3: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mit einem Schlüssel aus der keyvault-Ressource</span><span class="sxs-lookup"><span data-stu-id="ba9c2-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="ba9c2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba9c2-113">PARAMETERS</span></span>

### <span data-ttu-id="ba9c2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba9c2-114">-AsJob</span></span>
<span data-ttu-id="ba9c2-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ba9c2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba9c2-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ba9c2-116">-AssignIdentity</span></span>
<span data-ttu-id="ba9c2-117">Sie können eine Azure Active Directory-Identität für diesen Server für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault generieren und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ba9c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9c2-118">-DefaultProfile</span></span>
<span data-ttu-id="ba9c2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba9c2-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba9c2-120">-InputObject</span></span>
<span data-ttu-id="ba9c2-121">Die ApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-121">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="ba9c2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba9c2-122">-PassThru</span></span>
<span data-ttu-id="ba9c2-123">Sendet aktualisierte PsApiManagement an Pipeline, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="ba9c2-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba9c2-124">-Confirm</span></span>
<span data-ttu-id="ba9c2-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba9c2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba9c2-126">-WhatIf</span></span>
<span data-ttu-id="ba9c2-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba9c2-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba9c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9c2-129">CommonParameters</span></span>
<span data-ttu-id="ba9c2-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba9c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9c2-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba9c2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9c2-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba9c2-132">INPUTS</span></span>

### <span data-ttu-id="ba9c2-133">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba9c2-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="ba9c2-134">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba9c2-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ba9c2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba9c2-135">OUTPUTS</span></span>

### <span data-ttu-id="ba9c2-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba9c2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ba9c2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba9c2-137">NOTES</span></span>

## <span data-ttu-id="ba9c2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba9c2-138">RELATED LINKS</span></span>

[<span data-ttu-id="ba9c2-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba9c2-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="ba9c2-140">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba9c2-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ba9c2-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba9c2-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
