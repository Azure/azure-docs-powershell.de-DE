---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 1296e1e135acce9d4840e625d96931f6ecc11625
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843432"
---
# <span data-ttu-id="aef0d-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="aef0d-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="aef0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aef0d-102">SYNOPSIS</span></span>
<span data-ttu-id="aef0d-103">Ruft Informationen zu Azure-Anbieter Features ab.</span><span class="sxs-lookup"><span data-stu-id="aef0d-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="aef0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aef0d-104">SYNTAX</span></span>

### <span data-ttu-id="aef0d-105">ListAvailableParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aef0d-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aef0d-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="aef0d-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aef0d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aef0d-107">DESCRIPTION</span></span>
<span data-ttu-id="aef0d-108">Das Cmdlet " **Get-AzProviderFeature** " Ruft den Funktionsnamen, den Anbieternamen und den Registrierungsstatus für Azure-Anbieter Features ab.</span><span class="sxs-lookup"><span data-stu-id="aef0d-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="aef0d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aef0d-109">EXAMPLES</span></span>

### <span data-ttu-id="aef0d-110">Beispiel 1: Abrufen aller verfügbaren Features</span><span class="sxs-lookup"><span data-stu-id="aef0d-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="aef0d-111">Dieser Befehl ruft alle verfügbaren Features ab.</span><span class="sxs-lookup"><span data-stu-id="aef0d-111">This command gets all available features.</span></span>

### <span data-ttu-id="aef0d-112">Beispiel 2: Abrufen von Informationen zu einem bestimmten Feature</span><span class="sxs-lookup"><span data-stu-id="aef0d-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="aef0d-113">Dieser Befehl ruft Informationen für das Feature mit dem Namen AllowPreReleaseRegions für den angegebenen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="aef0d-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="aef0d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="aef0d-114">PARAMETERS</span></span>

### <span data-ttu-id="aef0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef0d-115">-DefaultProfile</span></span>
<span data-ttu-id="aef0d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="aef0d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef0d-117">-Featurename</span><span class="sxs-lookup"><span data-stu-id="aef0d-117">-FeatureName</span></span>
<span data-ttu-id="aef0d-118">Gibt den Namen des abzurufenden Features an.</span><span class="sxs-lookup"><span data-stu-id="aef0d-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="aef0d-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="aef0d-119">-ListAvailable</span></span>
<span data-ttu-id="aef0d-120">Gibt an, dass dieses Cmdlet alle Features abruft.</span><span class="sxs-lookup"><span data-stu-id="aef0d-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="aef0d-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="aef0d-121">-ProviderNamespace</span></span>
<span data-ttu-id="aef0d-122">Gibt den Namespace an, für den dieses Cmdlet Anbieter Features erhält.</span><span class="sxs-lookup"><span data-stu-id="aef0d-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="aef0d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef0d-123">CommonParameters</span></span>
<span data-ttu-id="aef0d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef0d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef0d-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef0d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef0d-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aef0d-126">INPUTS</span></span>

## <span data-ttu-id="aef0d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aef0d-127">OUTPUTS</span></span>

## <span data-ttu-id="aef0d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="aef0d-128">NOTES</span></span>

## <span data-ttu-id="aef0d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aef0d-129">RELATED LINKS</span></span>

[<span data-ttu-id="aef0d-130">Registrieren-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="aef0d-130">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


