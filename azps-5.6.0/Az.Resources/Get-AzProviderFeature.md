---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 67a0eee0dfe46b7b846958e1aa3f2be515a6b213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950640"
---
# <span data-ttu-id="49968-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="49968-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="49968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49968-102">SYNOPSIS</span></span>
<span data-ttu-id="49968-103">Ruft Informationen zu Azure-Anbieterfeatures ab.</span><span class="sxs-lookup"><span data-stu-id="49968-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="49968-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49968-104">SYNTAX</span></span>

### <span data-ttu-id="49968-105">ListAvailableParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="49968-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49968-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="49968-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49968-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49968-107">DESCRIPTION</span></span>
<span data-ttu-id="49968-108">Das **Get-AzProviderFeature-Cmdlet** ruft den Featurenamen, den Anbieternamen und den Registrierungsstatus für Azure-Anbieterfeatures ab.</span><span class="sxs-lookup"><span data-stu-id="49968-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="49968-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49968-109">EXAMPLES</span></span>

### <span data-ttu-id="49968-110">Beispiel 1: Alle verfügbaren Features erhalten</span><span class="sxs-lookup"><span data-stu-id="49968-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="49968-111">Dieser Befehl ruft alle verfügbaren Features ab.</span><span class="sxs-lookup"><span data-stu-id="49968-111">This command gets all available features.</span></span>

### <span data-ttu-id="49968-112">Beispiel 2: Informationen zu einem bestimmten Feature erhalten</span><span class="sxs-lookup"><span data-stu-id="49968-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="49968-113">Dieser Befehl ruft Informationen für das Feature "AllowPreReleaseRegions" für den angegebenen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="49968-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="49968-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="49968-114">PARAMETERS</span></span>

### <span data-ttu-id="49968-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49968-115">-DefaultProfile</span></span>
<span data-ttu-id="49968-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="49968-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49968-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="49968-117">-FeatureName</span></span>
<span data-ttu-id="49968-118">Gibt den Namen des zu erhaltenden Features an.</span><span class="sxs-lookup"><span data-stu-id="49968-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49968-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="49968-119">-ListAvailable</span></span>
<span data-ttu-id="49968-120">Gibt an, dass dieses Cmdlet alle Features erhält.</span><span class="sxs-lookup"><span data-stu-id="49968-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49968-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="49968-121">-ProviderNamespace</span></span>
<span data-ttu-id="49968-122">Gibt den Namespace an, für den dieses Cmdlet Anbieterfeatures erhält.</span><span class="sxs-lookup"><span data-stu-id="49968-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49968-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49968-123">CommonParameters</span></span>
<span data-ttu-id="49968-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49968-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49968-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49968-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49968-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49968-126">INPUTS</span></span>

### <span data-ttu-id="49968-127">System.String</span><span class="sxs-lookup"><span data-stu-id="49968-127">System.String</span></span>

## <span data-ttu-id="49968-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49968-128">OUTPUTS</span></span>

### <span data-ttu-id="49968-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="49968-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="49968-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="49968-130">NOTES</span></span>

## <span data-ttu-id="49968-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="49968-131">RELATED LINKS</span></span>

[<span data-ttu-id="49968-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="49968-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


