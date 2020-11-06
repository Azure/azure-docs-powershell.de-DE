---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: d48d1913a30fc03ca0ebaf86195b981a6ebe70fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504618"
---
# <span data-ttu-id="a68d2-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a68d2-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="a68d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a68d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a68d2-103">Legt eine benutzerdefinierte Hostname-Konfiguration für einen API-Verwaltungsdienst Proxy oder ein Portal fest.</span><span class="sxs-lookup"><span data-stu-id="a68d2-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a68d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a68d2-104">SYNTAX</span></span>

### <span data-ttu-id="a68d2-105">SetSpecificService (Standard)</span><span class="sxs-lookup"><span data-stu-id="a68d2-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a68d2-106">SetFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="a68d2-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a68d2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a68d2-107">DESCRIPTION</span></span>
<span data-ttu-id="a68d2-108">Das Cmdlet " **Satz-AzureRmApiManagementHostnames** " wendet eine benutzerdefinierte Hostname-Konfiguration für einen API-Verwaltungsdienst Proxy oder ein Portal an.</span><span class="sxs-lookup"><span data-stu-id="a68d2-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="a68d2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a68d2-109">EXAMPLES</span></span>

### <span data-ttu-id="a68d2-110">Beispiel 1: Einrichten der benutzerdefinierten Hostname-Konfiguration für einen Proxy und ein Portal</span><span class="sxs-lookup"><span data-stu-id="a68d2-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="a68d2-111">Mit diesem Befehl wird die benutzerdefinierte Hostname-Konfiguration für Proxy und Portal festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a68d2-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="a68d2-112">Beispiel 2: Konfigurieren eines benutzerdefinierten Hostnamens für einen Proxy und ein Portal</span><span class="sxs-lookup"><span data-stu-id="a68d2-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="a68d2-113">In diesem Beispiel wird ein benutzerdefinierter Hostname für Proxy und Portal konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a68d2-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="a68d2-114">Sie müssen entsprechende Zertifikate importieren und dann die benutzerdefinierten Hostnamen anwenden.</span><span class="sxs-lookup"><span data-stu-id="a68d2-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="a68d2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a68d2-115">PARAMETERS</span></span>

### <span data-ttu-id="a68d2-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a68d2-116">-ApiManagement</span></span>
<span data-ttu-id="a68d2-117">Gibt die **PsApiManagement** -Instanz an, aus der dieses Cmdlet die *PortalHostnameConfiguration* -und *ProxyHostnameConfiguration* -Parameter abruft.</span><span class="sxs-lookup"><span data-stu-id="a68d2-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a68d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68d2-118">-DefaultProfile</span></span>
<span data-ttu-id="a68d2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a68d2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a68d2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a68d2-120">-Name</span></span>
<span data-ttu-id="a68d2-121">Gibt den Namen der API-Verwaltungsinstanz an.</span><span class="sxs-lookup"><span data-stu-id="a68d2-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: String
Parameter Sets: SetSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a68d2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a68d2-122">-PassThru</span></span>
<span data-ttu-id="a68d2-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a68d2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a68d2-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a68d2-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a68d2-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68d2-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="a68d2-126">Gibt die Konfiguration des benutzerdefinierten Portal-Hosts an.</span><span class="sxs-lookup"><span data-stu-id="a68d2-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="a68d2-127">Wenn Sie $NULL an das Cmdlet übergeben, wird der Standardhostname festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a68d2-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a68d2-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68d2-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="a68d2-129">Gibt die benutzerdefinierte Proxy-Hostname-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a68d2-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="a68d2-130">Durch Übergabe $NULL wird der Standardhostname festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a68d2-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a68d2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a68d2-131">-ResourceGroupName</span></span>
<span data-ttu-id="a68d2-132">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungsinstanz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a68d2-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: String
Parameter Sets: SetSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a68d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68d2-133">CommonParameters</span></span>
<span data-ttu-id="a68d2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a68d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68d2-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68d2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68d2-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a68d2-136">INPUTS</span></span>

### <span data-ttu-id="a68d2-137">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a68d2-137">PsApiManagement</span></span>
<span data-ttu-id="a68d2-138">Der Parameter "ApiManagement" akzeptiert den Wert vom Typ "PsApiManagement" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a68d2-138">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="a68d2-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a68d2-139">OUTPUTS</span></span>

### <span data-ttu-id="a68d2-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a68d2-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a68d2-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a68d2-141">NOTES</span></span>

## <span data-ttu-id="a68d2-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a68d2-142">RELATED LINKS</span></span>

[<span data-ttu-id="a68d2-143">Importieren-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a68d2-143">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="a68d2-144">Neu – AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68d2-144">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


