---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: fa0e3682d62f01d7d305d190c6765aab709bed15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498374"
---
# <span data-ttu-id="d33de-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d33de-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="d33de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d33de-102">SYNOPSIS</span></span>
<span data-ttu-id="d33de-103">Entfernt eine benutzerdefinierte Domäne.</span><span class="sxs-lookup"><span data-stu-id="d33de-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d33de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d33de-104">SYNTAX</span></span>

### <span data-ttu-id="d33de-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d33de-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d33de-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d33de-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d33de-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d33de-107">DESCRIPTION</span></span>
<span data-ttu-id="d33de-108">Das Cmdlet **Remove-AzureRmCdnCustomDomain** entfernt die benutzerdefinierte Domäne aus einem Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="d33de-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d33de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d33de-109">EXAMPLES</span></span>

## <span data-ttu-id="d33de-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d33de-110">PARAMETERS</span></span>

### <span data-ttu-id="d33de-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d33de-111">-CdnCustomDomain</span></span>
<span data-ttu-id="d33de-112">Gibt die benutzerdefinierte Domäne an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d33de-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d33de-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d33de-113">-CustomDomainName</span></span>
<span data-ttu-id="d33de-114">Gibt den Ressourcennamen der benutzerdefinierten Domäne an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d33de-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d33de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33de-115">-DefaultProfile</span></span>
<span data-ttu-id="d33de-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d33de-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d33de-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="d33de-117">-EndpointName</span></span>
<span data-ttu-id="d33de-118">Gibt den Namen des Endpunkts an, von dem dieses Cmdlet eine benutzerdefinierte Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="d33de-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="d33de-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d33de-119">-PassThru</span></span>
<span data-ttu-id="d33de-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d33de-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d33de-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d33de-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d33de-122">-Profilname</span><span class="sxs-lookup"><span data-stu-id="d33de-122">-ProfileName</span></span>
<span data-ttu-id="d33de-123">Gibt den Namen des Profils an, aus dem dieses Cmdlet eine benutzerdefinierte Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="d33de-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="d33de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d33de-124">-ResourceGroupName</span></span>
<span data-ttu-id="d33de-125">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet eine benutzerdefinierte Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="d33de-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="d33de-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d33de-126">-Confirm</span></span>
<span data-ttu-id="d33de-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d33de-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d33de-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d33de-128">-WhatIf</span></span>
<span data-ttu-id="d33de-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d33de-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d33de-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d33de-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d33de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33de-131">CommonParameters</span></span>
<span data-ttu-id="d33de-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d33de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33de-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d33de-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33de-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d33de-134">INPUTS</span></span>

### <span data-ttu-id="d33de-135">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d33de-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="d33de-136">Parameter: CdnCustomDomain (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d33de-136">Parameters: CdnCustomDomain (ByValue)</span></span>

### <span data-ttu-id="d33de-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d33de-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d33de-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d33de-138">OUTPUTS</span></span>

### <span data-ttu-id="d33de-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d33de-139">System.Boolean</span></span>

## <span data-ttu-id="d33de-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d33de-140">NOTES</span></span>

## <span data-ttu-id="d33de-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d33de-141">RELATED LINKS</span></span>

[<span data-ttu-id="d33de-142">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d33de-142">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="d33de-143">Neu – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d33de-143">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="d33de-144">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d33de-144">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


