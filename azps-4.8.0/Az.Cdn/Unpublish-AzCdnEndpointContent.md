---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010024"
---
# <span data-ttu-id="bf258-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="bf258-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="bf258-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf258-102">SYNOPSIS</span></span>
<span data-ttu-id="bf258-103">Bereinigt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="bf258-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="bf258-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf258-104">SYNTAX</span></span>

### <span data-ttu-id="bf258-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf258-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf258-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf258-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf258-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf258-107">DESCRIPTION</span></span>
<span data-ttu-id="bf258-108">Mit dem Cmdlet " **UNPUBLISH-AzCdnEndpointContent** " wird der Inhalt aus einem Azure Content Delivery Network (CDN)-Endpunkt bereinigt.</span><span class="sxs-lookup"><span data-stu-id="bf258-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bf258-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf258-109">EXAMPLES</span></span>

## <span data-ttu-id="bf258-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf258-110">PARAMETERS</span></span>

### <span data-ttu-id="bf258-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf258-111">-CdnEndpoint</span></span>
<span data-ttu-id="bf258-112">Gibt den Endpunkt an, den dieses Cmdlet bereinigt.</span><span class="sxs-lookup"><span data-stu-id="bf258-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="bf258-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf258-113">-DefaultProfile</span></span>
<span data-ttu-id="bf258-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bf258-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf258-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="bf258-115">-EndpointName</span></span>
<span data-ttu-id="bf258-116">Gibt den Namen des Endpunkts an, den dieses Cmdlet bereinigt.</span><span class="sxs-lookup"><span data-stu-id="bf258-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="bf258-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf258-117">-PassThru</span></span>
<span data-ttu-id="bf258-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf258-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf258-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="bf258-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf258-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="bf258-120">-ProfileName</span></span>
<span data-ttu-id="bf258-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="bf258-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="bf258-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="bf258-122">-PurgeContent</span></span>
<span data-ttu-id="bf258-123">Gibt ein Array relativer Pfade für den Inhalt auf dem Ursprungsserver an, den dieses Cmdlet bereinigt.</span><span class="sxs-lookup"><span data-stu-id="bf258-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="bf258-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf258-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf258-125">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="bf258-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="bf258-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf258-126">-Confirm</span></span>
<span data-ttu-id="bf258-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf258-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf258-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf258-128">-WhatIf</span></span>
<span data-ttu-id="bf258-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf258-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf258-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf258-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf258-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf258-131">CommonParameters</span></span>
<span data-ttu-id="bf258-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf258-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf258-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf258-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf258-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf258-134">INPUTS</span></span>

### <span data-ttu-id="bf258-135">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf258-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="bf258-136">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="bf258-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bf258-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf258-137">OUTPUTS</span></span>

### <span data-ttu-id="bf258-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf258-138">System.Boolean</span></span>

## <span data-ttu-id="bf258-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf258-139">NOTES</span></span>

## <span data-ttu-id="bf258-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf258-140">RELATED LINKS</span></span>

[<span data-ttu-id="bf258-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="bf258-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


