---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 73d5c679e1079f99cc19f2af6c22e2d5b5a491fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943112"
---
# <span data-ttu-id="e48ba-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e48ba-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="e48ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e48ba-102">SYNOPSIS</span></span>
<span data-ttu-id="e48ba-103">Lädt Inhalt an einen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e48ba-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="e48ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e48ba-104">SYNTAX</span></span>

### <span data-ttu-id="e48ba-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e48ba-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e48ba-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e48ba-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e48ba-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e48ba-107">DESCRIPTION</span></span>
<span data-ttu-id="e48ba-108">Das **Cmdlet Publish-AzCdnEndpointContent** lädt Inhalte von einem Ursprungsserver für den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e48ba-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e48ba-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e48ba-109">EXAMPLES</span></span>

## <span data-ttu-id="e48ba-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e48ba-110">PARAMETERS</span></span>

### <span data-ttu-id="e48ba-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e48ba-111">-CdnEndpoint</span></span>
<span data-ttu-id="e48ba-112">Gibt den CDN-Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="e48ba-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="e48ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48ba-113">-DefaultProfile</span></span>
<span data-ttu-id="e48ba-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e48ba-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e48ba-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e48ba-115">-EndpointName</span></span>
<span data-ttu-id="e48ba-116">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="e48ba-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="e48ba-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="e48ba-117">-LoadContent</span></span>
<span data-ttu-id="e48ba-118">Gibt ein Array relativer Pfade für den Inhalt auf dem Ursprungsserver an, den dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="e48ba-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48ba-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e48ba-119">-PassThru</span></span>
<span data-ttu-id="e48ba-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e48ba-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e48ba-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e48ba-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e48ba-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e48ba-122">-ProfileName</span></span>
<span data-ttu-id="e48ba-123">Gibt den Namen des Profils an, dem der Ursprungsserver angehört.</span><span class="sxs-lookup"><span data-stu-id="e48ba-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e48ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e48ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="e48ba-125">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="e48ba-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e48ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48ba-126">CommonParameters</span></span>
<span data-ttu-id="e48ba-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e48ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48ba-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e48ba-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48ba-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e48ba-129">INPUTS</span></span>

### <span data-ttu-id="e48ba-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e48ba-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="e48ba-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e48ba-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e48ba-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e48ba-132">OUTPUTS</span></span>

### <span data-ttu-id="e48ba-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e48ba-133">System.Boolean</span></span>

## <span data-ttu-id="e48ba-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e48ba-134">NOTES</span></span>

## <span data-ttu-id="e48ba-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e48ba-135">RELATED LINKS</span></span>

[<span data-ttu-id="e48ba-136">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e48ba-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


