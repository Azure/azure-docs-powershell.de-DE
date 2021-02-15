---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145921"
---
# <span data-ttu-id="92e6b-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="92e6b-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="92e6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="92e6b-103">Registrierung eines Ressourcenanbieters wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="92e6b-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="92e6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92e6b-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92e6b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="92e6b-106">Mit **dem Cmdlet "Unregister-AzResourceProvider"** wird die Registrierung eines Azure-Ressourcenanbieters aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="92e6b-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="92e6b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="92e6b-108">Beispiel 1: Aufheben der Registrierung des Ressourcenanbieters mit ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="92e6b-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="92e6b-109">Mit diesem Befehl wird die Registrierung des Ressourcenanbieters "Microsoft.support" aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="92e6b-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="92e6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92e6b-110">PARAMETERS</span></span>

### <span data-ttu-id="92e6b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="92e6b-111">-ApiVersion</span></span>
<span data-ttu-id="92e6b-112">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="92e6b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="92e6b-113">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="92e6b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="92e6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e6b-114">-DefaultProfile</span></span>
<span data-ttu-id="92e6b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="92e6b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e6b-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="92e6b-116">-Pre</span></span>
<span data-ttu-id="92e6b-117">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="92e6b-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="92e6b-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="92e6b-118">-ProviderNamespace</span></span>
<span data-ttu-id="92e6b-119">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="92e6b-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="92e6b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92e6b-120">-Confirm</span></span>
<span data-ttu-id="92e6b-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92e6b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92e6b-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="92e6b-122">-WhatIf</span></span>
<span data-ttu-id="92e6b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92e6b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e6b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92e6b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92e6b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e6b-125">CommonParameters</span></span>
<span data-ttu-id="92e6b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e6b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e6b-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92e6b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e6b-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92e6b-128">INPUTS</span></span>

### <span data-ttu-id="92e6b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="92e6b-129">System.String</span></span>

## <span data-ttu-id="92e6b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92e6b-130">OUTPUTS</span></span>

### <span data-ttu-id="92e6b-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="92e6b-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="92e6b-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="92e6b-132">NOTES</span></span>

## <span data-ttu-id="92e6b-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="92e6b-133">RELATED LINKS</span></span>

[<span data-ttu-id="92e6b-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="92e6b-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="92e6b-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="92e6b-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


