---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178098"
---
# <span data-ttu-id="3dd2d-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="3dd2d-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="3dd2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3dd2d-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd2d-103">Fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="3dd2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dd2d-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd2d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3dd2d-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd2d-106">Das Cmdlet **Add-AzApiManagementApiToGateway** fügt eine Azure API-Verwaltungs-API zu einem Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="3dd2d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3dd2d-107">EXAMPLES</span></span>

### <span data-ttu-id="3dd2d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3dd2d-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="3dd2d-109">Mit diesem Befehl wird die angegebene API dem angegebenen Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="3dd2d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dd2d-110">PARAMETERS</span></span>

### <span data-ttu-id="3dd2d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3dd2d-111">-ApiId</span></span>
<span data-ttu-id="3dd2d-112">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-112">Identifier of existing API.</span></span>
<span data-ttu-id="3dd2d-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3dd2d-114">-Context</span><span class="sxs-lookup"><span data-stu-id="3dd2d-114">-Context</span></span>
<span data-ttu-id="3dd2d-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3dd2d-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd2d-117">-DefaultProfile</span></span>
<span data-ttu-id="3dd2d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd2d-119">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="3dd2d-119">-GatewayId</span></span>
<span data-ttu-id="3dd2d-120">Bezeichner des vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="3dd2d-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="3dd2d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dd2d-122">-PassThru</span></span>
<span data-ttu-id="3dd2d-123">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3dd2d-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-124">This parameter is optional.</span></span>
<span data-ttu-id="3dd2d-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="3dd2d-125">Default value is false.</span></span>

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

### <span data-ttu-id="3dd2d-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="3dd2d-126">-ProvisioningState</span></span>
<span data-ttu-id="3dd2d-127">Bereitstellungsstatus (erstellt).</span><span class="sxs-lookup"><span data-stu-id="3dd2d-127">Provisioning State (Created).</span></span>
<span data-ttu-id="3dd2d-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd2d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3dd2d-129">-Confirm</span></span>
<span data-ttu-id="3dd2d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd2d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd2d-131">-WhatIf</span></span>
<span data-ttu-id="3dd2d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dd2d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd2d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd2d-134">CommonParameters</span></span>
<span data-ttu-id="3dd2d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd2d-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dd2d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd2d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3dd2d-137">INPUTS</span></span>

### <span data-ttu-id="3dd2d-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3dd2d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3dd2d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3dd2d-139">System.String</span></span>

### <span data-ttu-id="3dd2d-140">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGatewayApiProvisioningState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement; Version = 2.0.1.0; Kultur = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3dd2d-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3dd2d-141">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="3dd2d-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3dd2d-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3dd2d-142">OUTPUTS</span></span>

### <span data-ttu-id="3dd2d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3dd2d-143">System.Boolean</span></span>

## <span data-ttu-id="3dd2d-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3dd2d-144">NOTES</span></span>

## <span data-ttu-id="3dd2d-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3dd2d-145">RELATED LINKS</span></span>

[<span data-ttu-id="3dd2d-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="3dd2d-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)