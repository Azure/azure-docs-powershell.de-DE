---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500906"
---
# <span data-ttu-id="aed7e-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="aed7e-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="aed7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aed7e-102">SYNOPSIS</span></span>
<span data-ttu-id="aed7e-103">Lädt Inhalt zu einem Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="aed7e-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aed7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aed7e-104">SYNTAX</span></span>

### <span data-ttu-id="aed7e-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="aed7e-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed7e-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="aed7e-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aed7e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aed7e-107">DESCRIPTION</span></span>
<span data-ttu-id="aed7e-108">Das Cmdlet " **Publish-AzureRmCdnEndpointContent** " lädt Inhalte von einem Ursprungsserver für den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="aed7e-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="aed7e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aed7e-109">EXAMPLES</span></span>

## <span data-ttu-id="aed7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aed7e-110">PARAMETERS</span></span>

### <span data-ttu-id="aed7e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="aed7e-111">-CdnEndpoint</span></span>
<span data-ttu-id="aed7e-112">Sepcifies Sie den CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="aed7e-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="aed7e-113">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="aed7e-113">-EndpointName</span></span>
<span data-ttu-id="aed7e-114">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="aed7e-114">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="aed7e-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="aed7e-115">-LoadContent</span></span>
<span data-ttu-id="aed7e-116">Gibt ein Array relativer Pfade für den Inhalt auf dem Ursprungsserver an, den dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="aed7e-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="aed7e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aed7e-117">-PassThru</span></span>
<span data-ttu-id="aed7e-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="aed7e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aed7e-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="aed7e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aed7e-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="aed7e-120">-ProfileName</span></span>
<span data-ttu-id="aed7e-121">Gibt den Namen des Profils an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="aed7e-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="aed7e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed7e-122">-ResourceGroupName</span></span>
<span data-ttu-id="aed7e-123">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="aed7e-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="aed7e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed7e-124">-DefaultProfile</span></span>
<span data-ttu-id="aed7e-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aed7e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed7e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed7e-126">CommonParameters</span></span>
<span data-ttu-id="aed7e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed7e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed7e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed7e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed7e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aed7e-129">INPUTS</span></span>

### <span data-ttu-id="aed7e-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="aed7e-130">PSEndpoint</span></span>
<span data-ttu-id="aed7e-131">Der Parameter "CdnEndpoint" akzeptiert den Wert vom Typ "PSEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="aed7e-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="aed7e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aed7e-132">OUTPUTS</span></span>

### <span data-ttu-id="aed7e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aed7e-133">System.Boolean</span></span>

## <span data-ttu-id="aed7e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="aed7e-134">NOTES</span></span>

## <span data-ttu-id="aed7e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aed7e-135">RELATED LINKS</span></span>

[<span data-ttu-id="aed7e-136">Veröffentlichung aufheben – AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="aed7e-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


