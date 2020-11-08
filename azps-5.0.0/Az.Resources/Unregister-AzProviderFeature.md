---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178407"
---
# <span data-ttu-id="c790b-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c790b-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="c790b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c790b-102">SYNOPSIS</span></span>
<span data-ttu-id="c790b-103">Hebt die Registrierung eines Azure-Anbieter Features in Ihrem Konto auf.</span><span class="sxs-lookup"><span data-stu-id="c790b-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="c790b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c790b-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c790b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c790b-105">DESCRIPTION</span></span>
<span data-ttu-id="c790b-106">Mit dem Cmdlet " **Unregister-AzProviderFeature** " wird die Registrierung eines Azure-Anbieter Features in Ihrem Konto aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="c790b-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="c790b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c790b-107">EXAMPLES</span></span>

### <span data-ttu-id="c790b-108">Beispiel 1: Aufheben der Registrierung eines Features</span><span class="sxs-lookup"><span data-stu-id="c790b-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="c790b-109">Dadurch wird die Registrierung der AllowApplicationSecurityGroups-Funktion für Microsoft. Network von Ihrem Konto aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="c790b-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="c790b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c790b-110">PARAMETERS</span></span>

### <span data-ttu-id="c790b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c790b-111">-DefaultProfile</span></span>
<span data-ttu-id="c790b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c790b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c790b-113">-Featurename</span><span class="sxs-lookup"><span data-stu-id="c790b-113">-FeatureName</span></span>
<span data-ttu-id="c790b-114">Der Name der Funktion.</span><span class="sxs-lookup"><span data-stu-id="c790b-114">The feature name.</span></span>

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

### <span data-ttu-id="c790b-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c790b-115">-ProviderNamespace</span></span>
<span data-ttu-id="c790b-116">Der Ressourcenanbieter-Namespace.</span><span class="sxs-lookup"><span data-stu-id="c790b-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="c790b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c790b-117">-Confirm</span></span>
<span data-ttu-id="c790b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c790b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c790b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c790b-119">-WhatIf</span></span>
<span data-ttu-id="c790b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c790b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c790b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c790b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c790b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c790b-122">CommonParameters</span></span>
<span data-ttu-id="c790b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c790b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c790b-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c790b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c790b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c790b-125">INPUTS</span></span>

### <span data-ttu-id="c790b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c790b-126">System.String</span></span>

## <span data-ttu-id="c790b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c790b-127">OUTPUTS</span></span>

### <span data-ttu-id="c790b-128">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c790b-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="c790b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c790b-129">NOTES</span></span>

## <span data-ttu-id="c790b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c790b-130">RELATED LINKS</span></span>