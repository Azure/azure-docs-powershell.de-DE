---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179933"
---
# <span data-ttu-id="063c9-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="063c9-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="063c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="063c9-102">SYNOPSIS</span></span>
<span data-ttu-id="063c9-103">Fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="063c9-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="063c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="063c9-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="063c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="063c9-105">DESCRIPTION</span></span>
<span data-ttu-id="063c9-106">Das Cmdlet " **Remove-AzApiManagementApiFromGateway** " fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="063c9-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="063c9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="063c9-107">EXAMPLES</span></span>

### <span data-ttu-id="063c9-108">Beispiel 1: Entfernen einer API von einem Gateway</span><span class="sxs-lookup"><span data-stu-id="063c9-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="063c9-109">Mit diesem Befehl wird die angegebene API von einem Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="063c9-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="063c9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="063c9-110">PARAMETERS</span></span>

### <span data-ttu-id="063c9-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="063c9-111">-ApiId</span></span>
<span data-ttu-id="063c9-112">Bezeichner der vorhandenen APIs, die vom Gateway entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="063c9-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="063c9-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="063c9-113">This parameter is required.</span></span>

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

### <span data-ttu-id="063c9-114">-Context</span><span class="sxs-lookup"><span data-stu-id="063c9-114">-Context</span></span>
<span data-ttu-id="063c9-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="063c9-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="063c9-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="063c9-116">This parameter is required.</span></span>

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

### <span data-ttu-id="063c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063c9-117">-DefaultProfile</span></span>
<span data-ttu-id="063c9-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="063c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="063c9-119">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="063c9-119">-GatewayId</span></span>
<span data-ttu-id="063c9-120">Bezeichner des vorhandenen Gateways, von dem die API entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="063c9-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="063c9-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="063c9-121">This parameter is required.</span></span>

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

### <span data-ttu-id="063c9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="063c9-122">-PassThru</span></span>
<span data-ttu-id="063c9-123">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="063c9-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="063c9-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="063c9-124">This parameter is optional.</span></span>
<span data-ttu-id="063c9-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="063c9-125">Default value is false.</span></span>

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

### <span data-ttu-id="063c9-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="063c9-126">-Confirm</span></span>
<span data-ttu-id="063c9-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="063c9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="063c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="063c9-128">-WhatIf</span></span>
<span data-ttu-id="063c9-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="063c9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="063c9-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="063c9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="063c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063c9-131">CommonParameters</span></span>
<span data-ttu-id="063c9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="063c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063c9-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="063c9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063c9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="063c9-134">INPUTS</span></span>

### <span data-ttu-id="063c9-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="063c9-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="063c9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="063c9-136">System.String</span></span>

### <span data-ttu-id="063c9-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="063c9-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="063c9-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="063c9-138">OUTPUTS</span></span>

### <span data-ttu-id="063c9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="063c9-139">System.Boolean</span></span>

## <span data-ttu-id="063c9-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="063c9-140">NOTES</span></span>

## <span data-ttu-id="063c9-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="063c9-141">RELATED LINKS</span></span>
