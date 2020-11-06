---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500733"
---
# <span data-ttu-id="830cf-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="830cf-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="830cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="830cf-102">SYNOPSIS</span></span>
<span data-ttu-id="830cf-103">Registriert ein Azure-Anbieter Feature in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="830cf-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="830cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="830cf-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="830cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="830cf-105">DESCRIPTION</span></span>
<span data-ttu-id="830cf-106">Das Cmdlet " **Register-AzureRmProviderFeature** " registriert ein Azure-Anbieter Feature in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="830cf-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="830cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="830cf-107">EXAMPLES</span></span>

## <span data-ttu-id="830cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="830cf-108">PARAMETERS</span></span>

### <span data-ttu-id="830cf-109">-Featurename</span><span class="sxs-lookup"><span data-stu-id="830cf-109">-FeatureName</span></span>
<span data-ttu-id="830cf-110">Gibt den Namen des vom Cmdlet registrierten Features an.</span><span class="sxs-lookup"><span data-stu-id="830cf-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="830cf-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="830cf-111">-ProviderNamespace</span></span>
<span data-ttu-id="830cf-112">Gibt einen Namespace an, für den dieses Cmdlet ein Anbieter Feature registriert.</span><span class="sxs-lookup"><span data-stu-id="830cf-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="830cf-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="830cf-113">-Confirm</span></span>
<span data-ttu-id="830cf-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="830cf-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="830cf-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="830cf-115">-WhatIf</span></span>
<span data-ttu-id="830cf-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="830cf-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="830cf-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="830cf-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="830cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830cf-118">-DefaultProfile</span></span>
<span data-ttu-id="830cf-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="830cf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="830cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830cf-120">CommonParameters</span></span>
<span data-ttu-id="830cf-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830cf-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="830cf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830cf-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="830cf-123">INPUTS</span></span>

## <span data-ttu-id="830cf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="830cf-124">OUTPUTS</span></span>

### <span data-ttu-id="830cf-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="830cf-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="830cf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="830cf-126">NOTES</span></span>

## <span data-ttu-id="830cf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="830cf-127">RELATED LINKS</span></span>

[<span data-ttu-id="830cf-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="830cf-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


