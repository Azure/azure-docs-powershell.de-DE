---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174846"
---
# <span data-ttu-id="174d7-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="174d7-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="174d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="174d7-102">SYNOPSIS</span></span>
<span data-ttu-id="174d7-103">Ruft alle oder eine bestimmte Hostname-Konfiguration für das vorhandene Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="174d7-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="174d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="174d7-104">SYNTAX</span></span>

### <span data-ttu-id="174d7-105">GetByGatewayId (Standard)</span><span class="sxs-lookup"><span data-stu-id="174d7-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="174d7-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="174d7-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="174d7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="174d7-107">DESCRIPTION</span></span>
<span data-ttu-id="174d7-108">Das Cmdlet " **Get-AzApiManagementGatewayHostnameConfiguration** " ruft alle oder eine bestimmte Hostname-Konfiguration für das vorhandene Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="174d7-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="174d7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="174d7-109">EXAMPLES</span></span>

### <span data-ttu-id="174d7-110">Beispiel 1: Abrufen aller Hostnamen-Konfigurationen für das Gateway</span><span class="sxs-lookup"><span data-stu-id="174d7-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="174d7-111">Dieser Befehl ruft alle Hostnamen-Konfigurationen für ein "0123456789"-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="174d7-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="174d7-112">Beispiel 2: Abrufen einer Hostname-Konfiguration für das Gateway</span><span class="sxs-lookup"><span data-stu-id="174d7-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="174d7-113">Dieser Befehl ruft die "123"-Hostname-Konfiguration für ein "0123456789"-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="174d7-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="174d7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="174d7-114">PARAMETERS</span></span>

### <span data-ttu-id="174d7-115">-Context</span><span class="sxs-lookup"><span data-stu-id="174d7-115">-Context</span></span>
<span data-ttu-id="174d7-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="174d7-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="174d7-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="174d7-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="174d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174d7-118">-DefaultProfile</span></span>
<span data-ttu-id="174d7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="174d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="174d7-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="174d7-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="174d7-121">Hostname-Konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="174d7-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="174d7-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="174d7-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="174d7-123">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="174d7-123">-GatewayId</span></span>
<span data-ttu-id="174d7-124">Gateway-ID.</span><span class="sxs-lookup"><span data-stu-id="174d7-124">Gateway identifier.</span></span>
<span data-ttu-id="174d7-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="174d7-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="174d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174d7-126">CommonParameters</span></span>
<span data-ttu-id="174d7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="174d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174d7-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="174d7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174d7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="174d7-129">INPUTS</span></span>

### <span data-ttu-id="174d7-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="174d7-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="174d7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="174d7-131">System.String</span></span>

## <span data-ttu-id="174d7-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="174d7-132">OUTPUTS</span></span>

### <span data-ttu-id="174d7-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="174d7-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="174d7-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="174d7-134">NOTES</span></span>

## <span data-ttu-id="174d7-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="174d7-135">RELATED LINKS</span></span>
