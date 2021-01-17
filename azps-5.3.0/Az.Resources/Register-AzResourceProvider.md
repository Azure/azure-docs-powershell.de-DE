---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459259"
---
# <span data-ttu-id="133d3-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="133d3-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="133d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="133d3-102">SYNOPSIS</span></span>
<span data-ttu-id="133d3-103">Registriert einen Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="133d3-103">Registers a resource provider.</span></span>

## <span data-ttu-id="133d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="133d3-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="133d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="133d3-105">DESCRIPTION</span></span>
<span data-ttu-id="133d3-106">Das **Cmdlet "Register-AzResourceProvider"** registriert einen Azure-Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="133d3-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="133d3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="133d3-107">EXAMPLES</span></span>

### <span data-ttu-id="133d3-108">Beispiel 1: Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="133d3-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="133d3-109">Dadurch wird der Microsoft.Network-Anbieter für Ihr Konto registriert.</span><span class="sxs-lookup"><span data-stu-id="133d3-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="133d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="133d3-110">PARAMETERS</span></span>

### <span data-ttu-id="133d3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="133d3-111">-ApiVersion</span></span>
<span data-ttu-id="133d3-112">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="133d3-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="133d3-113">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="133d3-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="133d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133d3-114">-DefaultProfile</span></span>
<span data-ttu-id="133d3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="133d3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="133d3-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="133d3-116">-Pre</span></span>
<span data-ttu-id="133d3-117">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="133d3-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="133d3-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="133d3-118">-ProviderNamespace</span></span>
<span data-ttu-id="133d3-119">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="133d3-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="133d3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="133d3-120">-Confirm</span></span>
<span data-ttu-id="133d3-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="133d3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="133d3-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="133d3-122">-WhatIf</span></span>
<span data-ttu-id="133d3-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="133d3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="133d3-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="133d3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="133d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133d3-125">CommonParameters</span></span>
<span data-ttu-id="133d3-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="133d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133d3-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="133d3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133d3-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="133d3-128">INPUTS</span></span>

### <span data-ttu-id="133d3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="133d3-129">System.String</span></span>

## <span data-ttu-id="133d3-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="133d3-130">OUTPUTS</span></span>

### <span data-ttu-id="133d3-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="133d3-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="133d3-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="133d3-132">NOTES</span></span>

## <span data-ttu-id="133d3-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="133d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="133d3-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="133d3-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="133d3-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="133d3-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


