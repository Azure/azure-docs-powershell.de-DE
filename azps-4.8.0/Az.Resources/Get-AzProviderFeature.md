---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167388"
---
# <span data-ttu-id="04369-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="04369-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="04369-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04369-102">SYNOPSIS</span></span>
<span data-ttu-id="04369-103">Ruft Informationen zu Azure-Anbieter Features ab.</span><span class="sxs-lookup"><span data-stu-id="04369-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="04369-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04369-104">SYNTAX</span></span>

### <span data-ttu-id="04369-105">ListAvailableParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="04369-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04369-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="04369-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04369-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04369-107">DESCRIPTION</span></span>
<span data-ttu-id="04369-108">Das Cmdlet " **Get-AzProviderFeature** " Ruft den Funktionsnamen, den Anbieternamen und den Registrierungsstatus für Azure-Anbieter Features ab.</span><span class="sxs-lookup"><span data-stu-id="04369-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="04369-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04369-109">EXAMPLES</span></span>

### <span data-ttu-id="04369-110">Beispiel 1: Abrufen aller verfügbaren Features</span><span class="sxs-lookup"><span data-stu-id="04369-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="04369-111">Dieser Befehl ruft alle verfügbaren Features ab.</span><span class="sxs-lookup"><span data-stu-id="04369-111">This command gets all available features.</span></span>

### <span data-ttu-id="04369-112">Beispiel 2: Abrufen von Informationen zu einem bestimmten Feature</span><span class="sxs-lookup"><span data-stu-id="04369-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="04369-113">Dieser Befehl ruft Informationen für das Feature mit dem Namen AllowPreReleaseRegions für den angegebenen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="04369-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="04369-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="04369-114">PARAMETERS</span></span>

### <span data-ttu-id="04369-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04369-115">-DefaultProfile</span></span>
<span data-ttu-id="04369-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="04369-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04369-117">-Featurename</span><span class="sxs-lookup"><span data-stu-id="04369-117">-FeatureName</span></span>
<span data-ttu-id="04369-118">Gibt den Namen des abzurufenden Features an.</span><span class="sxs-lookup"><span data-stu-id="04369-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="04369-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="04369-119">-ListAvailable</span></span>
<span data-ttu-id="04369-120">Gibt an, dass dieses Cmdlet alle Features abruft.</span><span class="sxs-lookup"><span data-stu-id="04369-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="04369-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="04369-121">-ProviderNamespace</span></span>
<span data-ttu-id="04369-122">Gibt den Namespace an, für den dieses Cmdlet Anbieter Features erhält.</span><span class="sxs-lookup"><span data-stu-id="04369-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="04369-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04369-123">CommonParameters</span></span>
<span data-ttu-id="04369-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04369-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04369-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04369-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04369-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04369-126">INPUTS</span></span>

### <span data-ttu-id="04369-127">System. String</span><span class="sxs-lookup"><span data-stu-id="04369-127">System.String</span></span>

## <span data-ttu-id="04369-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04369-128">OUTPUTS</span></span>

### <span data-ttu-id="04369-129">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="04369-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="04369-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="04369-130">NOTES</span></span>

## <span data-ttu-id="04369-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04369-131">RELATED LINKS</span></span>

[<span data-ttu-id="04369-132">Registrieren-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="04369-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


