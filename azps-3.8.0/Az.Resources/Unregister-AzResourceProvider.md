---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996398"
---
# <span data-ttu-id="cc1fb-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="cc1fb-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="cc1fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1fb-103">Hebt die Registrierung eines Ressourcenanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="cc1fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc1fb-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc1fb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc1fb-105">DESCRIPTION</span></span>
<span data-ttu-id="cc1fb-106">Das Cmdlet " **Unregister-AzResourceProvider** " hebt die Registrierung eines Azure-Ressourcenanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="cc1fb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc1fb-107">EXAMPLES</span></span>

### <span data-ttu-id="cc1fb-108">Beispiel 1: Aufheben der Registrierung des Ressourcenanbieters mit ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="cc1fb-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="cc1fb-109">Mit diesem Befehl wird der Ressourcenanbieter "Microsoft. Support" aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="cc1fb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc1fb-110">PARAMETERS</span></span>

### <span data-ttu-id="cc1fb-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cc1fb-111">-ApiVersion</span></span>
<span data-ttu-id="cc1fb-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cc1fb-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="cc1fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1fb-114">-DefaultProfile</span></span>
<span data-ttu-id="cc1fb-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cc1fb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc1fb-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="cc1fb-116">-Pre</span></span>
<span data-ttu-id="cc1fb-117">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cc1fb-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="cc1fb-118">-ProviderNamespace</span></span>
<span data-ttu-id="cc1fb-119">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="cc1fb-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc1fb-120">-Confirm</span></span>
<span data-ttu-id="cc1fb-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc1fb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc1fb-122">-WhatIf</span></span>
<span data-ttu-id="cc1fb-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc1fb-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc1fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1fb-125">CommonParameters</span></span>
<span data-ttu-id="cc1fb-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc1fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1fb-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc1fb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1fb-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc1fb-128">INPUTS</span></span>

### <span data-ttu-id="cc1fb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cc1fb-129">System.String</span></span>

## <span data-ttu-id="cc1fb-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc1fb-130">OUTPUTS</span></span>

### <span data-ttu-id="cc1fb-131">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="cc1fb-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="cc1fb-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc1fb-132">NOTES</span></span>

## <span data-ttu-id="cc1fb-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc1fb-133">RELATED LINKS</span></span>

[<span data-ttu-id="cc1fb-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="cc1fb-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="cc1fb-135">Registrieren-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="cc1fb-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


