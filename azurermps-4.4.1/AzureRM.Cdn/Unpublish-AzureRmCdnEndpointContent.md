---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a774aec8114883d3ba2a5edf189f115f99d3eb4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497837"
---
# <span data-ttu-id="d7db6-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="d7db6-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="d7db6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7db6-102">SYNOPSIS</span></span>
<span data-ttu-id="d7db6-103">Bereinigt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="d7db6-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7db6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7db6-104">SYNTAX</span></span>

### <span data-ttu-id="d7db6-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7db6-105">Parameter Set for fields parameters (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7db6-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="d7db6-106">Parameter Set for object parameters</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7db6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7db6-107">DESCRIPTION</span></span>
<span data-ttu-id="d7db6-108">Mit dem Cmdlet " **UNPUBLISH-AzureRmCdnEndpointContent** " wird der Inhalt aus einem Azure Content Delivery Network (CDN)-Endpunkt bereinigt.</span><span class="sxs-lookup"><span data-stu-id="d7db6-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d7db6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7db6-109">EXAMPLES</span></span>

## <span data-ttu-id="d7db6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7db6-110">PARAMETERS</span></span>

### <span data-ttu-id="d7db6-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7db6-111">-CdnEndpoint</span></span>
<span data-ttu-id="d7db6-112">Gibt den Endpunkt an, den dieses Cmdlet bereinigt.</span><span class="sxs-lookup"><span data-stu-id="d7db6-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7db6-113">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="d7db6-113">-EndpointName</span></span>
<span data-ttu-id="d7db6-114">Gibt den Namen des Endpunkts an, den dieses Cmdlet bereinigt.</span><span class="sxs-lookup"><span data-stu-id="d7db6-114">Specifies name of the endpoint that this cmdlet purges.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7db6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7db6-115">-PassThru</span></span>
<span data-ttu-id="d7db6-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d7db6-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7db6-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d7db6-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7db6-118">-Profilname</span><span class="sxs-lookup"><span data-stu-id="d7db6-118">-ProfileName</span></span>
<span data-ttu-id="d7db6-119">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="d7db6-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7db6-120">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="d7db6-120">-PurgeContent</span></span>
<span data-ttu-id="d7db6-121">Gibt ein Array relativer Pfade für den Inhalt auf dem Ursprungsserver an, den dieses Cmdlet bereinigt.</span><span class="sxs-lookup"><span data-stu-id="d7db6-121">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="d7db6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7db6-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7db6-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="d7db6-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7db6-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7db6-124">-Confirm</span></span>
<span data-ttu-id="d7db6-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7db6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7db6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7db6-126">-WhatIf</span></span>
<span data-ttu-id="d7db6-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7db6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7db6-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7db6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7db6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7db6-129">-DefaultProfile</span></span>
<span data-ttu-id="d7db6-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7db6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7db6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7db6-131">CommonParameters</span></span>
<span data-ttu-id="d7db6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7db6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7db6-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7db6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7db6-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7db6-134">INPUTS</span></span>

### <span data-ttu-id="d7db6-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7db6-135">PSEndpoint</span></span>
<span data-ttu-id="d7db6-136">Der Parameter "CdnEndpoint" akzeptiert den Wert vom Typ "PSEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7db6-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="d7db6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7db6-137">OUTPUTS</span></span>

### <span data-ttu-id="d7db6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7db6-138">System.Boolean</span></span>

## <span data-ttu-id="d7db6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7db6-139">NOTES</span></span>

## <span data-ttu-id="d7db6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7db6-140">RELATED LINKS</span></span>

[<span data-ttu-id="d7db6-141">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="d7db6-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


