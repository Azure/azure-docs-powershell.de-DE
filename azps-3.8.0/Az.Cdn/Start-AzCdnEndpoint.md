---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003033"
---
# <span data-ttu-id="002e6-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="002e6-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="002e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="002e6-102">SYNOPSIS</span></span>
<span data-ttu-id="002e6-103">Startet einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="002e6-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="002e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="002e6-104">SYNTAX</span></span>

### <span data-ttu-id="002e6-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="002e6-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="002e6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="002e6-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="002e6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="002e6-107">DESCRIPTION</span></span>
<span data-ttu-id="002e6-108">Das Cmdlet **Start-AzCdnEndpoint** startet einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="002e6-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="002e6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="002e6-109">EXAMPLES</span></span>

## <span data-ttu-id="002e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="002e6-110">PARAMETERS</span></span>

### <span data-ttu-id="002e6-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="002e6-111">-CdnEndpoint</span></span>
<span data-ttu-id="002e6-112">Gibt den Endpunkt an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="002e6-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="002e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002e6-113">-DefaultProfile</span></span>
<span data-ttu-id="002e6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="002e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="002e6-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="002e6-115">-EndpointName</span></span>
<span data-ttu-id="002e6-116">Gibt den Namen des Endpunkts an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="002e6-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="002e6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="002e6-117">-PassThru</span></span>
<span data-ttu-id="002e6-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="002e6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="002e6-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="002e6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="002e6-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="002e6-120">-ProfileName</span></span>
<span data-ttu-id="002e6-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="002e6-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="002e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="002e6-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="002e6-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="002e6-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="002e6-124">-Confirm</span></span>
<span data-ttu-id="002e6-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="002e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="002e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="002e6-126">-WhatIf</span></span>
<span data-ttu-id="002e6-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="002e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="002e6-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="002e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="002e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002e6-129">CommonParameters</span></span>
<span data-ttu-id="002e6-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="002e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002e6-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="002e6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002e6-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="002e6-132">INPUTS</span></span>

### <span data-ttu-id="002e6-133">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="002e6-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="002e6-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="002e6-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="002e6-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="002e6-135">OUTPUTS</span></span>

### <span data-ttu-id="002e6-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="002e6-136">System.Boolean</span></span>

## <span data-ttu-id="002e6-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="002e6-137">NOTES</span></span>

## <span data-ttu-id="002e6-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="002e6-138">RELATED LINKS</span></span>

[<span data-ttu-id="002e6-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="002e6-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="002e6-140">Neu – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="002e6-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="002e6-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="002e6-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="002e6-142">Satz-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="002e6-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="002e6-143">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="002e6-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


