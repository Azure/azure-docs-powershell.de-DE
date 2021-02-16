---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e1afa87d1ab21222987a4eeecf68a3786934ef57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162380"
---
# <span data-ttu-id="dc2cf-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc2cf-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="dc2cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="dc2cf-103">Stoppt den CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="dc2cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc2cf-104">SYNTAX</span></span>

### <span data-ttu-id="dc2cf-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc2cf-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc2cf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc2cf-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc2cf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc2cf-107">DESCRIPTION</span></span>
<span data-ttu-id="dc2cf-108">Das **Cmdlet "Stop-AzCdnEndpoint"** beendet den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="dc2cf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc2cf-109">EXAMPLES</span></span>

## <span data-ttu-id="dc2cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc2cf-110">PARAMETERS</span></span>

### <span data-ttu-id="dc2cf-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc2cf-111">-CdnEndpoint</span></span>
<span data-ttu-id="dc2cf-112">Gibt das Endpunktobjekt an, das dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="dc2cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc2cf-113">-DefaultProfile</span></span>
<span data-ttu-id="dc2cf-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dc2cf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc2cf-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dc2cf-115">-EndpointName</span></span>
<span data-ttu-id="dc2cf-116">Gibt den Namen des Endpunkts an, der von diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="dc2cf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc2cf-117">-PassThru</span></span>
<span data-ttu-id="dc2cf-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dc2cf-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc2cf-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="dc2cf-120">-ProfileName</span></span>
<span data-ttu-id="dc2cf-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="dc2cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc2cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="dc2cf-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="dc2cf-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc2cf-124">-Confirm</span></span>
<span data-ttu-id="dc2cf-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc2cf-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dc2cf-126">-WhatIf</span></span>
<span data-ttu-id="dc2cf-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc2cf-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc2cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc2cf-129">CommonParameters</span></span>
<span data-ttu-id="dc2cf-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc2cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc2cf-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc2cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc2cf-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc2cf-132">INPUTS</span></span>

### <span data-ttu-id="dc2cf-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc2cf-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="dc2cf-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dc2cf-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dc2cf-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc2cf-135">OUTPUTS</span></span>

### <span data-ttu-id="dc2cf-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc2cf-136">System.Boolean</span></span>

## <span data-ttu-id="dc2cf-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dc2cf-137">NOTES</span></span>

## <span data-ttu-id="dc2cf-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dc2cf-138">RELATED LINKS</span></span>

[<span data-ttu-id="dc2cf-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc2cf-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="dc2cf-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc2cf-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="dc2cf-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc2cf-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="dc2cf-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc2cf-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="dc2cf-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc2cf-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


