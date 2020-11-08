---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009347"
---
# <span data-ttu-id="fc65b-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="fc65b-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="fc65b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc65b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc65b-103">Lädt Inhalt zu einem Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="fc65b-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="fc65b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc65b-104">SYNTAX</span></span>

### <span data-ttu-id="fc65b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc65b-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc65b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc65b-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc65b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc65b-107">DESCRIPTION</span></span>
<span data-ttu-id="fc65b-108">Das Cmdlet " **Publish-AzCdnEndpointContent** " lädt Inhalte von einem Ursprungsserver für den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="fc65b-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="fc65b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc65b-109">EXAMPLES</span></span>

## <span data-ttu-id="fc65b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc65b-110">PARAMETERS</span></span>

### <span data-ttu-id="fc65b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc65b-111">-CdnEndpoint</span></span>
<span data-ttu-id="fc65b-112">Gibt den CDN-Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="fc65b-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="fc65b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc65b-113">-DefaultProfile</span></span>
<span data-ttu-id="fc65b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fc65b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc65b-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="fc65b-115">-EndpointName</span></span>
<span data-ttu-id="fc65b-116">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="fc65b-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="fc65b-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="fc65b-117">-LoadContent</span></span>
<span data-ttu-id="fc65b-118">Gibt ein Array relativer Pfade für den Inhalt auf dem Ursprungsserver an, den dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="fc65b-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="fc65b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc65b-119">-PassThru</span></span>
<span data-ttu-id="fc65b-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fc65b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc65b-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="fc65b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc65b-122">-Profilname</span><span class="sxs-lookup"><span data-stu-id="fc65b-122">-ProfileName</span></span>
<span data-ttu-id="fc65b-123">Gibt den Namen des Profils an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="fc65b-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="fc65b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc65b-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc65b-125">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="fc65b-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="fc65b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc65b-126">CommonParameters</span></span>
<span data-ttu-id="fc65b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc65b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc65b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc65b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc65b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc65b-129">INPUTS</span></span>

### <span data-ttu-id="fc65b-130">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc65b-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="fc65b-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="fc65b-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc65b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc65b-132">OUTPUTS</span></span>

### <span data-ttu-id="fc65b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc65b-133">System.Boolean</span></span>

## <span data-ttu-id="fc65b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc65b-134">NOTES</span></span>

## <span data-ttu-id="fc65b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc65b-135">RELATED LINKS</span></span>

[<span data-ttu-id="fc65b-136">Veröffentlichung aufheben – AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="fc65b-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


