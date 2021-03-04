---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 8fe856b1b8b710c1db139474f15d432f32c2652a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933739"
---
# <span data-ttu-id="3e940-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3e940-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="3e940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e940-102">SYNOPSIS</span></span>
<span data-ttu-id="3e940-103">Registriert einen Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="3e940-103">Registers a resource provider.</span></span>

## <span data-ttu-id="3e940-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e940-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e940-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e940-105">DESCRIPTION</span></span>
<span data-ttu-id="3e940-106">Das **Cmdlet Register-AzResourceProvider** registriert einen Azure-Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="3e940-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="3e940-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e940-107">EXAMPLES</span></span>

### <span data-ttu-id="3e940-108">Beispiel 1: Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="3e940-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="3e940-109">Dadurch wird der Microsoft.Network-Anbieter für Ihr Konto registriert.</span><span class="sxs-lookup"><span data-stu-id="3e940-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="3e940-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3e940-110">PARAMETERS</span></span>

### <span data-ttu-id="3e940-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3e940-111">-ApiVersion</span></span>
<span data-ttu-id="3e940-112">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="3e940-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3e940-113">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="3e940-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e940-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e940-114">-DefaultProfile</span></span>
<span data-ttu-id="3e940-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3e940-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e940-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="3e940-116">-Pre</span></span>
<span data-ttu-id="3e940-117">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e940-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e940-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3e940-118">-ProviderNamespace</span></span>
<span data-ttu-id="3e940-119">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="3e940-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="3e940-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e940-120">-Confirm</span></span>
<span data-ttu-id="3e940-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e940-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e940-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e940-122">-WhatIf</span></span>
<span data-ttu-id="3e940-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e940-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e940-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e940-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e940-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e940-125">CommonParameters</span></span>
<span data-ttu-id="3e940-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e940-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e940-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e940-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e940-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e940-128">INPUTS</span></span>

### <span data-ttu-id="3e940-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3e940-129">System.String</span></span>

## <span data-ttu-id="3e940-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e940-130">OUTPUTS</span></span>

### <span data-ttu-id="3e940-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3e940-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="3e940-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3e940-132">NOTES</span></span>

## <span data-ttu-id="3e940-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3e940-133">RELATED LINKS</span></span>

[<span data-ttu-id="3e940-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3e940-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="3e940-135">Aufheben der Registrierung-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3e940-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


