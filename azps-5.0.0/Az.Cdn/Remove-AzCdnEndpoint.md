---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179303"
---
# <span data-ttu-id="60069-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60069-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="60069-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60069-102">SYNOPSIS</span></span>
<span data-ttu-id="60069-103">Entfernt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="60069-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="60069-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60069-104">SYNTAX</span></span>

### <span data-ttu-id="60069-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="60069-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60069-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60069-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60069-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60069-107">DESCRIPTION</span></span>
<span data-ttu-id="60069-108">Das Cmdlet **Remove-AzCdnEndpoint** entfernt einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="60069-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="60069-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60069-109">EXAMPLES</span></span>

## <span data-ttu-id="60069-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="60069-110">PARAMETERS</span></span>

### <span data-ttu-id="60069-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60069-111">-CdnEndpoint</span></span>
<span data-ttu-id="60069-112">Gibt den Endpunkt an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="60069-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="60069-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60069-113">-DefaultProfile</span></span>
<span data-ttu-id="60069-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="60069-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60069-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="60069-115">-EndpointName</span></span>
<span data-ttu-id="60069-116">Gibt den Namen des Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="60069-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="60069-117">-Force</span><span class="sxs-lookup"><span data-stu-id="60069-117">-Force</span></span>
<span data-ttu-id="60069-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="60069-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="60069-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60069-119">-PassThru</span></span>
<span data-ttu-id="60069-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="60069-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="60069-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="60069-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="60069-122">-Profilname</span><span class="sxs-lookup"><span data-stu-id="60069-122">-ProfileName</span></span>
<span data-ttu-id="60069-123">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="60069-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="60069-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60069-124">-ResourceGroupName</span></span>
<span data-ttu-id="60069-125">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="60069-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="60069-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60069-126">-Confirm</span></span>
<span data-ttu-id="60069-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60069-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60069-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60069-128">-WhatIf</span></span>
<span data-ttu-id="60069-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60069-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60069-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60069-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60069-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60069-131">CommonParameters</span></span>
<span data-ttu-id="60069-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60069-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60069-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60069-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60069-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60069-134">INPUTS</span></span>

### <span data-ttu-id="60069-135">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="60069-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="60069-136">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="60069-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60069-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60069-137">OUTPUTS</span></span>

### <span data-ttu-id="60069-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60069-138">System.Boolean</span></span>

## <span data-ttu-id="60069-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="60069-139">NOTES</span></span>

## <span data-ttu-id="60069-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60069-140">RELATED LINKS</span></span>

[<span data-ttu-id="60069-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60069-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="60069-142">Neu – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60069-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="60069-143">Satz-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60069-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="60069-144">Anfang-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60069-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="60069-145">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60069-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


