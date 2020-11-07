---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: a606bbcb630ab4868e64221b9bcaa8f471327977
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820852"
---
# <span data-ttu-id="b53a1-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53a1-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="b53a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b53a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b53a1-103">Beendet den CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b53a1-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="b53a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b53a1-104">SYNTAX</span></span>

### <span data-ttu-id="b53a1-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b53a1-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b53a1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b53a1-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b53a1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b53a1-107">DESCRIPTION</span></span>
<span data-ttu-id="b53a1-108">Das Cmdlet **Stop-AzCdnEndpoint** beendet den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b53a1-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b53a1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b53a1-109">EXAMPLES</span></span>

## <span data-ttu-id="b53a1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b53a1-110">PARAMETERS</span></span>

### <span data-ttu-id="b53a1-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53a1-111">-CdnEndpoint</span></span>
<span data-ttu-id="b53a1-112">Gibt das Endpunkt Objekt an, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b53a1-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b53a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53a1-113">-DefaultProfile</span></span>
<span data-ttu-id="b53a1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b53a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b53a1-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="b53a1-115">-EndpointName</span></span>
<span data-ttu-id="b53a1-116">Gibt den Namen des Endpunkts an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b53a1-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b53a1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b53a1-117">-PassThru</span></span>
<span data-ttu-id="b53a1-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b53a1-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b53a1-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b53a1-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b53a1-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="b53a1-120">-ProfileName</span></span>
<span data-ttu-id="b53a1-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="b53a1-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b53a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b53a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="b53a1-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="b53a1-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b53a1-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b53a1-124">-Confirm</span></span>
<span data-ttu-id="b53a1-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b53a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b53a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b53a1-126">-WhatIf</span></span>
<span data-ttu-id="b53a1-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b53a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b53a1-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b53a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b53a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53a1-129">CommonParameters</span></span>
<span data-ttu-id="b53a1-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53a1-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b53a1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53a1-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b53a1-132">INPUTS</span></span>

### <span data-ttu-id="b53a1-133">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53a1-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b53a1-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="b53a1-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b53a1-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b53a1-135">OUTPUTS</span></span>

### <span data-ttu-id="b53a1-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b53a1-136">System.Boolean</span></span>

## <span data-ttu-id="b53a1-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="b53a1-137">NOTES</span></span>

## <span data-ttu-id="b53a1-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b53a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="b53a1-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53a1-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="b53a1-140">Neu – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53a1-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="b53a1-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53a1-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="b53a1-142">Satz-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53a1-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b53a1-143">Anfang-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53a1-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


