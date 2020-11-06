---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 49afefc7b80b5475735f61cb0511366b7f27a466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93506009"
---
# <span data-ttu-id="0e321-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e321-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="0e321-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e321-102">SYNOPSIS</span></span>
<span data-ttu-id="0e321-103">Entfernt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="0e321-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e321-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e321-104">SYNTAX</span></span>

### <span data-ttu-id="0e321-105">Parametersatz für fields-Parameter</span><span class="sxs-lookup"><span data-stu-id="0e321-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e321-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="0e321-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e321-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e321-107">DESCRIPTION</span></span>
<span data-ttu-id="0e321-108">Das Cmdlet **Remove-AzureRmCdnEndpoint** entfernt einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="0e321-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0e321-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e321-109">EXAMPLES</span></span>

## <span data-ttu-id="0e321-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e321-110">PARAMETERS</span></span>

### <span data-ttu-id="0e321-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e321-111">-CdnEndpoint</span></span>
<span data-ttu-id="0e321-112">Gibt den Endpunkt an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="0e321-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0e321-113">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="0e321-113">-EndpointName</span></span>
<span data-ttu-id="0e321-114">Gibt den Namen des Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="0e321-114">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0e321-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0e321-115">-Force</span></span>
<span data-ttu-id="0e321-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0e321-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0e321-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e321-117">-PassThru</span></span>
<span data-ttu-id="0e321-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0e321-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0e321-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0e321-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0e321-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="0e321-120">-ProfileName</span></span>
<span data-ttu-id="0e321-121">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="0e321-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0e321-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e321-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e321-123">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="0e321-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0e321-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e321-124">-Confirm</span></span>
<span data-ttu-id="0e321-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e321-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e321-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e321-126">-WhatIf</span></span>
<span data-ttu-id="0e321-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e321-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e321-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e321-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e321-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e321-129">-DefaultProfile</span></span>
<span data-ttu-id="0e321-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e321-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e321-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e321-131">CommonParameters</span></span>
<span data-ttu-id="0e321-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e321-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e321-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e321-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e321-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e321-134">INPUTS</span></span>

### <span data-ttu-id="0e321-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e321-135">PSEndpoint</span></span>
<span data-ttu-id="0e321-136">Der Parameter "CdnEndpoint" akzeptiert den Wert vom Typ "PSEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0e321-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="0e321-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e321-137">OUTPUTS</span></span>

### <span data-ttu-id="0e321-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e321-138">System.Boolean</span></span>

## <span data-ttu-id="0e321-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e321-139">NOTES</span></span>

## <span data-ttu-id="0e321-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e321-140">RELATED LINKS</span></span>

[<span data-ttu-id="0e321-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e321-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0e321-142">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e321-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0e321-143">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e321-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0e321-144">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e321-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0e321-145">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e321-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


