---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008756"
---
# <span data-ttu-id="4683e-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4683e-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="4683e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4683e-102">SYNOPSIS</span></span>
<span data-ttu-id="4683e-103">Trennt eine API von einem Gateway.</span><span class="sxs-lookup"><span data-stu-id="4683e-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="4683e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4683e-104">SYNTAX</span></span>

### <span data-ttu-id="4683e-105">ContextParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4683e-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4683e-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4683e-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4683e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4683e-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4683e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4683e-108">DESCRIPTION</span></span>
<span data-ttu-id="4683e-109">Das Cmdlet **Remove-AzApiManagementGateway** trennt eine API von einem Gateway.</span><span class="sxs-lookup"><span data-stu-id="4683e-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="4683e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4683e-110">EXAMPLES</span></span>

### <span data-ttu-id="4683e-111">Beispiel 1: Entfernen eines vorhandenen Gateways</span><span class="sxs-lookup"><span data-stu-id="4683e-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="4683e-112">Mit diesem Befehl wird ein vorhandenes Gateway entfernt, und der Benutzer wird nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="4683e-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="4683e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4683e-113">PARAMETERS</span></span>

### <span data-ttu-id="4683e-114">-Context</span><span class="sxs-lookup"><span data-stu-id="4683e-114">-Context</span></span>
<span data-ttu-id="4683e-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4683e-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4683e-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4683e-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4683e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4683e-117">-DefaultProfile</span></span>
<span data-ttu-id="4683e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4683e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4683e-119">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="4683e-119">-GatewayId</span></span>
<span data-ttu-id="4683e-120">Bezeichner des vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="4683e-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="4683e-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4683e-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4683e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4683e-122">-InputObject</span></span>
<span data-ttu-id="4683e-123">Instanz von PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4683e-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="4683e-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4683e-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4683e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4683e-125">-PassThru</span></span>
<span data-ttu-id="4683e-126">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4683e-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4683e-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4683e-127">This parameter is optional.</span></span>
<span data-ttu-id="4683e-128">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="4683e-128">Default value is false.</span></span>

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

### <span data-ttu-id="4683e-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4683e-129">-ResourceId</span></span>
<span data-ttu-id="4683e-130">Arm-Quell Code des Gateways.</span><span class="sxs-lookup"><span data-stu-id="4683e-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="4683e-131">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4683e-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4683e-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4683e-132">-Confirm</span></span>
<span data-ttu-id="4683e-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4683e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4683e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4683e-134">-WhatIf</span></span>
<span data-ttu-id="4683e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4683e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4683e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4683e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4683e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4683e-137">CommonParameters</span></span>
<span data-ttu-id="4683e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4683e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4683e-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4683e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4683e-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4683e-140">INPUTS</span></span>

### <span data-ttu-id="4683e-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4683e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4683e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4683e-142">System.String</span></span>

### <span data-ttu-id="4683e-143">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="4683e-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4683e-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4683e-144">OUTPUTS</span></span>

### <span data-ttu-id="4683e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4683e-145">System.Boolean</span></span>

## <span data-ttu-id="4683e-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="4683e-146">NOTES</span></span>

## <span data-ttu-id="4683e-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4683e-147">RELATED LINKS</span></span>
