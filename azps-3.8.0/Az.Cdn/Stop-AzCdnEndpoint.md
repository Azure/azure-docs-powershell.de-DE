---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e1afa87d1ab21222987a4eeecf68a3786934ef57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003032"
---
# <span data-ttu-id="2633f-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2633f-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="2633f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2633f-102">SYNOPSIS</span></span>
<span data-ttu-id="2633f-103">Beendet den CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="2633f-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="2633f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2633f-104">SYNTAX</span></span>

### <span data-ttu-id="2633f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2633f-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2633f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2633f-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2633f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2633f-107">DESCRIPTION</span></span>
<span data-ttu-id="2633f-108">Das Cmdlet **Stop-AzCdnEndpoint** beendet den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="2633f-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2633f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2633f-109">EXAMPLES</span></span>

## <span data-ttu-id="2633f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2633f-110">PARAMETERS</span></span>

### <span data-ttu-id="2633f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2633f-111">-CdnEndpoint</span></span>
<span data-ttu-id="2633f-112">Gibt das Endpunkt Objekt an, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="2633f-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2633f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2633f-113">-DefaultProfile</span></span>
<span data-ttu-id="2633f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2633f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2633f-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="2633f-115">-EndpointName</span></span>
<span data-ttu-id="2633f-116">Gibt den Namen des Endpunkts an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="2633f-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2633f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2633f-117">-PassThru</span></span>
<span data-ttu-id="2633f-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2633f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2633f-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2633f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2633f-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="2633f-120">-ProfileName</span></span>
<span data-ttu-id="2633f-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="2633f-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2633f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2633f-122">-ResourceGroupName</span></span>
<span data-ttu-id="2633f-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="2633f-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2633f-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2633f-124">-Confirm</span></span>
<span data-ttu-id="2633f-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2633f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2633f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2633f-126">-WhatIf</span></span>
<span data-ttu-id="2633f-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2633f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2633f-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2633f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2633f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2633f-129">CommonParameters</span></span>
<span data-ttu-id="2633f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2633f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2633f-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2633f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2633f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2633f-132">INPUTS</span></span>

### <span data-ttu-id="2633f-133">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2633f-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="2633f-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2633f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2633f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2633f-135">OUTPUTS</span></span>

### <span data-ttu-id="2633f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2633f-136">System.Boolean</span></span>

## <span data-ttu-id="2633f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2633f-137">NOTES</span></span>

## <span data-ttu-id="2633f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2633f-138">RELATED LINKS</span></span>

[<span data-ttu-id="2633f-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2633f-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="2633f-140">Neu – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2633f-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="2633f-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2633f-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="2633f-142">Satz-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2633f-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="2633f-143">Anfang-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2633f-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


