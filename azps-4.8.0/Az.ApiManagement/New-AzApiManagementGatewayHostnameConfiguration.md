---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165364"
---
# <span data-ttu-id="34d0f-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="34d0f-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="34d0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="34d0f-103">Erstellt einen Hostnamen-configuratin für das vorhandene Gateway.</span><span class="sxs-lookup"><span data-stu-id="34d0f-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="34d0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34d0f-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34d0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="34d0f-106">Das Cmdlet **New-AzApiManagementGatewayHostnameConfiguration** erstellt einen Hostname-configuratin für das vorhandene Gateway.</span><span class="sxs-lookup"><span data-stu-id="34d0f-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="34d0f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="34d0f-108">Beispiel 1: Erstellen einer Hostname-Konfiguration für das vorhandene Gateway</span><span class="sxs-lookup"><span data-stu-id="34d0f-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="34d0f-109">Dieser Befehl erstellt eine "H01"-Hostname-Konfiguration für ein "G01"-Gateway.</span><span class="sxs-lookup"><span data-stu-id="34d0f-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="34d0f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34d0f-110">PARAMETERS</span></span>

### <span data-ttu-id="34d0f-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="34d0f-111">-CertificateResourceId</span></span>
<span data-ttu-id="34d0f-112">Ein Ressourcenbezeichner für die vorhandene Zertifikat-ID. Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="34d0f-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="34d0f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="34d0f-113">-Context</span></span>
<span data-ttu-id="34d0f-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="34d0f-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="34d0f-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="34d0f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="34d0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d0f-116">-DefaultProfile</span></span>
<span data-ttu-id="34d0f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34d0f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d0f-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="34d0f-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="34d0f-119">Bezeichner des neuen Gateway-Hostname confiuration.</span><span class="sxs-lookup"><span data-stu-id="34d0f-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="34d0f-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="34d0f-120">This parameter is optional.</span></span>
<span data-ttu-id="34d0f-121">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="34d0f-121">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34d0f-122">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="34d0f-122">-GatewayId</span></span>
<span data-ttu-id="34d0f-123">Bezeichner des vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="34d0f-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="34d0f-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="34d0f-124">This parameter is required.</span></span>

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

### <span data-ttu-id="34d0f-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="34d0f-125">-Hostname</span></span>
<span data-ttu-id="34d0f-126">Hostname.</span><span class="sxs-lookup"><span data-stu-id="34d0f-126">Hostname.</span></span>
<span data-ttu-id="34d0f-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="34d0f-127">This parameter is required.</span></span>

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

### <span data-ttu-id="34d0f-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="34d0f-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="34d0f-129">Flag, um NegotiateClientCertificate zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="34d0f-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="34d0f-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="34d0f-130">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34d0f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34d0f-131">-Confirm</span></span>
<span data-ttu-id="34d0f-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34d0f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34d0f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d0f-133">-WhatIf</span></span>
<span data-ttu-id="34d0f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34d0f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34d0f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34d0f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34d0f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d0f-136">CommonParameters</span></span>
<span data-ttu-id="34d0f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d0f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d0f-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34d0f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d0f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34d0f-139">INPUTS</span></span>

### <span data-ttu-id="34d0f-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="34d0f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="34d0f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="34d0f-141">System.String</span></span>

### <span data-ttu-id="34d0f-142">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="34d0f-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="34d0f-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34d0f-143">OUTPUTS</span></span>

### <span data-ttu-id="34d0f-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="34d0f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="34d0f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="34d0f-145">NOTES</span></span>

## <span data-ttu-id="34d0f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34d0f-146">RELATED LINKS</span></span>
