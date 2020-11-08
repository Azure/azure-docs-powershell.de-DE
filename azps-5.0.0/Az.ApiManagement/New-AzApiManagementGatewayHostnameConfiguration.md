---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178079"
---
# <span data-ttu-id="d0a16-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0a16-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="d0a16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0a16-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a16-103">Erstellt einen Hostnamen-configuratin für das vorhandene Gateway.</span><span class="sxs-lookup"><span data-stu-id="d0a16-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="d0a16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0a16-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0a16-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0a16-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a16-106">Das Cmdlet **New-AzApiManagementGatewayHostnameConfiguration** erstellt einen Hostname-configuratin für das vorhandene Gateway.</span><span class="sxs-lookup"><span data-stu-id="d0a16-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="d0a16-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0a16-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a16-108">Beispiel 1: Erstellen einer Hostname-Konfiguration für das vorhandene Gateway</span><span class="sxs-lookup"><span data-stu-id="d0a16-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="d0a16-109">Dieser Befehl erstellt eine "H01"-Hostname-Konfiguration für ein "G01"-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d0a16-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="d0a16-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0a16-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a16-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="d0a16-111">-CertificateResourceId</span></span>
<span data-ttu-id="d0a16-112">Ein Ressourcenbezeichner für die vorhandene Zertifikat-ID. Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0a16-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="d0a16-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d0a16-113">-Context</span></span>
<span data-ttu-id="d0a16-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d0a16-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d0a16-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0a16-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d0a16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a16-116">-DefaultProfile</span></span>
<span data-ttu-id="d0a16-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0a16-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a16-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d0a16-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="d0a16-119">Bezeichner des neuen Gateway-Hostname confiuration.</span><span class="sxs-lookup"><span data-stu-id="d0a16-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="d0a16-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d0a16-120">This parameter is optional.</span></span>
<span data-ttu-id="d0a16-121">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="d0a16-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="d0a16-122">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="d0a16-122">-GatewayId</span></span>
<span data-ttu-id="d0a16-123">Bezeichner des vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="d0a16-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="d0a16-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0a16-124">This parameter is required.</span></span>

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

### <span data-ttu-id="d0a16-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="d0a16-125">-Hostname</span></span>
<span data-ttu-id="d0a16-126">Hostname.</span><span class="sxs-lookup"><span data-stu-id="d0a16-126">Hostname.</span></span>
<span data-ttu-id="d0a16-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0a16-127">This parameter is required.</span></span>

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

### <span data-ttu-id="d0a16-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d0a16-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="d0a16-129">Flag, um NegotiateClientCertificate zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="d0a16-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="d0a16-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d0a16-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0a16-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d0a16-131">-Confirm</span></span>
<span data-ttu-id="d0a16-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0a16-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a16-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a16-133">-WhatIf</span></span>
<span data-ttu-id="d0a16-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0a16-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0a16-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0a16-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a16-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a16-136">CommonParameters</span></span>
<span data-ttu-id="d0a16-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a16-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a16-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0a16-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a16-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0a16-139">INPUTS</span></span>

### <span data-ttu-id="d0a16-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d0a16-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0a16-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d0a16-141">System.String</span></span>

### <span data-ttu-id="d0a16-142">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d0a16-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d0a16-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0a16-143">OUTPUTS</span></span>

### <span data-ttu-id="d0a16-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0a16-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="d0a16-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0a16-145">NOTES</span></span>

## <span data-ttu-id="d0a16-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0a16-146">RELATED LINKS</span></span>
