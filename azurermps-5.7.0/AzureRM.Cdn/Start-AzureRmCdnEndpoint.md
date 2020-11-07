---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/start-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: cfa0eb8506230fe14b9ddf48bcd7562acf45a590
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662966"
---
# <span data-ttu-id="a8a90-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8a90-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="a8a90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8a90-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a90-103">Startet einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="a8a90-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8a90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8a90-104">SYNTAX</span></span>

### <span data-ttu-id="a8a90-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8a90-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8a90-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8a90-106">ByObjectParameterSet</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8a90-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8a90-107">DESCRIPTION</span></span>
<span data-ttu-id="a8a90-108">Das Cmdlet **Start-AzureRmCdnEndpoint** startet einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="a8a90-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a8a90-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8a90-109">EXAMPLES</span></span>

## <span data-ttu-id="a8a90-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8a90-110">PARAMETERS</span></span>

### <span data-ttu-id="a8a90-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8a90-111">-CdnEndpoint</span></span>
<span data-ttu-id="a8a90-112">Gibt den Endpunkt an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="a8a90-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a90-113">-DefaultProfile</span></span>
<span data-ttu-id="a8a90-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a8a90-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a90-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="a8a90-115">-EndpointName</span></span>
<span data-ttu-id="a8a90-116">Gibt den Namen des Endpunkts an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="a8a90-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a90-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8a90-117">-PassThru</span></span>
<span data-ttu-id="a8a90-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a8a90-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8a90-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a8a90-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a90-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="a8a90-120">-ProfileName</span></span>
<span data-ttu-id="a8a90-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="a8a90-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a90-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a90-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8a90-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="a8a90-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a90-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8a90-124">-Confirm</span></span>
<span data-ttu-id="a8a90-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8a90-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a90-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8a90-126">-WhatIf</span></span>
<span data-ttu-id="a8a90-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8a90-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8a90-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8a90-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a90-129">CommonParameters</span></span>
<span data-ttu-id="a8a90-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a90-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a90-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a90-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8a90-132">INPUTS</span></span>

### <span data-ttu-id="a8a90-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8a90-133">PSEndpoint</span></span>
<span data-ttu-id="a8a90-134">Der Parameter "CdnEndpoint" akzeptiert den Wert vom Typ "PSEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a8a90-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a8a90-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8a90-135">OUTPUTS</span></span>

### <span data-ttu-id="a8a90-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8a90-136">System.Boolean</span></span>

## <span data-ttu-id="a8a90-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8a90-137">NOTES</span></span>

## <span data-ttu-id="a8a90-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8a90-138">RELATED LINKS</span></span>

[<span data-ttu-id="a8a90-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8a90-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="a8a90-140">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8a90-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="a8a90-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8a90-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="a8a90-142">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8a90-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="a8a90-143">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8a90-143">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


