---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 6feb7eb3f20e06c8dfffaa3dd9a1fb2bf3cc4c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498373"
---
# <span data-ttu-id="8ab60-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ab60-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="8ab60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ab60-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab60-103">Entfernt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="8ab60-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ab60-104">SYNTAX</span></span>

### <span data-ttu-id="8ab60-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ab60-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab60-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ab60-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ab60-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ab60-107">DESCRIPTION</span></span>
<span data-ttu-id="8ab60-108">Das Cmdlet **Remove-AzureRmCdnEndpoint** entfernt einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="8ab60-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="8ab60-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ab60-109">EXAMPLES</span></span>

## <span data-ttu-id="8ab60-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ab60-110">PARAMETERS</span></span>

### <span data-ttu-id="8ab60-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ab60-111">-CdnEndpoint</span></span>
<span data-ttu-id="8ab60-112">Gibt den Endpunkt an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ab60-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8ab60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab60-113">-DefaultProfile</span></span>
<span data-ttu-id="8ab60-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8ab60-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ab60-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="8ab60-115">-EndpointName</span></span>
<span data-ttu-id="8ab60-116">Gibt den Namen des Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ab60-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8ab60-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8ab60-117">-Force</span></span>
<span data-ttu-id="8ab60-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8ab60-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab60-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ab60-119">-PassThru</span></span>
<span data-ttu-id="8ab60-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8ab60-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8ab60-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="8ab60-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8ab60-122">-Profilname</span><span class="sxs-lookup"><span data-stu-id="8ab60-122">-ProfileName</span></span>
<span data-ttu-id="8ab60-123">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="8ab60-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8ab60-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab60-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ab60-125">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="8ab60-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8ab60-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ab60-126">-Confirm</span></span>
<span data-ttu-id="8ab60-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ab60-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ab60-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab60-128">-WhatIf</span></span>
<span data-ttu-id="8ab60-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ab60-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ab60-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ab60-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ab60-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab60-131">CommonParameters</span></span>
<span data-ttu-id="8ab60-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab60-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab60-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ab60-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab60-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ab60-134">INPUTS</span></span>

### <span data-ttu-id="8ab60-135">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ab60-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="8ab60-136">Parameter: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ab60-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="8ab60-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8ab60-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ab60-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ab60-138">OUTPUTS</span></span>

### <span data-ttu-id="8ab60-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ab60-139">System.Boolean</span></span>

## <span data-ttu-id="8ab60-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ab60-140">NOTES</span></span>

## <span data-ttu-id="8ab60-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ab60-141">RELATED LINKS</span></span>

[<span data-ttu-id="8ab60-142">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ab60-142">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8ab60-143">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ab60-143">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8ab60-144">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ab60-144">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8ab60-145">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ab60-145">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8ab60-146">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ab60-146">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


