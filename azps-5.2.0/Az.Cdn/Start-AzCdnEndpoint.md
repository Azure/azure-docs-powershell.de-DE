---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303795"
---
# <span data-ttu-id="7cbe7-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cbe7-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="7cbe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cbe7-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbe7-103">Startet einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="7cbe7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cbe7-104">SYNTAX</span></span>

### <span data-ttu-id="7cbe7-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7cbe7-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cbe7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cbe7-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cbe7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cbe7-107">DESCRIPTION</span></span>
<span data-ttu-id="7cbe7-108">Das **Start-AzCdnEndpoint-Cmdlet** startet einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7cbe7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7cbe7-109">EXAMPLES</span></span>

## <span data-ttu-id="7cbe7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cbe7-110">PARAMETERS</span></span>

### <span data-ttu-id="7cbe7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cbe7-111">-CdnEndpoint</span></span>
<span data-ttu-id="7cbe7-112">Gibt den Endpunkt an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbe7-113">-DefaultProfile</span></span>
<span data-ttu-id="7cbe7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7cbe7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cbe7-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7cbe7-115">-EndpointName</span></span>
<span data-ttu-id="7cbe7-116">Gibt den Namen des Endpunkts an, der mit diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cbe7-117">-PassThru</span></span>
<span data-ttu-id="7cbe7-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7cbe7-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7cbe7-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7cbe7-120">-ProfileName</span></span>
<span data-ttu-id="7cbe7-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbe7-122">-ResourceGroupName</span></span>
<span data-ttu-id="7cbe7-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cbe7-124">-Confirm</span></span>
<span data-ttu-id="7cbe7-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe7-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7cbe7-126">-WhatIf</span></span>
<span data-ttu-id="7cbe7-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbe7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbe7-129">CommonParameters</span></span>
<span data-ttu-id="7cbe7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cbe7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbe7-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cbe7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbe7-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7cbe7-132">INPUTS</span></span>

### <span data-ttu-id="7cbe7-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cbe7-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="7cbe7-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7cbe7-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7cbe7-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7cbe7-135">OUTPUTS</span></span>

### <span data-ttu-id="7cbe7-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7cbe7-136">System.Boolean</span></span>

## <span data-ttu-id="7cbe7-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7cbe7-137">NOTES</span></span>

## <span data-ttu-id="7cbe7-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7cbe7-138">RELATED LINKS</span></span>

[<span data-ttu-id="7cbe7-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cbe7-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="7cbe7-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cbe7-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="7cbe7-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cbe7-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="7cbe7-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cbe7-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="7cbe7-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cbe7-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


