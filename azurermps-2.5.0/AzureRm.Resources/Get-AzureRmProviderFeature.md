---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 182accdabc368e72451a0c1d9a1d78f1cf561730
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849511"
---
# <span data-ttu-id="b77ed-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="b77ed-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="b77ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b77ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b77ed-103">Ruft Informationen zu Azure-Anbieter Features ab.</span><span class="sxs-lookup"><span data-stu-id="b77ed-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b77ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b77ed-104">SYNTAX</span></span>

### <span data-ttu-id="b77ed-105">ListAvailableParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b77ed-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77ed-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="b77ed-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b77ed-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b77ed-107">DESCRIPTION</span></span>
<span data-ttu-id="b77ed-108">Das Cmdlet " **Get-AzureRmProviderFeature** " Ruft den Funktionsnamen, den Anbieternamen und den Registrierungsstatus für Azure-Anbieter Features ab.</span><span class="sxs-lookup"><span data-stu-id="b77ed-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="b77ed-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b77ed-109">EXAMPLES</span></span>

### <span data-ttu-id="b77ed-110">Beispiel 1: Abrufen aller verfügbaren Features</span><span class="sxs-lookup"><span data-stu-id="b77ed-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="b77ed-111">Dieser Befehl ruft alle verfügbaren Features ab.</span><span class="sxs-lookup"><span data-stu-id="b77ed-111">This command gets all available features.</span></span>

### <span data-ttu-id="b77ed-112">Beispiel 2: Abrufen von Informationen zu einem bestimmten Feature</span><span class="sxs-lookup"><span data-stu-id="b77ed-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="b77ed-113">Dieser Befehl ruft Informationen für das Feature mit dem Namen AllowPreReleaseRegions für den angegebenen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="b77ed-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="b77ed-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b77ed-114">PARAMETERS</span></span>

### <span data-ttu-id="b77ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77ed-115">-DefaultProfile</span></span>
<span data-ttu-id="b77ed-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b77ed-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b77ed-117">-Featurename</span><span class="sxs-lookup"><span data-stu-id="b77ed-117">-FeatureName</span></span>
<span data-ttu-id="b77ed-118">Gibt den Namen des abzurufenden Features an.</span><span class="sxs-lookup"><span data-stu-id="b77ed-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="b77ed-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b77ed-119">-ListAvailable</span></span>
<span data-ttu-id="b77ed-120">Gibt an, dass dieses Cmdlet alle Features abruft.</span><span class="sxs-lookup"><span data-stu-id="b77ed-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="b77ed-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b77ed-121">-ProviderNamespace</span></span>
<span data-ttu-id="b77ed-122">Gibt den Namespace an, für den dieses Cmdlet Anbieter Features erhält.</span><span class="sxs-lookup"><span data-stu-id="b77ed-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="b77ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77ed-123">CommonParameters</span></span>
<span data-ttu-id="b77ed-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77ed-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77ed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77ed-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b77ed-126">INPUTS</span></span>

## <span data-ttu-id="b77ed-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b77ed-127">OUTPUTS</span></span>

## <span data-ttu-id="b77ed-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b77ed-128">NOTES</span></span>

## <span data-ttu-id="b77ed-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b77ed-129">RELATED LINKS</span></span>

[<span data-ttu-id="b77ed-130">Registrieren-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="b77ed-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


