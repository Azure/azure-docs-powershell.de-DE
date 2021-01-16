---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301171"
---
# <span data-ttu-id="6b918-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6b918-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="6b918-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b918-102">SYNOPSIS</span></span>
<span data-ttu-id="6b918-103">Die Registrierung eines Features eines Azure-Anbieters in Ihrem Konto wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="6b918-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="6b918-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b918-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b918-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b918-105">DESCRIPTION</span></span>
<span data-ttu-id="6b918-106">Mit **dem Cmdlet "Unregister-AzProviderFeature"** wird die Registrierung eines Features eines Azure-Anbieters in Ihrem Konto aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="6b918-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="6b918-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b918-107">EXAMPLES</span></span>

### <span data-ttu-id="6b918-108">Beispiel 1: Aufheben der Registrierung eines Features</span><span class="sxs-lookup"><span data-stu-id="6b918-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="6b918-109">Dadurch wird die Registrierung des Features "AllowApplicationSecurityGroups" für Microsoft.Network von Ihrem Konto aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="6b918-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="6b918-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b918-110">PARAMETERS</span></span>

### <span data-ttu-id="6b918-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b918-111">-DefaultProfile</span></span>
<span data-ttu-id="6b918-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b918-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b918-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="6b918-113">-FeatureName</span></span>
<span data-ttu-id="6b918-114">Der Name des Features.</span><span class="sxs-lookup"><span data-stu-id="6b918-114">The feature name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b918-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="6b918-115">-ProviderNamespace</span></span>
<span data-ttu-id="6b918-116">Der Namespace des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="6b918-116">The resource provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b918-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b918-117">-Confirm</span></span>
<span data-ttu-id="6b918-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b918-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b918-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6b918-119">-WhatIf</span></span>
<span data-ttu-id="6b918-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b918-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b918-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b918-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b918-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b918-122">CommonParameters</span></span>
<span data-ttu-id="6b918-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b918-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b918-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b918-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b918-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b918-125">INPUTS</span></span>

### <span data-ttu-id="6b918-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6b918-126">System.String</span></span>

## <span data-ttu-id="6b918-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b918-127">OUTPUTS</span></span>

### <span data-ttu-id="6b918-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6b918-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="6b918-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6b918-129">NOTES</span></span>

## <span data-ttu-id="6b918-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6b918-130">RELATED LINKS</span></span>