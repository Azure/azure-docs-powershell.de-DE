---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: d13eb98b01380fcb02392d1ac3f34c8d70c7f6dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663756"
---
# <span data-ttu-id="83759-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="83759-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="83759-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83759-102">SYNOPSIS</span></span>
<span data-ttu-id="83759-103">Ruft Informationen zu Azure-Anbieter Features ab.</span><span class="sxs-lookup"><span data-stu-id="83759-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83759-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83759-104">SYNTAX</span></span>

### <span data-ttu-id="83759-105">ListAvailableParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="83759-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83759-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="83759-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83759-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83759-107">DESCRIPTION</span></span>
<span data-ttu-id="83759-108">Das Cmdlet " **Get-AzureRmProviderFeature** " Ruft den Funktionsnamen, den Anbieternamen und den Registrierungsstatus für Azure-Anbieter Features ab.</span><span class="sxs-lookup"><span data-stu-id="83759-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="83759-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83759-109">EXAMPLES</span></span>

### <span data-ttu-id="83759-110">Beispiel 1: Abrufen aller verfügbaren Features</span><span class="sxs-lookup"><span data-stu-id="83759-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="83759-111">Dieser Befehl ruft alle verfügbaren Features ab.</span><span class="sxs-lookup"><span data-stu-id="83759-111">This command gets all available features.</span></span>

### <span data-ttu-id="83759-112">Beispiel 2: Abrufen von Informationen zu einem bestimmten Feature</span><span class="sxs-lookup"><span data-stu-id="83759-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="83759-113">Dieser Befehl ruft Informationen für das Feature mit dem Namen AllowPreReleaseRegions für den angegebenen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="83759-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="83759-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="83759-114">PARAMETERS</span></span>

### <span data-ttu-id="83759-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83759-115">-DefaultProfile</span></span>
<span data-ttu-id="83759-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="83759-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83759-117">-Featurename</span><span class="sxs-lookup"><span data-stu-id="83759-117">-FeatureName</span></span>
<span data-ttu-id="83759-118">Gibt den Namen des abzurufenden Features an.</span><span class="sxs-lookup"><span data-stu-id="83759-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83759-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="83759-119">-ListAvailable</span></span>
<span data-ttu-id="83759-120">Gibt an, dass dieses Cmdlet alle Features abruft.</span><span class="sxs-lookup"><span data-stu-id="83759-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83759-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="83759-121">-ProviderNamespace</span></span>
<span data-ttu-id="83759-122">Gibt den Namespace an, für den dieses Cmdlet Anbieter Features erhält.</span><span class="sxs-lookup"><span data-stu-id="83759-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83759-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83759-123">CommonParameters</span></span>
<span data-ttu-id="83759-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83759-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83759-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83759-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83759-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83759-126">INPUTS</span></span>

### <span data-ttu-id="83759-127">Keine</span><span class="sxs-lookup"><span data-stu-id="83759-127">None</span></span>
<span data-ttu-id="83759-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="83759-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83759-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83759-129">OUTPUTS</span></span>

### <span data-ttu-id="83759-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="83759-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="83759-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="83759-131">NOTES</span></span>

## <span data-ttu-id="83759-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83759-132">RELATED LINKS</span></span>

[<span data-ttu-id="83759-133">Registrieren-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="83759-133">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


