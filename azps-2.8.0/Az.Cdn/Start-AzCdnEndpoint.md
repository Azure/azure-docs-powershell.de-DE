---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 8d174fc74373ab29153be13fc78acd5da639e7d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652264"
---
# <span data-ttu-id="b9129-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9129-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="b9129-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9129-102">SYNOPSIS</span></span>
<span data-ttu-id="b9129-103">Startet einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b9129-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="b9129-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9129-104">SYNTAX</span></span>

### <span data-ttu-id="b9129-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9129-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9129-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9129-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9129-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9129-107">DESCRIPTION</span></span>
<span data-ttu-id="b9129-108">Das Cmdlet **Start-AzCdnEndpoint** startet einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b9129-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b9129-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9129-109">EXAMPLES</span></span>

## <span data-ttu-id="b9129-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9129-110">PARAMETERS</span></span>

### <span data-ttu-id="b9129-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9129-111">-CdnEndpoint</span></span>
<span data-ttu-id="b9129-112">Gibt den Endpunkt an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="b9129-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="b9129-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9129-113">-DefaultProfile</span></span>
<span data-ttu-id="b9129-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b9129-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9129-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="b9129-115">-EndpointName</span></span>
<span data-ttu-id="b9129-116">Gibt den Namen des Endpunkts an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="b9129-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="b9129-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9129-117">-PassThru</span></span>
<span data-ttu-id="b9129-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b9129-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b9129-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b9129-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9129-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="b9129-120">-ProfileName</span></span>
<span data-ttu-id="b9129-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="b9129-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b9129-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9129-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9129-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="b9129-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b9129-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9129-124">-Confirm</span></span>
<span data-ttu-id="b9129-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9129-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9129-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9129-126">-WhatIf</span></span>
<span data-ttu-id="b9129-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9129-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9129-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9129-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9129-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9129-129">CommonParameters</span></span>
<span data-ttu-id="b9129-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9129-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9129-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9129-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9129-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9129-132">INPUTS</span></span>

### <span data-ttu-id="b9129-133">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9129-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b9129-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="b9129-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b9129-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9129-135">OUTPUTS</span></span>

### <span data-ttu-id="b9129-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9129-136">System.Boolean</span></span>

## <span data-ttu-id="b9129-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9129-137">NOTES</span></span>

## <span data-ttu-id="b9129-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9129-138">RELATED LINKS</span></span>

[<span data-ttu-id="b9129-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9129-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="b9129-140">Neu – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9129-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="b9129-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9129-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="b9129-142">Satz-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9129-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b9129-143">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9129-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


