---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 1ab198fc422cfb0f880f8c1a3dcd860134b4c2c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950632"
---
# <span data-ttu-id="fa80c-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fa80c-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="fa80c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa80c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa80c-103">Registriert ein Azure-Anbieterfeature in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="fa80c-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="fa80c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa80c-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa80c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa80c-105">DESCRIPTION</span></span>
<span data-ttu-id="fa80c-106">Das **Cmdlet Register-AzProviderFeature** registriert ein Azure-Anbieterfeature in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="fa80c-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="fa80c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa80c-107">EXAMPLES</span></span>

### <span data-ttu-id="fa80c-108">Beispiel 1: Registrieren eines Features</span><span class="sxs-lookup"><span data-stu-id="fa80c-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="fa80c-109">Dadurch wird Ihrem Konto das Feature AllowApplicationSecurityGroups für Microsoft.Network hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="fa80c-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="fa80c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fa80c-110">PARAMETERS</span></span>

### <span data-ttu-id="fa80c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa80c-111">-DefaultProfile</span></span>
<span data-ttu-id="fa80c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fa80c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa80c-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="fa80c-113">-FeatureName</span></span>
<span data-ttu-id="fa80c-114">Gibt den Namen des Features an, das von diesem Cmdlet registriert wird.</span><span class="sxs-lookup"><span data-stu-id="fa80c-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="fa80c-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fa80c-115">-ProviderNamespace</span></span>
<span data-ttu-id="fa80c-116">Gibt einen Namespace an, für den dieses Cmdlet ein Anbieterfeature registriert.</span><span class="sxs-lookup"><span data-stu-id="fa80c-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="fa80c-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa80c-117">-Confirm</span></span>
<span data-ttu-id="fa80c-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa80c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa80c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa80c-119">-WhatIf</span></span>
<span data-ttu-id="fa80c-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa80c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa80c-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa80c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa80c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa80c-122">CommonParameters</span></span>
<span data-ttu-id="fa80c-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa80c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa80c-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa80c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa80c-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa80c-125">INPUTS</span></span>

### <span data-ttu-id="fa80c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="fa80c-126">System.String</span></span>

## <span data-ttu-id="fa80c-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa80c-127">OUTPUTS</span></span>

### <span data-ttu-id="fa80c-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fa80c-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="fa80c-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fa80c-129">NOTES</span></span>

## <span data-ttu-id="fa80c-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fa80c-130">RELATED LINKS</span></span>

[<span data-ttu-id="fa80c-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fa80c-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


