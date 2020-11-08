---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995034"
---
# <span data-ttu-id="af734-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="af734-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="af734-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af734-102">SYNOPSIS</span></span>
<span data-ttu-id="af734-103">Entfernt eine benutzerdefinierte Domäne.</span><span class="sxs-lookup"><span data-stu-id="af734-103">Removes a custom domain.</span></span>

## <span data-ttu-id="af734-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af734-104">SYNTAX</span></span>

### <span data-ttu-id="af734-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="af734-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af734-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af734-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af734-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af734-107">DESCRIPTION</span></span>
<span data-ttu-id="af734-108">Das Cmdlet **Remove-AzCdnCustomDomain** entfernt die benutzerdefinierte Domäne aus einem Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="af734-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="af734-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af734-109">EXAMPLES</span></span>

## <span data-ttu-id="af734-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="af734-110">PARAMETERS</span></span>

### <span data-ttu-id="af734-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="af734-111">-CdnCustomDomain</span></span>
<span data-ttu-id="af734-112">Gibt die benutzerdefinierte Domäne an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="af734-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af734-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="af734-113">-CustomDomainName</span></span>
<span data-ttu-id="af734-114">Gibt den Ressourcennamen der benutzerdefinierten Domäne an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="af734-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="af734-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af734-115">-DefaultProfile</span></span>
<span data-ttu-id="af734-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="af734-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af734-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="af734-117">-EndpointName</span></span>
<span data-ttu-id="af734-118">Gibt den Namen des Endpunkts an, von dem dieses Cmdlet eine benutzerdefinierte Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="af734-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="af734-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af734-119">-PassThru</span></span>
<span data-ttu-id="af734-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="af734-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="af734-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="af734-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af734-122">-Profilname</span><span class="sxs-lookup"><span data-stu-id="af734-122">-ProfileName</span></span>
<span data-ttu-id="af734-123">Gibt den Namen des Profils an, aus dem dieses Cmdlet eine benutzerdefinierte Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="af734-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="af734-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af734-124">-ResourceGroupName</span></span>
<span data-ttu-id="af734-125">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet eine benutzerdefinierte Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="af734-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="af734-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af734-126">-Confirm</span></span>
<span data-ttu-id="af734-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af734-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af734-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af734-128">-WhatIf</span></span>
<span data-ttu-id="af734-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af734-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af734-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af734-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af734-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af734-131">CommonParameters</span></span>
<span data-ttu-id="af734-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af734-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af734-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af734-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af734-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af734-134">INPUTS</span></span>

### <span data-ttu-id="af734-135">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="af734-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="af734-136">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="af734-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af734-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af734-137">OUTPUTS</span></span>

### <span data-ttu-id="af734-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af734-138">System.Boolean</span></span>

## <span data-ttu-id="af734-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="af734-139">NOTES</span></span>

## <span data-ttu-id="af734-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af734-140">RELATED LINKS</span></span>

[<span data-ttu-id="af734-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="af734-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="af734-142">Neu – AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="af734-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="af734-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="af734-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


