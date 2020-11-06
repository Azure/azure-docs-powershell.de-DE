---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: 6be1d4f755d11c6c0cbd32488b59f4e141278633
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480117"
---
# <span data-ttu-id="c2ddd-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c2ddd-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="c2ddd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ddd-103">Registriert ein Azure-Anbieter Feature in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2ddd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2ddd-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ddd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ddd-106">Das Cmdlet " **Register-AzureRmProviderFeature** " registriert ein Azure-Anbieter Feature in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="c2ddd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="c2ddd-108">Beispiel 1: Registrieren eines Features</span><span class="sxs-lookup"><span data-stu-id="c2ddd-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="c2ddd-109">Dadurch wird das AllowApplicationSecurityGroups-Feature für Microsoft. Network zu Ihrem Konto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="c2ddd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2ddd-110">PARAMETERS</span></span>

### <span data-ttu-id="c2ddd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ddd-111">-DefaultProfile</span></span>
<span data-ttu-id="c2ddd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c2ddd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2ddd-113">-Featurename</span><span class="sxs-lookup"><span data-stu-id="c2ddd-113">-FeatureName</span></span>
<span data-ttu-id="c2ddd-114">Gibt den Namen des vom Cmdlet registrierten Features an.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ddd-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c2ddd-115">-ProviderNamespace</span></span>
<span data-ttu-id="c2ddd-116">Gibt einen Namespace an, für den dieses Cmdlet ein Anbieter Feature registriert.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ddd-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2ddd-117">-Confirm</span></span>
<span data-ttu-id="c2ddd-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ddd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ddd-119">-WhatIf</span></span>
<span data-ttu-id="c2ddd-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ddd-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ddd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ddd-122">CommonParameters</span></span>
<span data-ttu-id="c2ddd-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ddd-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ddd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ddd-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2ddd-125">INPUTS</span></span>

## <span data-ttu-id="c2ddd-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2ddd-126">OUTPUTS</span></span>

## <span data-ttu-id="c2ddd-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2ddd-127">NOTES</span></span>

## <span data-ttu-id="c2ddd-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2ddd-128">RELATED LINKS</span></span>

[<span data-ttu-id="c2ddd-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c2ddd-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


