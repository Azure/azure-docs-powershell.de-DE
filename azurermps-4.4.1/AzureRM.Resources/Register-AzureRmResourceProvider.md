---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 92d94950bc4bc90494482b22b81cbd918c8b6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500722"
---
# <span data-ttu-id="ebb1f-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ebb1f-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="ebb1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ebb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb1f-103">Registriert einen Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebb1f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebb1f-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebb1f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebb1f-105">DESCRIPTION</span></span>
<span data-ttu-id="ebb1f-106">Das Cmdlet **Register-AzureRmResourceProvider** registriert einen Azure-Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="ebb1f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebb1f-107">EXAMPLES</span></span>

## <span data-ttu-id="ebb1f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebb1f-108">PARAMETERS</span></span>

### <span data-ttu-id="ebb1f-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ebb1f-109">-ApiVersion</span></span>
<span data-ttu-id="ebb1f-110">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ebb1f-111">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ebb1f-112">-Pre</span><span class="sxs-lookup"><span data-stu-id="ebb1f-112">-Pre</span></span>
<span data-ttu-id="ebb1f-113">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ebb1f-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ebb1f-114">-ProviderNamespace</span></span>
<span data-ttu-id="ebb1f-115">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="ebb1f-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ebb1f-116">-Confirm</span></span>
<span data-ttu-id="ebb1f-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebb1f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebb1f-118">-WhatIf</span></span>
<span data-ttu-id="ebb1f-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebb1f-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebb1f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb1f-121">-DefaultProfile</span></span>
<span data-ttu-id="ebb1f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebb1f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb1f-123">CommonParameters</span></span>
<span data-ttu-id="ebb1f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb1f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb1f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb1f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ebb1f-126">INPUTS</span></span>

## <span data-ttu-id="ebb1f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ebb1f-127">OUTPUTS</span></span>

### <span data-ttu-id="ebb1f-128">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ebb1f-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="ebb1f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ebb1f-129">NOTES</span></span>

## <span data-ttu-id="ebb1f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ebb1f-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebb1f-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ebb1f-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="ebb1f-132">Registrierung aufheben-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ebb1f-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


