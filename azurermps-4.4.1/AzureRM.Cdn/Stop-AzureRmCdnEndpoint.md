---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 83229b9251e7cbbbe4bd17d73004b9bc64800511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497857"
---
# <span data-ttu-id="0287f-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0287f-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="0287f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0287f-102">SYNOPSIS</span></span>
<span data-ttu-id="0287f-103">Beendet den CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="0287f-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0287f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0287f-104">SYNTAX</span></span>

### <span data-ttu-id="0287f-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="0287f-105">Parameter Set for fields parameters (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0287f-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="0287f-106">Parameter Set for object parameters</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0287f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0287f-107">DESCRIPTION</span></span>
<span data-ttu-id="0287f-108">Das Cmdlet **Stop-AzureRmCdnEndpoint** beendet den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="0287f-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0287f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0287f-109">EXAMPLES</span></span>

## <span data-ttu-id="0287f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0287f-110">PARAMETERS</span></span>

### <span data-ttu-id="0287f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0287f-111">-CdnEndpoint</span></span>
<span data-ttu-id="0287f-112">Gibt das Endpunkt Objekt an, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0287f-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0287f-113">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="0287f-113">-EndpointName</span></span>
<span data-ttu-id="0287f-114">Gibt den Namen des Endpunkts an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0287f-114">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0287f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0287f-115">-PassThru</span></span>
<span data-ttu-id="0287f-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0287f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0287f-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0287f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0287f-118">-Profilname</span><span class="sxs-lookup"><span data-stu-id="0287f-118">-ProfileName</span></span>
<span data-ttu-id="0287f-119">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="0287f-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0287f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0287f-120">-ResourceGroupName</span></span>
<span data-ttu-id="0287f-121">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="0287f-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0287f-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0287f-122">-Confirm</span></span>
<span data-ttu-id="0287f-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0287f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0287f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0287f-124">-WhatIf</span></span>
<span data-ttu-id="0287f-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0287f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0287f-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0287f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0287f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0287f-127">-DefaultProfile</span></span>
<span data-ttu-id="0287f-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0287f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0287f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0287f-129">CommonParameters</span></span>
<span data-ttu-id="0287f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0287f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0287f-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0287f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0287f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0287f-132">INPUTS</span></span>

### <span data-ttu-id="0287f-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0287f-133">PSEndpoint</span></span>
<span data-ttu-id="0287f-134">Der Parameter "CdnEndpoint" akzeptiert den Wert vom Typ "PSEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0287f-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="0287f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0287f-135">OUTPUTS</span></span>

### <span data-ttu-id="0287f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0287f-136">System.Boolean</span></span>

## <span data-ttu-id="0287f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0287f-137">NOTES</span></span>

## <span data-ttu-id="0287f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0287f-138">RELATED LINKS</span></span>

[<span data-ttu-id="0287f-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0287f-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0287f-140">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0287f-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0287f-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0287f-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0287f-142">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0287f-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0287f-143">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0287f-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


