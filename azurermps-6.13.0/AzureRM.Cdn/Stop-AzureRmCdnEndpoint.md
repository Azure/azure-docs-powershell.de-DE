---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 20206ebf99d597a2961804bf3062cd4c049f8017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663677"
---
# <span data-ttu-id="be466-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be466-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="be466-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be466-102">SYNOPSIS</span></span>
<span data-ttu-id="be466-103">Beendet den CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="be466-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be466-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be466-104">SYNTAX</span></span>

### <span data-ttu-id="be466-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="be466-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be466-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be466-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be466-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be466-107">DESCRIPTION</span></span>
<span data-ttu-id="be466-108">Das Cmdlet **Stop-AzureRmCdnEndpoint** beendet den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="be466-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="be466-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be466-109">EXAMPLES</span></span>

## <span data-ttu-id="be466-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="be466-110">PARAMETERS</span></span>

### <span data-ttu-id="be466-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be466-111">-CdnEndpoint</span></span>
<span data-ttu-id="be466-112">Gibt das Endpunkt Objekt an, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="be466-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="be466-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be466-113">-DefaultProfile</span></span>
<span data-ttu-id="be466-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="be466-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be466-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="be466-115">-EndpointName</span></span>
<span data-ttu-id="be466-116">Gibt den Namen des Endpunkts an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="be466-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="be466-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be466-117">-PassThru</span></span>
<span data-ttu-id="be466-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="be466-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="be466-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="be466-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="be466-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="be466-120">-ProfileName</span></span>
<span data-ttu-id="be466-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="be466-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="be466-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be466-122">-ResourceGroupName</span></span>
<span data-ttu-id="be466-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="be466-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="be466-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be466-124">-Confirm</span></span>
<span data-ttu-id="be466-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be466-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be466-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be466-126">-WhatIf</span></span>
<span data-ttu-id="be466-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be466-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be466-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be466-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be466-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be466-129">CommonParameters</span></span>
<span data-ttu-id="be466-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be466-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be466-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be466-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be466-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be466-132">INPUTS</span></span>

### <span data-ttu-id="be466-133">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="be466-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="be466-134">Parameter: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be466-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="be466-135">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="be466-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="be466-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be466-136">OUTPUTS</span></span>

### <span data-ttu-id="be466-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be466-137">System.Boolean</span></span>

## <span data-ttu-id="be466-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="be466-138">NOTES</span></span>

## <span data-ttu-id="be466-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be466-139">RELATED LINKS</span></span>

[<span data-ttu-id="be466-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be466-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="be466-141">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be466-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="be466-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be466-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="be466-143">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be466-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="be466-144">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be466-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


