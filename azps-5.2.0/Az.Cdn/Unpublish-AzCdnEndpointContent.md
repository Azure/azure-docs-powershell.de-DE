---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299395"
---
# <span data-ttu-id="74c4a-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="74c4a-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="74c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="74c4a-103">Bereinigen eines CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="74c4a-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="74c4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74c4a-104">SYNTAX</span></span>

### <span data-ttu-id="74c4a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="74c4a-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74c4a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74c4a-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74c4a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="74c4a-108">Das **Cmdlet "Unpublish-AzCdnEndpointContent"** entfernt den Inhalt von einem Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="74c4a-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="74c4a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74c4a-109">EXAMPLES</span></span>

## <span data-ttu-id="74c4a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74c4a-110">PARAMETERS</span></span>

### <span data-ttu-id="74c4a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="74c4a-111">-CdnEndpoint</span></span>
<span data-ttu-id="74c4a-112">Gibt den Endpunkt an, der von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="74c4a-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="74c4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c4a-113">-DefaultProfile</span></span>
<span data-ttu-id="74c4a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="74c4a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74c4a-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="74c4a-115">-EndpointName</span></span>
<span data-ttu-id="74c4a-116">Gibt den Namen des Endpunkts an, der von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="74c4a-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="74c4a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74c4a-117">-PassThru</span></span>
<span data-ttu-id="74c4a-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="74c4a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="74c4a-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="74c4a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74c4a-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="74c4a-120">-ProfileName</span></span>
<span data-ttu-id="74c4a-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="74c4a-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="74c4a-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="74c4a-122">-PurgeContent</span></span>
<span data-ttu-id="74c4a-123">Gibt ein Array relativer Pfade für den Inhalt auf dem Ursprungsserver an, der von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="74c4a-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="74c4a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c4a-124">-ResourceGroupName</span></span>
<span data-ttu-id="74c4a-125">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="74c4a-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="74c4a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74c4a-126">-Confirm</span></span>
<span data-ttu-id="74c4a-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74c4a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c4a-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="74c4a-128">-WhatIf</span></span>
<span data-ttu-id="74c4a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74c4a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c4a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74c4a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c4a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c4a-131">CommonParameters</span></span>
<span data-ttu-id="74c4a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c4a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c4a-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74c4a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c4a-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74c4a-134">INPUTS</span></span>

### <span data-ttu-id="74c4a-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="74c4a-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="74c4a-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74c4a-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="74c4a-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74c4a-137">OUTPUTS</span></span>

### <span data-ttu-id="74c4a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74c4a-138">System.Boolean</span></span>

## <span data-ttu-id="74c4a-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74c4a-139">NOTES</span></span>

## <span data-ttu-id="74c4a-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74c4a-140">RELATED LINKS</span></span>

[<span data-ttu-id="74c4a-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="74c4a-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


