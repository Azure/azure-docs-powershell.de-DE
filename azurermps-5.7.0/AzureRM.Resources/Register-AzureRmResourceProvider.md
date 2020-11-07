---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 9e379df74f974e303faac300515e6bb7844e770b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663432"
---
# <span data-ttu-id="12c2d-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="12c2d-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="12c2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="12c2d-103">Registriert einen Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="12c2d-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12c2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12c2d-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12c2d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="12c2d-106">Das Cmdlet **Register-AzureRmResourceProvider** registriert einen Azure-Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="12c2d-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="12c2d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="12c2d-108">Beispiel 1: Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="12c2d-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="12c2d-109">Dadurch wird der Microsoft. Network-Anbieter für Ihr Konto registriert.</span><span class="sxs-lookup"><span data-stu-id="12c2d-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="12c2d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="12c2d-110">PARAMETERS</span></span>

### <span data-ttu-id="12c2d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="12c2d-111">-ApiVersion</span></span>
<span data-ttu-id="12c2d-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="12c2d-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="12c2d-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="12c2d-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="12c2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c2d-114">-DefaultProfile</span></span>
<span data-ttu-id="12c2d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="12c2d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12c2d-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="12c2d-116">-Pre</span></span>
<span data-ttu-id="12c2d-117">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="12c2d-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="12c2d-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="12c2d-118">-ProviderNamespace</span></span>
<span data-ttu-id="12c2d-119">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="12c2d-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="12c2d-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12c2d-120">-Confirm</span></span>
<span data-ttu-id="12c2d-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12c2d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12c2d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c2d-122">-WhatIf</span></span>
<span data-ttu-id="12c2d-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12c2d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12c2d-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12c2d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12c2d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c2d-125">CommonParameters</span></span>
<span data-ttu-id="12c2d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c2d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c2d-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c2d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c2d-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12c2d-128">INPUTS</span></span>

### <span data-ttu-id="12c2d-129">Keine</span><span class="sxs-lookup"><span data-stu-id="12c2d-129">None</span></span>
<span data-ttu-id="12c2d-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="12c2d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12c2d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12c2d-131">OUTPUTS</span></span>

### <span data-ttu-id="12c2d-132">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="12c2d-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="12c2d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="12c2d-133">NOTES</span></span>

## <span data-ttu-id="12c2d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12c2d-134">RELATED LINKS</span></span>

[<span data-ttu-id="12c2d-135">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="12c2d-135">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="12c2d-136">Registrierung aufheben-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="12c2d-136">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


