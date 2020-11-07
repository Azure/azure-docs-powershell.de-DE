---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 57a01f831ab92b7ae8ca45fbf9535ed4fa7df0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659579"
---
# <span data-ttu-id="32af9-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="32af9-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="32af9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32af9-102">SYNOPSIS</span></span>
<span data-ttu-id="32af9-103">Registriert ein Azure-Anbieter Feature in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="32af9-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="32af9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32af9-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32af9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32af9-105">DESCRIPTION</span></span>
<span data-ttu-id="32af9-106">Das Cmdlet " **Register-AzProviderFeature** " registriert ein Azure-Anbieter Feature in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="32af9-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="32af9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32af9-107">EXAMPLES</span></span>

### <span data-ttu-id="32af9-108">Beispiel 1: Registrieren eines Features</span><span class="sxs-lookup"><span data-stu-id="32af9-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="32af9-109">Dadurch wird das AllowApplicationSecurityGroups-Feature für Microsoft. Network zu Ihrem Konto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="32af9-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="32af9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="32af9-110">PARAMETERS</span></span>

### <span data-ttu-id="32af9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32af9-111">-DefaultProfile</span></span>
<span data-ttu-id="32af9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="32af9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32af9-113">-Featurename</span><span class="sxs-lookup"><span data-stu-id="32af9-113">-FeatureName</span></span>
<span data-ttu-id="32af9-114">Gibt den Namen des vom Cmdlet registrierten Features an.</span><span class="sxs-lookup"><span data-stu-id="32af9-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="32af9-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="32af9-115">-ProviderNamespace</span></span>
<span data-ttu-id="32af9-116">Gibt einen Namespace an, für den dieses Cmdlet ein Anbieter Feature registriert.</span><span class="sxs-lookup"><span data-stu-id="32af9-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="32af9-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32af9-117">-Confirm</span></span>
<span data-ttu-id="32af9-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32af9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32af9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32af9-119">-WhatIf</span></span>
<span data-ttu-id="32af9-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32af9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32af9-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32af9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32af9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32af9-122">CommonParameters</span></span>
<span data-ttu-id="32af9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32af9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32af9-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32af9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32af9-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32af9-125">INPUTS</span></span>

### <span data-ttu-id="32af9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="32af9-126">System.String</span></span>

## <span data-ttu-id="32af9-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32af9-127">OUTPUTS</span></span>

### <span data-ttu-id="32af9-128">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="32af9-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="32af9-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="32af9-129">NOTES</span></span>

## <span data-ttu-id="32af9-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32af9-130">RELATED LINKS</span></span>

[<span data-ttu-id="32af9-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="32af9-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


