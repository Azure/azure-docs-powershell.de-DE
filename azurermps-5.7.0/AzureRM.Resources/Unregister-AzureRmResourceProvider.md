---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: 875dd42cb0aefd6d6422d99463cd56ace720411a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663426"
---
# <span data-ttu-id="a5bfe-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a5bfe-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="a5bfe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="a5bfe-103">Hebt die Registrierung eines Ressourcenanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5bfe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5bfe-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5bfe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="a5bfe-106">Das Cmdlet " **Unregister-AzureRmResourceProvider** " hebt die Registrierung eines Azure-Ressourcenanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="a5bfe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5bfe-107">EXAMPLES</span></span>

## <span data-ttu-id="a5bfe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5bfe-108">PARAMETERS</span></span>

### <span data-ttu-id="a5bfe-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a5bfe-109">-ApiVersion</span></span>
<span data-ttu-id="a5bfe-110">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a5bfe-111">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-111">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bfe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5bfe-112">-DefaultProfile</span></span>
<span data-ttu-id="a5bfe-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a5bfe-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bfe-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="a5bfe-114">-Pre</span></span>
<span data-ttu-id="a5bfe-115">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bfe-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="a5bfe-116">-ProviderNamespace</span></span>
<span data-ttu-id="a5bfe-117">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="a5bfe-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5bfe-118">-Confirm</span></span>
<span data-ttu-id="a5bfe-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bfe-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5bfe-120">-WhatIf</span></span>
<span data-ttu-id="a5bfe-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5bfe-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bfe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5bfe-123">CommonParameters</span></span>
<span data-ttu-id="a5bfe-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5bfe-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5bfe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5bfe-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5bfe-126">INPUTS</span></span>

### <span data-ttu-id="a5bfe-127">Keine</span><span class="sxs-lookup"><span data-stu-id="a5bfe-127">None</span></span>
<span data-ttu-id="a5bfe-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a5bfe-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5bfe-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5bfe-129">OUTPUTS</span></span>

### <span data-ttu-id="a5bfe-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider]</span><span class="sxs-lookup"><span data-stu-id="a5bfe-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider]</span></span>

## <span data-ttu-id="a5bfe-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5bfe-131">NOTES</span></span>

## <span data-ttu-id="a5bfe-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5bfe-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5bfe-133">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a5bfe-133">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="a5bfe-134">Registrieren-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a5bfe-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


