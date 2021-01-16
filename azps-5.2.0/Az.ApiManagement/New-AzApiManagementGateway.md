---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293921"
---
# <span data-ttu-id="1bb81-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1bb81-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="1bb81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bb81-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb81-103">Erstellt eine neue Gatewayentität.</span><span class="sxs-lookup"><span data-stu-id="1bb81-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="1bb81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bb81-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb81-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bb81-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb81-106">Das **Cmdlet "New-AzApiManagementGateway"** erstellt eine neue Gatewayentität.</span><span class="sxs-lookup"><span data-stu-id="1bb81-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="1bb81-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1bb81-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb81-108">Beispiel 1: Erstellen eines Gateways</span><span class="sxs-lookup"><span data-stu-id="1bb81-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="1bb81-109">Mit diesem Befehl wird ein Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="1bb81-109">This command creates a gateway.</span></span>

## <span data-ttu-id="1bb81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bb81-110">PARAMETERS</span></span>

### <span data-ttu-id="1bb81-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1bb81-111">-Context</span></span>
<span data-ttu-id="1bb81-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1bb81-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1bb81-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bb81-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1bb81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb81-114">-DefaultProfile</span></span>
<span data-ttu-id="1bb81-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bb81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bb81-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bb81-116">-Description</span></span>
<span data-ttu-id="1bb81-117">Gatewaybeschreibung.</span><span class="sxs-lookup"><span data-stu-id="1bb81-117">Gateway description.</span></span>
<span data-ttu-id="1bb81-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1bb81-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="1bb81-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1bb81-119">-GatewayId</span></span>
<span data-ttu-id="1bb81-120">ID des neuen Gateways.</span><span class="sxs-lookup"><span data-stu-id="1bb81-120">Identifier of new gateway.</span></span>
<span data-ttu-id="1bb81-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1bb81-121">This parameter is optional.</span></span>
<span data-ttu-id="1bb81-122">Wenn keine Angabe angegeben wird, wird ein Code generiert.</span><span class="sxs-lookup"><span data-stu-id="1bb81-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="1bb81-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="1bb81-123">-LocationData</span></span>
<span data-ttu-id="1bb81-124">Gatewayspeicherort.</span><span class="sxs-lookup"><span data-stu-id="1bb81-124">Gateway location.</span></span>
<span data-ttu-id="1bb81-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bb81-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb81-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bb81-126">-Confirm</span></span>
<span data-ttu-id="1bb81-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bb81-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb81-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1bb81-128">-WhatIf</span></span>
<span data-ttu-id="1bb81-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bb81-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bb81-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bb81-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb81-131">CommonParameters</span></span>
<span data-ttu-id="1bb81-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb81-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bb81-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb81-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1bb81-134">INPUTS</span></span>

### <span data-ttu-id="1bb81-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1bb81-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1bb81-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1bb81-136">System.String</span></span>

### <span data-ttu-id="1bb81-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="1bb81-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="1bb81-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1bb81-138">OUTPUTS</span></span>

### <span data-ttu-id="1bb81-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1bb81-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="1bb81-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1bb81-140">NOTES</span></span>

## <span data-ttu-id="1bb81-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1bb81-141">RELATED LINKS</span></span>
