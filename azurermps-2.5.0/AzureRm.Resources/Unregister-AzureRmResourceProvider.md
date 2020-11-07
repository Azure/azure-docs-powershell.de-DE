---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ead0edddccc5372c04e2e4b77d7860bbad29c27a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849023"
---
# <span data-ttu-id="12eed-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="12eed-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="12eed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12eed-102">SYNOPSIS</span></span>
<span data-ttu-id="12eed-103">Hebt die Registrierung eines Ressourcenanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="12eed-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12eed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12eed-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12eed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12eed-105">DESCRIPTION</span></span>
<span data-ttu-id="12eed-106">Das Cmdlet " **Unregister-AzureRmResourceProvider** " hebt die Registrierung eines Azure-Ressourcenanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="12eed-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="12eed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12eed-107">EXAMPLES</span></span>

## <span data-ttu-id="12eed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12eed-108">PARAMETERS</span></span>

### <span data-ttu-id="12eed-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="12eed-109">-ApiVersion</span></span>
<span data-ttu-id="12eed-110">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="12eed-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="12eed-111">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="12eed-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="12eed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12eed-112">-DefaultProfile</span></span>
<span data-ttu-id="12eed-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="12eed-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12eed-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="12eed-114">-Pre</span></span>
<span data-ttu-id="12eed-115">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="12eed-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="12eed-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="12eed-116">-ProviderNamespace</span></span>
<span data-ttu-id="12eed-117">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="12eed-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="12eed-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12eed-118">-Confirm</span></span>
<span data-ttu-id="12eed-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12eed-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12eed-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12eed-120">-WhatIf</span></span>
<span data-ttu-id="12eed-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12eed-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12eed-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12eed-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12eed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12eed-123">CommonParameters</span></span>
<span data-ttu-id="12eed-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12eed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12eed-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12eed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12eed-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12eed-126">INPUTS</span></span>

## <span data-ttu-id="12eed-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12eed-127">OUTPUTS</span></span>

## <span data-ttu-id="12eed-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="12eed-128">NOTES</span></span>

## <span data-ttu-id="12eed-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12eed-129">RELATED LINKS</span></span>

[<span data-ttu-id="12eed-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="12eed-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="12eed-131">Registrieren-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="12eed-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


