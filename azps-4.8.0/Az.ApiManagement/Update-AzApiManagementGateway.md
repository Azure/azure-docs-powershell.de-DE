---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008190"
---
# <span data-ttu-id="a58d8-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a58d8-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="a58d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a58d8-102">SYNOPSIS</span></span>
<span data-ttu-id="a58d8-103">Konfiguriert ein API-Verwaltungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="a58d8-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="a58d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a58d8-104">SYNTAX</span></span>

### <span data-ttu-id="a58d8-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a58d8-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58d8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a58d8-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58d8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a58d8-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a58d8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a58d8-108">DESCRIPTION</span></span>
<span data-ttu-id="a58d8-109">Das Cmdlet **Update-AzApiManagementGateway** konfiguriert ein API-Verwaltungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="a58d8-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="a58d8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a58d8-110">EXAMPLES</span></span>

### <span data-ttu-id="a58d8-111">Beispiel 1: Konfigurieren einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a58d8-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="a58d8-112">Mit diesem Befehl wird ein Gateway konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a58d8-112">This command configures a gateway.</span></span>

## <span data-ttu-id="a58d8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a58d8-113">PARAMETERS</span></span>

### <span data-ttu-id="a58d8-114">-Context</span><span class="sxs-lookup"><span data-stu-id="a58d8-114">-Context</span></span>
<span data-ttu-id="a58d8-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a58d8-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a58d8-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a58d8-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a58d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58d8-117">-DefaultProfile</span></span>
<span data-ttu-id="a58d8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a58d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a58d8-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a58d8-119">-Description</span></span>
<span data-ttu-id="a58d8-120">Gateway-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="a58d8-120">Gateway description.</span></span>
<span data-ttu-id="a58d8-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a58d8-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="a58d8-122">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="a58d8-122">-GatewayId</span></span>
<span data-ttu-id="a58d8-123">Bezeichner des vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="a58d8-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="a58d8-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a58d8-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58d8-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a58d8-125">-InputObject</span></span>
<span data-ttu-id="a58d8-126">Instanz von PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a58d8-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="a58d8-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a58d8-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a58d8-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="a58d8-128">-LocationData</span></span>
<span data-ttu-id="a58d8-129">Gateway-Standort.</span><span class="sxs-lookup"><span data-stu-id="a58d8-129">Gateway location.</span></span>
<span data-ttu-id="a58d8-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a58d8-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58d8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a58d8-131">-PassThru</span></span>
<span data-ttu-id="a58d8-132">Wenn angegeben, wird Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGateway-Typs, der das geänderte Gateway darstellt.</span><span class="sxs-lookup"><span data-stu-id="a58d8-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="a58d8-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a58d8-133">-ResourceId</span></span>
<span data-ttu-id="a58d8-134">Arm-Quell Code des Gateways.</span><span class="sxs-lookup"><span data-stu-id="a58d8-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="a58d8-135">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a58d8-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58d8-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a58d8-136">-Confirm</span></span>
<span data-ttu-id="a58d8-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a58d8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a58d8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a58d8-138">-WhatIf</span></span>
<span data-ttu-id="a58d8-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a58d8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a58d8-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a58d8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a58d8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58d8-141">CommonParameters</span></span>
<span data-ttu-id="a58d8-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a58d8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58d8-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a58d8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58d8-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a58d8-144">INPUTS</span></span>

### <span data-ttu-id="a58d8-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a58d8-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a58d8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a58d8-146">System.String</span></span>

### <span data-ttu-id="a58d8-147">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="a58d8-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="a58d8-148">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a58d8-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a58d8-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a58d8-149">OUTPUTS</span></span>

### <span data-ttu-id="a58d8-150">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a58d8-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="a58d8-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="a58d8-151">NOTES</span></span>

## <span data-ttu-id="a58d8-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a58d8-152">RELATED LINKS</span></span>
